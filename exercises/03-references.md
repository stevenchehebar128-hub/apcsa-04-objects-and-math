# Exercise 3: Reference Drills (S13 homework)

Every snippet below uses the `Pet` class from `src/ObjectLab.java`:

```java
Pet(String name, int age)   // sets both
Pet(String name)            // age starts at 1
getName()   getAge()   birthday()   // birthday() adds 1 to age
```

For snippets 1 to 6: **draw** the variables and objects (a box per object, an arrow per reference variable), then write the output. Do this BEFORE you run anything. Draw on paper and paste a photo link, or sketch it as text in the picture box.

## Snippet 1
```java
Pet a = new Pet("Rex", 3);
Pet b = new Pet("Rex", 3);
a.birthday();
System.out.println(a.getAge() + " " + b.getAge());
```
Picture:
a-----> rex and is 3
b-----> rex and is 3


Output:3 3

## Snippet 2
```java
Pet a = new Pet("Rex", 3);
Pet b = a;
a.birthday();
System.out.println(b.getAge());
```
Picture:
a------> rex and is 3
b------> rex and is 3
Output:3

## Snippet 3
```java
Pet a = new Pet("Mia");
Pet b = new Pet("Zed", 9);
b = a;
b.birthday();
System.out.println(a.getAge() + " " + b.getName());
```
Picture:
a-----> mia and is 1
b-----> mia and is 1
Output:

## Snippet 4
```java
String s = "Java";
String t = s;
s = s + "!";
System.out.println(s + " " + t);
```
Picture:
s-----> Java1
t-----> Java


Output:Java! Java

## Snippet 5
```java
int x = 5;
int y = x;
y++;
System.out.println(x + " " + y);
```
Picture:
x---->5
y---->x(5) 
y++----> 6

Output:5 6

## Snippet 6
```java
Pet a = new Pet("Rex", 3);
Pet b = a;
a = null;
System.out.println(b.getName());
```
Picture:
a----> rex and is 3
b----> rex and is 3
a----> null 

Output:rex

## Snippet 7 (this one crashes)
```java
Pet a = new Pet("Rex", 3);
Pet b = a;
a = null;
b = null;
System.out.println(a.getName());
```
- Exception name:NullPointerExeption 
- Line that crashes:last line
- Which variable is null?both but only a is being used
- Your fix (one line of code): take out a = null

## Snippet 8: write your own
Write a snippet where two variables alias one `Pet`, then explain its output in two sentences.

```java
Pet a = new Pet("james", 9);
Pet b = a
Pet c = a 
System.out.println(a.getName() + " " + b.getName() + " " + c.getName());
System.out.println(a.getAge() + " " + b.getAge() + " " + c.getAge());
Explanation:We made an original pet and then made two copys of that pet (a) and we made two lines of print with their ages and their names. 

## Checked my predictions
Which snippets did I get wrong, and what was I assuming?
