---
title: "05 - Java Sockets"
date: 2023-02-26
draft: false
author: "Jailani Rahman"
image: /images/topic05_banner.png
description: ""
toc:
---

## 5. Java Sockets

### 5.1. Lecture Notes
<div>{{<embed-pdf url="../resources/05a - Java Socket.pdf">}}</div>

### 5.2. Exercises

#### 5.2.1. Exercise 1

<div>{{<embed-pdf url="../resources/05b - Java Socket Exercise I.pdf">}}</div>

#### 5.2.2. Exercise 2

![](../resources/05c%20-%20Java%20Socket%20Exercise%20II.png)

```java
import java.util.*;
import java.net.*;
import java.io.*;

public class GuessingClient {

	public static void main(String[] args) throws Exception {
		// 192.168.0.100
		Socket socket = new Socket("localhost", 9102);
		System.out.println("Connected to server");
		DataInputStream fromServer = 
				new DataInputStream(socket.getInputStream());
		DataOutputStream toServer =
				new DataOutputStream(socket.getOutputStream());
		
		String welcomeMsg = fromServer.readUTF();
		System.out.println(welcomeMsg);
		
		Scanner scanner = new Scanner(System.in);
		
		while(true) {
			System.out.println("Your turn.");
			System.out.println("Guess a number from 1 to 100:");
			int guessedNumber = Integer.parseInt(scanner.nextLine());
			toServer.writeInt(guessedNumber);
			
			System.out.println(fromServer.readUTF());
			if(fromServer.readBoolean()) {
				break;
			}
		}
	}
	
}
```

```java
import java.net.*;
import java.util.Random;
import java.io.*;

public class GuessingHandler implements Runnable {

	Socket player1, player2;
	DataInputStream fromPlayer1, fromPlayer2;
	DataOutputStream toPlayer1, toPlayer2;
	
	public GuessingHandler(Socket player1, Socket player2) {
		this.player1 = player1;
		this.player2 = player2;
	}
	
	public void run() {
		try {
			fromPlayer1 = new DataInputStream(player1.getInputStream());
			fromPlayer2 = new DataInputStream(player2.getInputStream());
			toPlayer1 = new DataOutputStream(player1.getOutputStream());
			toPlayer2 = new DataOutputStream(player2.getOutputStream());
			
			String welcomeMsg = "Connected: Starting guessing game as ";
			toPlayer1.writeUTF(
					welcomeMsg + "player 1.");
			toPlayer2.writeUTF(
					welcomeMsg + "player 2.");
			
			Random random = new Random();
			int randomValue = random.nextInt(99) + 1;
			System.out.println(randomValue);
			
			while(true) {
				int player1Guess = fromPlayer1.readInt();
				int player2Guess = fromPlayer2.readInt();
				
				byte player1Result =
						calculateWin(randomValue, player1Guess);
				byte player2Result =
						calculateWin(randomValue, player2Guess);
				
				String result1 = "";
				String result2 = "";
				boolean stopGame = false;
				if(player1Result == 1 && player2Result == 1) {
					result1 = "Draw";
					result2 = "Draw";
					stopGame = true;
				} else if(player1Result == 1 && player2Result != 1) {
					result1 = "You win";
					result2 = "You lose";
					stopGame = true;
				} else if(player1Result != 1 && player2Result == 1) {
					result1 = "You lose";
					result2 = "You win";
					stopGame = true;
				} else {
					if(player1Result == 2) {
						result1 = "Your guess is less than the random value.";
					} else {
						result1 = "Your guess is more than the random value.";
					}
					if(player2Result == 2) {
						result2 = "Your guess is less than the random value.";
					} else {
						result2 = "Your guess is more than the random value.";
					}
				}
				toPlayer1.writeUTF(result1);
				toPlayer2.writeUTF(result2);
				toPlayer1.writeBoolean(stopGame);
				toPlayer2.writeBoolean(stopGame);
				if(stopGame) {
					break;
				}
			}
			
		} catch (Exception e) {
			e.printStackTrace();
		}
	}
	
	public byte calculateWin(int randomValue, int playerGuess) {
		if(randomValue == playerGuess) {
			return 1;
		} else if (playerGuess < randomValue) {
			return 2;
		} else {
			return 3;
		}
	}
	
}
```

```java
import java.net.*;

public class GuessingServer {

	public static void main(String[] args) throws Exception {
		ServerSocket serverSocket = new ServerSocket(9102);
		System.out.println("Server has started.");
		
		while(true) {
			Socket player1 = serverSocket.accept();
			Socket player2 = serverSocket.accept();
			
			new Thread(new GuessingHandler(player1, player2)).start();
		}
	}
	
}
```

### 5.3. Practicals

```java
import java.net.*;
import java.io.*;
import java.util.Date;
import java.util.Scanner;

public class BasicClient {

	public static void main(String[] args) throws Exception{
		Scanner scanner = new Scanner(System.in);
		// 127.0.0.1
		Socket socket = new Socket("192.168.0.104", 9001);
		System.out.println("Connected to server since " + new Date());
		
		DataOutputStream toServer = new DataOutputStream(
				socket.getOutputStream());
		
		while(true) {
			System.out.println("Please input msg:");
			String msg = scanner.nextLine();
			toServer.writeUTF(msg);
			System.out.println("Sent msg: " + msg);
			
			if(msg.equalsIgnoreCase("q")) {
				System.out.println("Application terminated.");
				break;
			}
		}
		
		scanner.close();
		toServer.close();
	}
	
}
```

```java
import java.net.*;
import java.util.Date;
import java.io.*;

public class BasicServer {

	public static void main(String[] args) throws Exception {
		ServerSocket serverSocket = new ServerSocket(9001);
		System.out.println("Server is running as of " + new Date());
		Socket socket = serverSocket.accept();
		System.out.println("Client connected.");
		
		DataInputStream fromClient = new DataInputStream(
				socket.getInputStream());
		
		while(true) {
			System.out.println("Waiting msg from client");
			String msg = fromClient.readUTF();
			System.out.println("Received msg: " + msg);
			
			if(msg.equalsIgnoreCase("q")) {
				System.out.println("Server terminated.");
				break;
			}
		}
		
		fromClient.close();
	}
	
}
```

```java
import java.net.*;
import java.io.*;
import java.util.Date;

public class MultipleClientServer {

	public static void main(String[] args) throws Exception {
		ServerSocket serverSocket = new ServerSocket(9001);
		System.out.println("Server is running as of " + new Date());
		while(true) {
			Socket socket = serverSocket.accept();
			System.out.println("Client connected.");
			
			new Thread(new Runnable() {
				public void run() {
					DataInputStream fromClient = null;
					try {
						fromClient = new DataInputStream(
								socket.getInputStream());
						
						while(true) {
							System.out.println("Waiting msg from client");
							String msg = fromClient.readUTF();
							System.out.println("Received msg: " + msg);
							
							if(msg.equalsIgnoreCase("q")) {
								System.out.println("Server terminated.");
								break;
							}
						}
					} catch (Exception e) {
						
					} finally {
						if(fromClient != null) {							
							try {
								fromClient.close();
							} catch (IOException e) {
								// TODO Auto-generated catch block
								e.printStackTrace();
							}
						}
					}
				}
			}).start();
		}
		
	}
	
}
```

```java
import java.net.*;
import java.util.Scanner;
import java.io.*;

public class CircleClient {
	
	static DataInputStream fromServer;
	static DataOutputStream toServer;
	static Socket socket = null;

	public static void main(String[] args) {
		try {
			socket = new Socket("localhost", 9101);
			System.out.println("Connected to the server.");
			
			communicate();
		} catch (IOException e) {
			System.out.println("Problems connecting to server");
		} finally {
			if(socket != null) {
				try { socket.close(); } catch (IOException e) {}
			}
		}
	}
	
	public static void communicate() {
		Scanner scanner = new Scanner(System.in);
		try {
			fromServer = new DataInputStream(socket.getInputStream());
			toServer = new DataOutputStream(socket.getOutputStream());
						
			while(true) {
				System.out.println("Please type radius value ("
						+ "negative value will terminate app)");
				double radius = Double.parseDouble(scanner.nextLine());
				toServer.writeDouble(radius);
				if(radius < 0) {
					System.out.println("App terminated");
					System.exit(0);
				}
				double area = fromServer.readDouble();
				System.out.println("Area received: " + area);
			}
		} catch (IOException e) {
			System.out.println("Problems communication with server.");
		}
		
		
		scanner.close();
	}
	
}
```

```java
import java.net.*;
import java.io.*;

public class CircleServer {

	public static void main(String[] args) {
		ServerSocket serverSocket = null;
		try {
			serverSocket = new ServerSocket(9101);
			System.out.println("Server has started.");
			while(true) {
				Socket socket = serverSocket.accept();
				
				new Thread(new CircleSessionHandler(socket)).start();
			}
		} catch (IOException e) {
			System.out.println("Unable to start server.");
		} finally {
			if(serverSocket != null) {				
				try { serverSocket.close(); } catch (Exception e) {}
			}
		}
	}
	
}
```

```java
import java.net.*;
import java.io.*;

public class CircleSessionHandler implements Runnable {
	
	Socket socket;
	DataInputStream fromClient;
	DataOutputStream toClient;
	
	public CircleSessionHandler(Socket socket) {
		this.socket = socket;
	}

	public void run() {
		try {
			fromClient = new DataInputStream(socket.getInputStream());
			toClient = new DataOutputStream(socket.getOutputStream());
			
			while(true) {
				System.out.println("Waiting radius from client.");
				double radius = fromClient.readDouble();
				if(radius < 0) {
					System.out.println("Client disconnected");
					break;
				}
				double area = Math.PI * radius * radius;
				toClient.writeDouble(area);
				System.out.println("Received radius: " + radius +
						", Sent area: " + area);
			}
			
		} catch (IOException e) {
			System.out.println("Problem communicating with client.");
		} finally {
			if(socket != null) {
				try { socket.close(); } catch (IOException e) {}
			}
			if(fromClient != null) {
				try { fromClient.close(); } catch (IOException e) {}
			}
			if(toClient != null) {
				try { toClient.close(); } catch (IOException e) {}
			}
		}
	}

}
```