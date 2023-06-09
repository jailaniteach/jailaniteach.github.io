---
title: "04 - Java Binary Input & Output"
date: 2023-02-12
draft: false
author: "Jailani Rahman"
image: /images/topic04_banner.png
description: ""
toc:
---

---

## 4. Java Binary Input & Output

---

### 4.1. Lecture Notes
<div>{{<embed-pdf url="../resources/04a - JavaIO.pdf">}}</div>

<br>

---

### 4.2. Exercises
<div>{{<embed-pdf url="../resources/04b - Java IO Exercise.pdf">}}</div>

<br>

---

### 4.3. Practicals

#### 4.3.1. Practical 1

```java
import java.io.*;

public class LearningFileInputStream {

	public static void main(String[] args) {
		try(FileInputStream input =
				new FileInputStream("data.dat")) {
			int value;
			while((value = input.read()) != -1) {
				System.out.println(value);
			}
		} catch (FileNotFoundException e) {
			System.out.println("Inda jua ada tu.");
		} catch (IOException e) {
			System.out.println("Boh.");
		}
	}
	
}
```

```java
import java.io.*;

public class LearningFileOutputStream {

	public static void main(String[] args) {
		File file = new File("data.dat");
		try(FileOutputStream output = 
				new FileOutputStream(file)) {
			for(int i = 1; i <= 10; i++) {
				output.write(i);
			}
		} catch (FileNotFoundException e) {
			System.out.println("Nada file atu");
		} catch (IOException e) {
			System.out.println("Ada masalah");
		}
	}
	
}
```

<br>

---

#### 4.3.2. Practical 2

```java
import java.io.*;

public class LearningDataInputStream {

	public static void main(String[] args) throws Exception {
		try(
			DataInputStream input = new DataInputStream(
					new FileInputStream("data.dat"));	
				) {
			System.out.println(input.readInt());
			System.out.println(input.readDouble());
			System.out.println(input.readUTF());
		}
	}
	
}
```

```java
import java.io.*;

public class LearningDataOutputStream {

	public static void main(String[] args) throws Exception {
		try(
			DataOutputStream output = new DataOutputStream(
					new FileOutputStream("data.dat", false));	
				) {
			output.writeInt(100);
			output.writeDouble(78.5);
			output.writeUTF("Jailani");
		}
	}
	
}
```

```java
import java.io.*;
import java.util.Date;

public class LearningObjectInputStream {

	public static void main(String[] args) throws Exception {
		try(
			ObjectInputStream input = new ObjectInputStream(
					new FileInputStream("object.dat"));	
				) {
			System.out.println(input.readUTF());
			System.out.println(input.readInt());
			System.out.println(input.readObject());
			Student student1 = (Student) input.readObject();
			System.out.println(student1.id + " " + student1.name);
			Student student2 = (Student) input.readObject();
			System.out.println(student2.id + " " + student2.name);
			Student student3 = (Student) input.readObject();
			System.out.println(student3.id + " " + student3.name);
		}
	}
	
}
```

```java
import java.io.*;
import java.util.Date;

public class LearningObjectOutputStream {

	public static void main(String[] args) throws Exception {
		try(
			ObjectOutputStream output = new ObjectOutputStream(
					new FileOutputStream("object.dat"));	
				) {
			output.writeUTF("Jailani");
			output.writeInt(50);
			output.writeObject(new Date());
			Student student = new Student("22FTT1234", "Abu",
					new Group("DITN12", 11));
			output.writeObject(student);
			Group group2 = new Group("DITN11", 10);
			Student student2 = new Student("21FTT1567", "Bakar",
					group2);
			output.writeObject(student2);
			Student student3 = new Student("21FTT2143", "Curi",
					group2);
			output.writeObject(student3);
		}
	}
	
}
```

```java
import java.io.Serializable;

public class Student implements Serializable {

	String id;
	String name;
	Group group;
	
	public Student(String id, String name, Group group) {
		super();
		this.id = id;
		this.name = name;
		this.group = group;
	}
	
}
```

```java
import java.io.Serializable;

public class Group implements Serializable {

	String name;
	int intake;
	
	public Group(String name, int intake) {
		this.name = name;
		this.intake = intake;
	}
	
}
```

---