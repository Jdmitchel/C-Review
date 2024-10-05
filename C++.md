
# Introduction to C++

What is C++?
- C++ was created in 1979 by a Danish developer Bjarne Stroustrup, and was released to the public in 1983.
- C++ is an intermediate language level, as it falls between machine readability and human interpretation.
- C++ allows for higher level control over system and memory resources.
- C++ is an extension of the C language.

Where can you write C++ code?
- Notepad
- Compliers (Dev C++, VsCode, Eclipse, Codeblocks, NetBeans)
---

# Hello World

The first step to writing code starts with "Hello World".
After installing or preparing your ideal coding tool. make sure that the end of the file has `.cpp`, this will indicate that you are writing in C++.

```
#include <iostream> // iostream stands for standard input/output
using namespace std; // namespace std is used to make the code easier to write

int main(){ // int is used as the return type, letting the user know the program run successfully 
	cout << "Hello World!"; // cout is used to print to the screen and ; is used to end the line of code
	return 0;
} // make sure to close your code with curly braces.


```


---

# Data Types

## Strings

What is a string?
- A string is a series of stored characters.
- A string of characters is placed between double quotation marks (" ")
- A string in C++ is initialized using `string (variable)`. 

```
eg. 
string name = "John_Doe";

or

string name;
cin >> name; 
cout <<"Hello " << name
```
## Characters

What is a character?
- A character is a single ASCII value/symbol 
- A character occupies 1byte in memory
- `char (variable)` 

```
eg.

char letter = 'A'

or

char a = 65, b = 66, c = 67


```
## Integers

What is an integer?
- An integer is a defined as a whole number unit used for various operations
- Positive and negative whole numbers are integers
- `int (variable)`

```
eg.
int age = 99

```
## Float

What is a float?
- Float is a floating point number or a number that contains a decimal place
- `float (variable)`

```
eg.
float num = 10.2
```
## Double
What is double?
- Double is a data type that accepts whole and floating point number.
- Double has a length of 64 bits or 8 bytes
```
eg.
double num = 1000000.05687;
```

## Long

What is long?
- Long is used to store large integer data types 
- long int (variable). memory bytes 4
- long long int (variable) memory bytes 8

```
eg.
int num = 100000, num2 = 200000;
long int answer = num* num2;
cout << answer;


```


## Boolean

What is boolean?
- boolean variable operates using binary operation (True/False)
- bool (variable)
```
eg.
bool alive = True;

or 

bool positive = (1==1);
```


## Bitwise Operators
What is bitwise operation?
- A character that represents an action taken on data at the bit level
- `&` - AND = 1 and 1 = 1 else 0
- `|` - OR = 1 or 0 = 1 (one must be true to be true)
- `^` - XOR = 1 or 0 = 1 (only if one statement is true)
- `~` - Complement 
- `<<` - Left shift = Math ( num << 1 = (num << 0) * *2)
- `>>` - Right shift = Math ( num >> 1 = (num >> 0) /2)

```
Keep the table below in mind for binary numbers.
128|64|32|16|8|4|2|1|
 0 | 1| 0| 0|0|0|1|1| => 67  eg

General variables throughout 
int a = 12, b = 25
-----------------------------------------------------------------------------
AND
cout << a&b; // answer 8

OR
cout << a|b; // answer 29

XOR
cout <<a^b; // answer 21
-----------------------------------------------------------------------------

1's Complement
 a = 12 //binary 00001100
 ~a; // answer binary (11110011) = decimal (243)

2's Complement
follows the standard of 1 complement but you add 1 after. this is used to find the bitwise complement of the decimal value.

int a = 12
cout << ~a;

answer will be -13
-----------------------------------------------------------------------------

Left shift
The bits are shifted towards the left by a certain number of specified bits.
The left most bit is discarded and the right most bit remains vacant (replaced by 0).

int number = 12
for(int i =0; 1<= 2; 1++){
	cout << (number << i); // 0 -> 12, 1 -> 24, 2 -> 48
}
-----------------------------------------------------------------------------

Right shift
The bits are shifted towards the right by a certain number of specified bits.
The least significant bit is discarded, while the most significant bits are replaced by zero.

int number = 12
for(int i =0; 1<= 2; 1++){
	cout << (number >> i); // 0 -> 12, 1 -> 6, 2 -> 3
}
-----------------------------------------------------------------------------

```

## Mathematical Operations
Mathematical operations.
- `+` - Addition -> Adds values together
- `-` - Subtraction -> Subtracts values from one another
- `*` - Multiplication -> Multiples values
- `/` - Division -> Divides one value from one another
- `%` - Modulus -> Returns the remaining values from division
- `++` - Increments a value of a variable by 1
- `--` - Decrements the value of a variable by 1
- `( )` - Defines the order of power or the means at which operations are to take place



## Writing and Printing to the screen

To print to the screen `cout` is used and to write to the screen (type), `cin` is used.

```
int main(){
	string s;
	int age;

	cout<<"What is your name?" << endl;
	cin>>s;
	cout <<"How old are you?" <<endl;
	cin>>age;

	cout<<"My name is " << s << ", I am "<< age << " years old";
	
}

```


## Conditional Statements

What are conditional statements?
- conditional statements are operations or actions when the requirements are meet, they are indicated as True.
- in programing it is represented using if, else and while .

### If Statements

```
eg. 1

int a = 1;
int b = 2;
if(b>a){
	cout<<"two bee or not two bee";
}else{
	cout<<"One way out";
}
-----------------------------------------------------------------------------

eg. 2

int age = 20

if(age==0){
	cout<<"baby";
}
if(age <= 17){
	cout<<"child";
}
if(age > 18){
	cout<<"you are old";
}
-----------------------------------------------------------------------------

eg. 3

int a = 5, b = 10;

if (a>0 && b >0){
	cout<<"Both values are positive";
}
-----------------------------------------------------------------------------

eg. 4

int a = 8;
if((4+3) != a){
	cout<<"A is larger than 4 + 3";
}


```


### For Loops

What is a loop?
- Loops are an essential concept that allows execution of a block of code repeatedly until a condition is meet.
- A for loop is used when you know the number of times you want to traverse through the block of code.
- a `for` loop consists of an initialization statement, a condition and an increment/decrement operation.

```
eg. 1
for(int i = 0; i<10; i++){
	cout<<i <<"Iteration"<<endl;
}
-----------------------------------------------------------------------------
eg.2

int week = 3, day = 7;

for (int i = 0; i< week; i++){
	cout << "Week: "<< i<<endl;
	for(int j = 1; j < day; j++){
		cout <<" Day: "<< j <<endl;
	}
}
-----------------------------------------------------------------------------

eg. 3

int rows = 5, columns = 5, i;

for (i = 1; i<=rows; i++){
	for(int 1; j <= columns; j++){
		cout<< *;
	}
	cout<<endl;
}


```


### While Loops
What are while loops?
- while loops are are type of loop that continues until a certain condition is meet.
- the loop check if the condition is meet before entering.

```
eg. 1

bool alive = True;
int age = 0;

while(alive){
	if(age < 99){
		age++;
		alive = True;
	}else{
		alive = False;
	}
}

eg. 2

int num = 0;
while(num <10){
	cout<< "Number: "<< num<<endl;
	num++;
}

```


## Do-while 

What is do-while?
- Do while is similar to a while loop, with the difference being that the loop body is executed at least once even when the condition is false.

```
eg.

int num = 0;
do{
	cout<<"Number: "<< num<<endl;
	num++;
}while(num<5);

```


## Functions 

What are functions?
- A function is a group of statements that perform a specific task, organized as a separate unit of operation.
- functions allow for code to be reused.
- functions aid with writing clean code.

There are 2 different types of functions.
- `Standard Library`- these are predefined code such as sort(), strlen(), sqrt() and various others. These code functions are part of a standard library for use and must be imported using the appropriate headers.
- `User-defined functions`- these functions are created by use the developers for a specific purpose. The function must be defined and called when needed for use.

```
A function can be defined 
=> return type function_name(parameter list){}

- return type: This is the output product by the function.
- function name: name given to the function (use standard C++ naming convention). Names must be meaningful.
- parameter list: the list of input parameters/arguments that are needed to perform tasks. The arguement can also be left blank.

eg. 
int sum(int n, int m){return n+m}
void display(string words){ cout<<words<<endl;}
boolean compare(int level, int experience){.....}

```

### Function Prototypes

What are function prototypes?
- A function prototype is a function declaration without its body and information. 
- It informs the compiler about the function's name, return type and parameters.

Initially you would type the function before main to allow for execution. Essentially with function prototyping you can call the function after main as long as you call the prototype before main's execution.

```
eg.

int product(int x, int y);

int main(){
	int num1 = 10, num2 = 5;
	int result = product(num1, num2); // calling the function
	cout <<"The product: "<< result<<endl;
	return 0;
}

int product(int x, int y){return x*y;}


```


## Recursion 

What is recursion?
- A function that calls itself is a recursive function.
- [Recursive Call](https://www.programiz.com/sites/tutorial2program/files/cpp-function-recursion-working.png)
- A recursive function will continue until a condition is met.
- Thus to create an effective recursive function that does not go on infinitely, a specific terminating condition must be implemented (if, else statement).

```
eg.

Factorial

int factorial(int n);

int main(){
	int n, result;
	cout<<"enter a number: ";
	cin >> n;

	if(n<=0){
		cout<<"re-enter the number: ";
		cin >> n;
	}

	result = factorial(n);
	cout<< "Factorial of "<<n<<" = " << result;
	return 0;
}

int factorial(n){
	if(n == 1){
		return 1;
	}else{
		return n * factorial(n-1)
	}
}


eg 2.

Sum of natural numbers

int Sum(int n);

int main(){
	int n;

	cout<< "Type a postive, no negative whole number: ";
	cin>> n;

	int result = Sum(n);
	cout<< "The sum of natual numbers is: " << result;
	return 0;

}

int sum(int n){
	if(n !=0)
		return n + sum(n-1);
	return 0;
}


eg. 3

Highest Common Factor

int HCF(int num, int num2);

int main(){
	int num1, num2;

	cin >> num1 >> num2;
	int result = HCF(num1, num2);

	cout<< "The highest common factor of " << num1 << " and " << num2 << "is: " << result; 
	return 0;

}

int HFC(int num1, int num2){
	if (num2 !=0)
		return HFC(num2, num1%num2);
	else
		return num1;
}



```


## Arrays

What are arrays?
- an array is used to store multiple values of the sane data type in consecutive memory locations.

An array starts at index 0, unless assigned otherwise.

```
type name [elements] // the elements within the square brackets represent the number of the elements in the array and the number must be a constant expression.

int values[5]; // the integer aray is named values and contains 5 elements

int values[5] = {12, 10, 32, 0, 99}; //explicitly initializing values to the array.

cout << values[0]; // this will print the element in index 0

int values[5] = {}; // empty array

Both declarations below are valid
int values[] = { 10, 20, 30, 40};
int values[] {10, 20, 30, 40};


```

Code Example
```
#include <iostream>
using namespace std;

int arr[] = {16, 2, 77, 40, 12071};
int n, res =0;

int main(){
	for(n=0, n<5; n++){ // loops 5 times starting at 0
		result += arr[n]; // the array index is used to locate the element stored and add and store the values into the variable result 
	}
	cout<< result; //answer 12206
	return 0;
}

```

To discuss
- array traversal
- array addition and deletion to an array
- 
## Multidimensional Arrays




## ASCII



## Pointers



## Sorting 




## Searching 



## Structs



## Linked Lists



## Trees and Graphs







---


# Resources 

1. [Roadmap](roadmap.sh)
2. [CS50](https://pll.harvard.edu/course/cs50-introduction-computer-science)
3. [Codex](codedex.io)
4. 

---
