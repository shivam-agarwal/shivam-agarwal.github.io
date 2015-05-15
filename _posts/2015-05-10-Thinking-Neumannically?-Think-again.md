--- 
published: true
title: Thinking Neumannically? Think again ...
layout: post
author: Shivam Agarwal
category: articles
tags: 
- John von Neumann
- von Neumann Architecture
- Universal Turing Machine

---



i7 processors having 2.7 GHz clock speed, boosted to 3.3 GHz. Means in one second 3300000000 clock cycles are executed, capable of executing 92 billion instructions per second.

It certainly leaves you with a chill feeling. Isn’t it?

Do we ever imagine that so much is going on when we simply do a “quick” check of our facebook account and that too several times a day?

This article is going to be about the most basic element which started the revolution of Digital Computers.

<!-- more -->

**Question**- Have you ever wondered that in the name **John von Neumann**, von starts with a small case v?

One of my great teachers always says – “Tum dekhta hai par dekhta nai”, means we see but we don’t observe. The question above stands a testimony of the quote.

While building EDVAC (Electronic Discrete Variable Automatic Computer, a computer weighing 7850 kg.), an architecture was proposed as von Neumann Architecture.

Now why are we discussing an architecture that was introduced over 60 years ago? Because, even today you pick any desktop computer and it still uses the same architecture.

John von Neumann was a great mathematician. As the greatest inventions have simplest underlying principle, von Neumann architecture is no exception.

It says that program and data reside in same memory. There is a connection between CPU and memory (RAM), called bus. At a time CPU can either be fetching/writing data or fetching an instruction from memory. It’s simple right?

If you’re an Undergraduate in Computer Science, I bet some bells must be ringing in your mind. I’ll give you a hint, it’s called – **“Universal Turing Machine”**, which reads data from memory (through a memory tape) executed it and again writes back the result in memory. It’s not just a coincidence for two concepts so similar to emerge in near about the same time. Many of us don’t know but Alan Turing and John von Neumann worked together to shape the computers as we see them today. 

Coming back to the von Neumann architecture, we still use it with some modifications. Like cache has been inserted to get better speed. But that too is only a modification since at a time processor can either fetch an instruction or fetch/write data. So what’s so great about it that we still use it (no offense to sir Neumann). It’s simplicity of performing either of the tasks is the main reason why it’s still used. 

Imagine a computer where Instructions reside in different memory and data in a different one (this is Harvard architecture). The problem will be when to select what has to be done and then the selection would itself require some computation to be done which would again be performed by the same CPU. This complexity has forced processor makers to think in terms of Neumann architecture.

The obvious question would be that if there is only a single bus, wouldn’t it be a drawback in terms of speed? Definitely yes!! 

**The term "von Neumann bottleneck" was coined by John Backus in his 1977 ACM Turing Award lecture.** According to Backus:
## Blockquotes
“Surely there must be a less primitive way of making big changes in the store than by pushing vast numbers of words back and forth through the von Neumann bottleneck. Not only is this tube a literal bottleneck for the data traffic of a problem, but, more importantly, it is an intellectual bottleneck that has kept us tied to word-at-a-time thinking instead of encouraging us to think in terms of the larger conceptual units of the task at hand. Thus programming is basically planning and detailing the enormous traffic of words through the von Neumann bottleneck, and much of that traffic concerns not significant data itself, but where to find it.”

To make it simpler, we all know about instruction set and simple C.

Suppose we want to add two numbers. The c statement will be:

c = a + b;

Where a, b, c are variables.
Finally it will be converted into a sequence of instructions such as:

LDA  a

ADD b

STA  c

Further will be converted to:

DR -> M[a]   //DR- data register M[a]- stands for memory reference at address a. 

AC -> DR         // AC – accumulator register 

DR -> M[b]

AC -> AC + DR

M[c] -> AC


We observe that at one time either the data or an instruction (such as addition) is fetched from memory (and hence the Neumann architecture). 

That means computer has to perform tasks serially? Yes, it performs tasks serially at this level. But today parallelism is achieved today using computers based on von Neumann architectures in a different way through threads and employing multiple processors in a system. You can find a great practical article here. 

But from our previous program we can see how von Neumann architecture forces high level language developers to think in Neumann way. Read ["this"](http://www.cs.cmu.edu/~crary/819-f09/Backus78.pdf) article and you will be amazed.

There are systems build on Harvard architecture. But due to the concept of Cache memory we use today (which is modified Harvard architecture), the Harvard architecture is of little practical use.

In my opinion John von Neumann was a great administrator too, coz he employed the greatest administration rule, which was **Keep It Short and Simple**, unlike this article. :P

Oh I almost forgot to answer: **why v is in small case in the name John von Neumann?**

The answer is- **go GOOGLE it!!**  Self learning is the best.

Be force with you.

Further Read [“The First Draft Report on the EDVAC"](http://qss.stanford.edu/~godfrey/vonNeumann/vnedvac.pdf). 