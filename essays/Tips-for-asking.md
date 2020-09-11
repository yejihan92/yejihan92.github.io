---
layout: essay
type: essay
title: Tips for Asking a Good Qusetion
# All dates must be YYYY-MM-DD format!
date: 2020-09-10
labels:
  - StackOverflow
  - Questions
  - Answers 
  - Software 
---

<br />
<br />
<p align="center">
<img class="ui image" src="/images/Stackoverflow.png" width="50%" height="60%"/>
 </p>

<ul>

## Communication with StackOverflow

Many programmers in the world face a lot of challenges while programming. Everyone who has ever experienced programming often has to ask about unknown and unresolved errors. In this case, many programmers nowadays use the open-source community StackOverflow to solve the problem efficiently. In the absence of such as StackOverflow that the open-source community, people who lived in the past read all the books on numerous programs to the people around them and tried to find the cause of the problem and solve it. The open-source community StackOverflow is where programmers from around the world communicate, also, anyone can belong together. There are good questions and answers, but there are many low-quality questions and answers, so there are times when people who asked questions about programs get satisfactory results, and sometimes they get unsatisfactory results. In order for us to program effectively to get good questions and good answers, fist we need to think about the basic etiquette that we must adhere to on StackOverflow before asking or answering.
<br />

<p align="center">
<img class="ui image" src="/images/library.jpg" width="50%" height="60%"/>
 </p>
 
<br />
<br />
<br />

## Be specific with the question!

<p align="center">
<img class="ui image" src="/images/goodquestion.jpg" width="50%" height="60%"/>
</p>

There are countless times while programming we come across errors or unknown problems. In that case, just “No! I can't!” Instead of asking for help without any effort, we should think about ourselves enough to solve the problem and ask a question that people feel what we have done for solving the problem. StackOverflow is a question and answer site for professionals and avid programmers, so looking at specific questions and code is why software developers can get useful information most of the time from this website. Let's look at a good example of a StackOverflow question that shows signs of specific and varied attempts.
<br />

```js
import java.util.Scanner;
import java.util.Arrays;
public class searchSorting 
{
    public static void main (String[]args)
    {
        String line;
        int number, search, item, array[], first, last, middle;
        Scanner in = new Scanner(System.in);

        System.out.print("How many numbers you want to input?: ");
        number = in.nextInt();
        array = new int [number];

        item = Integer.parseInt(in.nextLine());
        double[] values = new double[item];

for (int i = 0; i < values.length; i++) {
    System.out.print("Input number " + i + ": ");
    values[i] = Double.parseDouble(in.nextLine());
}
for (int index = 0; index < 5; index++)
    System.out.print(values[index] + "  ");
    in.nextLine();
    Arrays.sort(values);
    System.out.println("Sorted number is: " + Arrays.toString(values));


System.out.println("Enter the number you are looking for?");
      search = in.nextInt();
      first = 0;
      last = (item - 1);
      middle = (first + last)/2;

      while( first <= last )
      {
         if ( array[middle] < item )
           first = middle + 1;
         else if ( array[middle] == item )
         {
           System.out.println(item + " found at location " + (middle + 1) + ".");
           break;
         }
         else
         {
             last = middle - 1;
         }
         middle = (first + last)/2;
      }
      if ( first > last )
          System.out.println(item + " is not found.\n");
   
}}
}


I am feeling quite stupid at this point for not being able to figure out something that is most likely a simple fix. 
I keep getting the error "Exception in thread "main" java.lang.NumberFormatException: For input string: "" at 
java.base/java.lang.NumberFormatException.forInputString(NumberFormatException.java:68) at java.base/java.lang.Integer.parseInt(Integer.java:662)
at java.base/java.lang.Integer.parseInt(Integer.java:770) at searchSorting.main(searchSorting.java:15)" after inputting how many numbers I want to input. 
Others solutions to this problem just don't seem to apply to me somehow. Thanks for the help

```
URL: https://stackoverflow.com/questions/63839319/java-lang-numberformatexception-error-after-inputting-a-number

One of the reasons this question has the same situation to me that I sometimes feel silly when I keep getting the same error when writing assignments or program code. Having had the same experience in the questioner's writing, I can see that he went through a lot of trial and error. And he can see if he thought and tried various attempts and methods to solve the problem. The respondent who answered the question also solved the problem by simply fixing two lines. I think this is one of the great examples of StackOverFlow where there are great programmers who can solve small mistakes we don't see. 
<br />
<br />
<br />

## Bad Cases

<p align="center">
<img class="ui image" src="/images/badtime.jpg" width="50%" height="60%"/>
</p>

There are a lot of great questions on StackOverflow, but there are a few things we should avoid. First of all, we should avoid asking questions simply to solve a task without any effort. This makes it impossible for us to program in the future to be creative thinking of programmers. When I can't solve the problem and want to give up due to continuous errors, I think that the greatest attraction of the program is when I solve the errors and succeed and it is the most meaningful. In addition to that, duplicate questions and answers should be avoided. Recently, in Korea, a new era language called "Finger Princess" has emerged when people ask other people around them without even searching for a problem. So, we have to look for similar answers or similar examples to our problem that someone has already done.
```js
If I save my A Package in a different directory and trying to import A Package from B Program, how do I do that?

How java finds my package?

I am an android beginner please relate a bit to android as well!
}
```
URL: https://stackoverflow.com/questions/63840848/how-import-keyword-find-other-packages

We need to look at an example of this question. Such a simple problem can be solved really simply by simply search Google or browsing our computer directory with the least amount of time.
</ul>

<br />
<br />
<br />
<br />
<br />
<br />
