- Download `jdk` and install it according to your platform
#### Key definitions
- `PACKAGE` => `package com.company;` => A package in java is used to group related classes. Think of it as a folder in a file directory.
- `FUNCTIONS` => `public static void main(String[] args){}` => functions which execute and holds the code , all the functions are in `class`
- `CLASS` => `public class Main {//Function }` => class which have many functions
#### Naming conventions
- For classes we use `PascalConvention`
- For functions we use `camelCaseConvention`
---
## DATA Types and Variables
- `Main` method is essential for java program
- Types of data types
	- Primitive Data type
		- `int` `byte` `long` `float` `double` `char` `short` `bool`
	- Non Primitive Data type
		- Will write it later
- `Variables` => variables are containers whose value can be changed
- Eg :- `int number = 8` 
- `Constants` => Constants are containers whose value can not be changed
#### Primitive Data types
- `byte` => Takes 1 byte , Default value is 0.
- `short` => Takes 2 byte , Default value is 0.
- `int` => Takes 4 byte , Default value is 0.
- `float` => Takes 4 byte , Default value is 0.0f .
- `long` => Takes 8 byte , Default value is 0.
- `double` => Takes 8 byte , Default value is 0.0d .
- `char` => Takes 2 byte (because it supports unicode) , Default value is `\U0000`.
- `boolean` => can be `true` or `false` , Default value is `false`.
---
#### Little snippit 
- Adding three numbers and printing its output
```java
public class Main {  
public static void main(String[] args) {  
// Application which adds three numbers and print its output  
int num1 = 123;  
int num2 = 321;  
int num3 = 233;  
int sum = num1 + num2 + num3;  
System.out.println("sum of " + num1 + "," + num2 + " and " + num3 + " is " + sum);  
}  
}
```
--- 
## Literals in JAVA
- A constant value which can be assigned to the variable is called as a literal
- `101`  => Integer literal
- `10.1f` => Float literal
- `10.1` => double literal (default decimal value is double)
- `11111111111111111111111L` => Long literal
- `'A'` => Character literal
- `true` => boolean literal
- `"Tanishq"`=> String literal
---
## Getting user input in Java `Scanner`
- `TalkingInput.java`
```java
import java.util.Scanner;  
  
public class TalkingInput {  
public static void main(String[] args) {  
Scanner sc = new Scanner(System.in);  

System.out.println("Talking input where whole line is considered input:- ");  
System.out.println(sc.nextLine());  
  
}  
}
```
---
#### Exercise => Converting km to miles
```java
import java.util.Scanner;  
  
public class Exercise1 {  
public static void main(String[] args) {  
// Changing kilometers to miles  
Scanner sc = new Scanner(System.in);  
System.out.println("Enter the km's");  
float km = sc.nextFloat();  
float miles = km*(0.621371f);  
System.out.println("Converted to miles:==> " + miles );  
  
}  
}
```
---
## JAVA Operators / Types of operators and expression in JAVA
- Types of operators
	- Arithmetic operator => `+,-,*,/,%,++,--`
	- Assignment operator => `==,+=`
	- Comparison operator => `==,>=,<=`
	- Logical operator => `&&,||,!`
	- Bitwise operator => `&,|`   (operates bitwise)

```java
...
int b = 9;
b += 4;
b *= 3; // Assignment operator
System.out.println(b);
System.out.println(64>5 && 64>8); // Logical operators
System.out.println(64>5 || 2>8); // Logical operators
...
```
---
### Precedence and Associativity of operators

![PnAOA](https://github.com/root-tanishq/CLSS/blob/main/Images/PnAOA.png)
---
### Resulting data types after arithmetic operation
![dataTypes](https://github.com/root-tanishq/CLSS/blob/main/Images/dataTypesAfterArithmeticOperations.png)
---
### Increment / Decrement Operators
```java
int i = 56;
System.out.println(i++); //56 (first use the i then increment its value)
System.out.println(i); //57
System.out.println(++i); //58 (first increment then use its value)
System.out.println(i); //58
```
---
## If else and else if statement
```java
if (condition) {
 // code to run
} else if (condition) {
// code to run
} else {
// code to run
}

```
```java
if (condition)
//one line of code to run;
```
--- 
## Switch statements
```java
switch (word) {
case 1:
//code to run
break;
case n:
//code to run
break;
default:
//Default code to run
}
```
--- 
## LOOPS
- for loop
- while loop
- do while loop
> `for` loop
```java
for(initialisation;condition;updation) {
// do something
}

for(int c = 0; c < 3 ; c++){
	System.out.println("Hello World!!!");
}
```
>`while` loop
```java
while(condition) {
// do something
}

int i = 0;
while(i < 11) {
	System.out.println("Hello World!");
	i++;
}
```
> `do while` loop
```java
do {
// do something
} while(condition);

int i = 0;
do {
	System.out.println(i);
	i = i + 1;
}while(i < 11);
```
---
## Arrays in JAVA
- kind of python list but little fancy 
```java
// Syntax
type[] arrayName = new type[size];

// Actual Example
int[] marks = new int[3];
marks[0] = 76; //defining value into a particular place
marks[1] = 26;
marks[2] = 61;

// another way of defining array
type[] arrayName = {1,2,3,n};

// its example
int marks[] = {97,96,56};
```
---
## 2D Arrays
```java
// Syntax
type[] [] arrayName = new type[rows] [columns];

// Example
int[] [] numbers = new int[3] [5];

// Location calling
numbers[0] [1]
numbers[1] [3]
```
---
## `Strings` Non primitive data type 
```java
// String declaration
String name = "Tanishq";
String fullName = "Tanishq Rathore";

// Scanner taking from user
String inputName = sc.next();
String inputName = sc.nextline();

//-> String manipulation

// Concatination
String firstName = "Tanishq";
String lastName = "Rathore";
String fullName = firstName + " " + lastName;

// Length calculation
System.out.println(fullName.length());

// charAt
for(int i=0; i<fullName.length(); i++){
	System.out.println(fullName.charAt(i));
}

//String comparison
String name1 = "Tony";
String name2 = "Tony";

if(name1.compareTo(name2) == 0){
//1 s1 > s2  +ve value
//2 s1 == s2  0
//3 s1 < s2  -ve value
System.out.println("Strings are equal");
}

// Substring
String sentence = "My name is Tony";
// substring(beginning index , end index )
String name = sentence.substring(11 , sentence.length())
```
---
## String builder
- Strings in java are Immutable thats why we use String builder to alter and make changes to data
```java
StringBuilder sb = new StringBuilder("Tony");

// get character
System.out.println(sb.charAt(0));

// set character
sb.setCharAt(0, 'P');
System.out.println(sb);

// Insert
sb.insert(0 , 'S');
System.out.println(sb);

sb.insert(2 , 'n');
System.out.println(sb);

// deleter characters
sb.delete(2,3);
System.out.println(sb);

// Appending
sb.append(" Stark");
System.out.println(sb);

// Length
System.out.println(sb.length());
```
---
## Operators
- `+`,`-`,`*`,`/`,`%` => Binary operators
- `++`,`--` => Unary operators
	- Pre Increment `++a`
	- Post increment `a++`
- `==`,`!=`,`>`,`<`,`>=`,`<=` => Relational operator
- `&&`,`||`,`!` => Logical operators 
- `&`,`|`,`^`,`~`,`<<`,`>>` => Bitwise operator
- `==`,`+=`,`-=`,`*=`,`/=` => Assignment operator
---
## Bit Manipulation
- Things we wil learn here
	- Get , Set , Clear , Update

#### Get Bit 
- Bit Mask `1<<i`
- Operation `AND`
- `1<<2`
```java
int n = 5;
int pos = 2;
int bitMask = 1<<pos;
if((bitMask & n) == 0) {
	System.out.println("bit was zero");
}else {
	System.out.println("bit was one");
}
```
#### Set Bit
- Bit Mask `1<<i`
- Operation `OR`
```java
int n = 5;
int pos = 2;
int bitMask = 1<<pos;
int newNumber = bitMask | n;
System.out.println(newNumber);
```
### Clear bit
- Bit Mask `1<<i`
- Operation `AND with NOT`
```java
int n = 5;
int pos = 2;
int bitMask = 1<<pos;
int notBitMask = ~(bitMask);

int newNumber = notBitMask & n;
System.out.println(newNumber);
```
#### Update bit
- For 0 => CLEAR Opeation
- Bit Mask `1<<i`
- Operation `AND with NOT`
- For 1 => Set Operation
- Bit Mask `1<<i`
- Operation `OR`
---
