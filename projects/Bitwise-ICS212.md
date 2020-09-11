---
layout: project
type: project
image: images/Bitwise operators.png
title: Bitwise Project
permalink: projects/bitwise
# All dates must be YYYY-MM-DD format!
date: 2020-09-04
labels:
  - C language
  - C programming
  - Bitwise
summary: A program that has four functions using bitwise operators of UH UNIX shell
---

<br />
<br />
<p align="center">
<img class="ui image" src="/images/bitwise4.png" width="100%" height="100%"/>
</p>
## Bitwise Project (KCC ICS212 project)

This Bitwise program is to write a program that contains 4 functions that take 6 command line arguments and use bitwise operators. One of the reasons this project was so important was its deep connection to the final project of the ICS212 class. Briefly explaining what the program should do, the user has to enter command-line arguments separated by 6 spaces. Next, the user needs to enter 4 characters (all ASCII characters) followed by 2 integers. If 4 characters and 2 integers separated by 6 spaces are not entered in sequence, the program should print an error message telling the user the correct input and exit the program.
<br />
<br />
<br />
<br />

Run the program and convert the command line input to "unsigned char" and "unsigned int" data types. If a negative integer input, unsigned is a part that we must pay attention to as there is no negative integer, so we should be careful looping. Looking at each function of the function,
```js
int twoComplement(unsigned int number) {
    int onesComplement = ~number;
    return onesComplement + 1;
}
```
twoComplement function needs to calculate the two's complement of the input parameter, so use "~" to return.
<br />
```
unsigned int charPacker(unsigned char ch1, unsigned char ch2, unsigned char ch3, unsigned char ch4) {
    unsigned int number = 0;

    number = (number | ch1) << 8;
    number = (number | ch2) << 8;
    number = (number | ch3) << 8;
    number = number | ch4;

    return number;
}
```
charPacker function compresses 4 characters into a single integer, so 8-bit characters are compressed into 32-bit integers using the left shift operator << and the bitwise OR operator |.
<br />
```
void intChopper(unsigned int number, unsigned char* ch1, unsigned char* ch2, unsigned char* ch3, unsigned char* ch4) {
    unsigned int mask = 0x000000FF;

    *ch4 = number & mask;
    *ch3 = (number >> 8) & mask;
    *ch2 = (number >> 8) & mask;
    *ch1 = (number >> 8) & mask;
}
```
Conversely, intChopper function truncates the integer into 4 characters and uses the right shift operator >> and bitwise AND operator & with a mask to separate the 32-bit integer into 4 8-bit parts.
<br />
```
unsigned int circleLeft(unsigned int count, unsigned int number) {
    return (number << count) | (number >> (32 - count));
}
```
circleLeft function is to perform a circular left shift of the bit, so it can be written as above.
<br />
<br />
<br />
<br />

In C programming, bit operators are basic content, but bit operators are important because they are a helpful concept when processing signals related to hardware, and it is a content that developers who do C programming must know exactly. Therefore, I learned the basic principle of working bitwise through this project that numbers on a computer don't really behave like numbers.
<br />
<br />
<br />
<br />


You can learn more about c language bitwise at the [Programiz Website](https://www.programiz.com/c-programming/bitwise-operators).

<br />
<br />
<br />
<br />

