---
layout: post
title: Informal Analysis of an Unknown Algorithm
tags:
- computer science
- udacity
- algorithms
---

So, as of earlier today I've been working through the [Algorithms course on
Udacity][1], and I wanted to work through the lesson 1 naive algorithm analysis
example in writing, so I could get a good grasp on the actual process of
analyzing it. Then I figured I might as well write it up a little neater so I
could actually publish it somewhere for posterity, and this blog post happened.


I'd also like to preface this by saying yes, I'm aware people could potentially
(though I don't think I get enough linking for it to be likely) use my analysis
and conclusion to "cheat" at the problem. And all I'll say to that is... if
you're just looking for the answer to the question, rather than trying to work
it out, you're probably not going to get much out of the course.


So, without further ado, let's get stuck in.


The code given for the algorithm itself is fairly simple:

    def naive(a, b):
        x = a
        y = b
        z = 0
        while x > 0:
            z = z + y
            x = x - 1
        return z


So... what does it do?


Well, first I'll start by breaking it down into two chunks - initialization, and
then the main loop.


The initialization is simply setting `x` and `y` as variables initially
duplicating the values of ``a`` and `b` (and is pretty much useless in real
terms, since Python passes ints by value, but that's irrelevant to the
analysis), and adds a new variable `z`, which starts out as 0.


The loop is the real meat of the algorithm, and it does two things:

- It increments `z` by the value of `y`.
- It decrements `x` by 1.


It also runs only while `x` is greater than 0 - combining this with
decrementing `x` by 1, and nothing else changing `x`, this means we know the
loop body will run `x` times.


Since `x` is never used to directly modify `z`, we can now ignore it beyond
remembering that it's the number of iterations of the loop. That means that in
practical terms, the loop's only effect is to increment `z` by `y` each time
it runs.


Since `y` never changes, this means `x` times, we increment `z` by `y`.
Or, in other words, it is `(x * y)` more than when we started.


Finally, since `z` starts as 0, its final value is `0 + (x * y)`, where
`x` is the original `x`, or to simplify, `z = x * y`. Since the original
`x` and `y` were equal to `a` and `b`, the algorithm's purpose is to
multiply `a` by `b`.


(Thanks for reading, if you got this far without boredom. I'd be interested to
hear if anyone found this post interesting, and especially if anyone would like
to see me step through similar processes when I run into them.)


[1] https://www.udacity.com/course/cs215
