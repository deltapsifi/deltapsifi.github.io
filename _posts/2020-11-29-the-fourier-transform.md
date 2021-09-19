---
layout: fouriertransform
author: ΔΨφ
title: "The Fourier Transform"
categories: 
  - "advanced-math"
tags: 
  - "Fourier Transform"
  - "Mathematics"
permalink: /2020-11-29-the-fourier-transform.md/
---

Hello 🖐, I am sorry that you had to wait so long for my next post but the truth is that I had tons of homework from school, and I will do my best to be regular.

In this article I will be giving you an insight into the Fourier Transform. We'll be talking about the definition of The Fourier Transform later, first let's talk about periodicity. Now what exactly is periodicity, it is the tendency of a particular phenomena to repeat at regular intervals. Periodicity is associated with symmetry.

In the case of The Fourier Transform we generally talk about periodicity in space and time. We can write any signal in terms of sinusoids because they are simple and periodic in nature. Let's take a variable "t" which will represent the time domain, then sin(2πt) is also periodic. If we fix the period of a signal to be 1 then the sum of the signals must also have the same period because the whole pattern cannot repeat unless the longest pattern repeats. So let's take the sum of signal.

$latex \\sum\_{k=1}^{n} A\_k sin (2\\pi kt) cos (\\varphi\_k)&s=4&fg=000000$

We can rewrite this as :

$latex \\sum\_{k=1}^{n} a\_k cos {2\\pi kt} + b\_k sin {2\\pi kt}&s=4&fg=000000$

This is the sum of the signal in sines and cosines; however, we usually write the expression of the sum in complex coefficients. This is because it is better, algebraically and conceptually, to write it in this form.

**$latex e^{2\\pi ikt} = cos{2\\pi kt} + isin{2\\pi kt}&s=4&fg=000000$**

This is Euler's formula. Now you may realize that our expression looks really different from this formula; however, through simple algebra we can get the following values for cosine and sine.

i = √-1

$latex cos {2\\pi kt} = \\frac{e^{2\\pi ikt} + e^{-2\\pi ikt}}{2}&s=4&fg=000000$

$latex sin {2\\pi kt} = \\frac{e^{2\\pi ikt} - e^{-2\\pi ikt}}{2i}&s=4&fg=000000$

(I am not showing you the derivation because it's extremely simple and it would be better if you do it yourself; however, if you still have any doubts feel free to [drop me an email](mailto:deltapsifi@outlook.com) and I will answer your queries.)

So in this way we can convert a trigonometric sum to the form :

$latex f(t) = \\sum\_{k = -n}^{n} D\_k e^{2\\pi ikt}&s=1&fg=000000$ where f(t) represents a real signal

Here, we take the summation from "-n" to "n" because we are only considering real signals, and the Dk 's are the complex coefficients. If you will write the expression and make the substitution in terms of the complex exponentials for the coefficients you will find symmetry among them. You should try this yourself it's really interesting and fun to do! When you do this you will find that all the complex terms essentially get cancelled and we get a real function. This is because we took the summation from "-n" to "n".

Here, the complex numbers will satisfy the symmetry property :-

D\-n = $latex D\_{n}^{\*} &s=2&fg=000000$

Let's say we have a periodic function, can we write it as a trigonometric sum / can we express it in terms of sinusoids?

In order to answer this question let's suppose we can write the equation and then find the unknown variable. Here the unknown variable is Dk so let's take any mth term and write it in a way by which we can take the unknown term out and put it on the other side, as follows:-

$latex f(t) = D\_{-n}e^{-2\\pi int} ......... D\_me^{2\\pi imt} .......... D\_{n} e^{2\\pi int}&s=3&fg=000000$

![](https://deltapsifi.files.wordpress.com/2020/11/image-23.png?w=488)

I separated the mth term and then got this equation.

Let's take the exponential term to the other side of the equation.

![](https://deltapsifi.files.wordpress.com/2020/11/image-25.png?w=622)

Now we will integrate this equation from 0 to 1 on both sides.

![](https://deltapsifi.files.wordpress.com/2020/11/image-28.png?w=795)

![](https://deltapsifi.files.wordpress.com/2020/11/image-29.png?w=737)

Now let's evaluate the last term from 0 to 1. When t = 0, only the fraction part is left because e0 \= 1. When t = 1, we get e2$latex \\pi &s=1&fg=000000$i(k-m). "(k-m)" is an integer so we essentially have e2$latex \\pi &s=1&fg=000000$i = cos 2$latex \\pi &s=2&fg=000000$ + i sin 2$latex \\pi &s=2&fg=000000$. Sin 2$latex \\pi &s=2&fg=000000$ = 0 and cos 2$latex \\pi &s=2&fg=000000$ = 1, so we again have the fraction part left as follows :

![](https://deltapsifi.files.wordpress.com/2020/11/image-30.png?w=779)

Therefore, the last term results to 0

Congratulations !! 🥳 You have got an equation to calculate the complex coefficient in the equation of the periodic function that we considered.

$latex D\_k = \\int\_{0}^{1} e^{-2\\pi ikt} f(t) \\cdot dt&s=4&fg=000000$

(I have made a tiny change in this equation : replacing "m" with "k".)

Thus, in order to write a general periodic function of the form $latex f(t) = \\sum\_{k = -n}^{n} D\_k e^{2\\pi ikt}&s=1&fg=000000$ , the coefficient -- $latex D\_k&s=1&fg=000000$ -- has to be given by the formula : $latex D\_k = \\int\_{0}^{1} e^{-2\\pi ikt} f(t) \\cdot dt&s=1&fg=000000$

However, our work is not yet done, we need to verify this again. So stay tuned for Fourier Transform - 2.
