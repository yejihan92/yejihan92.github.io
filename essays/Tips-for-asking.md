---
layout: essay
type: essay
title: Tips ofr Asking a Good Question!
date: 2020-09-10
labels:
  - StackOverflow
  - Questions
  - Answers
  - Software
---

<img class="ui centered large image" src="../images/Stackoverflow.png">

## Communication with StackOverflow

Many programmers in the world face a lot of challenges while programming. Everyone who has ever experienced programming often has to ask about unknown and unresolved errors. In this case, many programmers nowadays use the open-source community StackOverflow to solve the problem efficiently. In the absence of such as StackOverflow that the open-source community, people who lived in the past read all the books on numerous programs to the people around them and tried to find the cause of the problem and solve it. The open-source community StackOverflow is where programmers from around the world communicate, also, anyone can belong together. There are good questions and answers, but there are many low-quality questions and answers, so there are times when people who asked questions about programs get satisfactory results, and sometimes they get unsatisfactory results. In order for us to program effectively to get good questions and good answers, fist we need to think about the basic etiquette that we must adhere to on StackOverflow before asking or answering.

<img class="ui centered large image" src="../images/library.jpg">

## Be Specific with the Qestion!

<img class="ui centered large image" src="../images/goodquestion.jpg">

There are countless times while programming we come across errors or unknown problems. In that case, just “No! I can't!” Instead of asking for help without any effort, we should think about ourselves enough to solve the problem and ask a question that people feel what we have done for solving the problem. StackOverflow is a question and answer site for professionals and avid programmers, so looking at specific questions and code is why software developers can get useful information most of the time from this website. Let's look at a good example of a StackOverflow question that shows signs of specific and varied attempts.


```
What I want to try:
I want to try the spring cloud config for microservice project where I have a common config for all services and multiple configs for each service.
I got idea on how to use multiple profiles using spring.profiles.active and include. I am trying to understand how can I load multiple configs on config client?

What I have:
In my git repo I have spring-config-repo where I have ...
```
```
application.yml
orderclient.yml
subscriberclient.yml
jmsclient.yml
productclient.yml
```
```
I have my config Server pointed to my config repo.
```
```
spring:
  application:
  name: config-service
  cloud:
   config:
    server:
      git:
        uri: https://github.com/<user>/spring-config-repo

server:
 port: 8888
```
```    
I have my spring client where I want to use multiple configs. Here in my case for orderService I want to load application.yml,orderclient.yml,jmsconfig.yml and For Product microService I need 'orderconfig.yml,jmsclient.yml,productclient.yml'
```
```
spring:
application:
  name: orderclient
profiles:
  active: test
cloud:
  config:
    uri: http://localhost:8888
```
```
Above I can access properties from orderclient.yml.

My Question:
Question1:
How to access properties of jmsclient.yml,productclient.yml in orderclient application.

Question2:
Is there anyway to get list of all propertySources.name exposed by config server? where in above case it should dispaly
```
```
"propertySources": {
  "name": "https://github.com/<>/spring-config-repo/aplication.yml",
     "profiles": <available profiles for this say> Dev, Test,
  "name": "https://github.com/<>/spring-config-repo/orderclient.yml",
     "profiles": <available profiles for this say> Dev, Test
  "name": "https://github.com/<>/spring-config-repo/jmsclient.yml",
     "profiles": <available profiles for this say> Dev, Test
 ....}
```
```
Please let me know if my question is not clear or need more information. Thanks.

```
You can see more detais at the [Good Question Example](https://stackoverflow.com/questions/39215533/spring-cloud-config-how-to-use-multiple-configs).

Asking this question, he clearly explained his problem step by step. Those who responded to his question also provided information on how to solve the problem one by one and sources for answers to that problem. And anyone who's seen his questions can guess that he has tried several and different ways before posting the question.


## Bad Cases

<img class="ui centered large image" src="../images/badtime.jpg">

There are a lot of great questions on StackOverflow, but there are a few things we should avoid. First of all, we should avoid asking questions simply to solve a task without any effort. This makes it impossible for us to program in the future to be creative thinking of programmers. When I can't solve the problem and want to give up due to continuous errors, I think that the greatest attraction of the program is when I solve the errors and succeed and it is the most meaningful. In addition to that, duplicate questions and answers should be avoided. Recently, in Korea, a new era language called "Finger Princess" has emerged when people ask other people around them without even searching for a problem. So, we have to look for similar answers or similar examples to our problem that someone has already done.

```
If I save my A Package in a different directory and trying to import A Package from B Program, how do I do that?

How java finds my package?

I am an android beginner please relate a bit to android as well!
```
You can see more detais at the [Bad Question Example](https://stackoverflow.com/questions/63840848/how-import-keyword-find-other-packages).

We need to look at an example of this question. Such a simple problem can be solved really simply by simply search Google or browsing our computer directory with the least amount of time.

## Conclusion
