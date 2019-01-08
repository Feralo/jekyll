---
layout: post
title:  "Errors, Faults, Defects and Failures"
date:   2015-12-30 07:59:21 -0800
categories: Software Engineering update
---
The terms and their associated definitions are not consistently used in my
workplace, although I am trying to change that. After reading chapter 2, I
began to use the terms as defined in the book [Burnstein], and people have been
slightly caught off guard. I find it annoying that practically every software
inadequacy is labeled ‘bug’, and the only alternative that I have heard (with
less frequency) is ‘runtime error’. However, based on the textbook definitions,
it should just be called a 'software failure’, since the definition implies
that it occurs at runtime.

Similar to using the terms ‘sedan', ‘coup’ or ‘station wagon’ instead of
‘vehicle’; the notion of categorization allow us to speak with precision.
Failures are the end result of errors. Faults (or defects) are errors that may
(or may not be) manifested as failures. The linguistic specificity allows for
thinking about verification with greater precision.

Consider the following example: a software product halts abruptly when a
certain action is invoked under certain circumstances. If a team were limited
to only describing it as a ‘bug’ that caused the 'runtime error’, then they
would set out to find the bug and fix it: problem solved. However, with these
three terms (Error, Fault & Failure) in their repertoire, they could say: “This
unfortunate failure was caused by a mis-informed requirement, let’s find and
eradicate the defect and then correct the business requirement that was the
root cause". Having a broader vocabulary enables more robust reasoning and
allows for a more complete solution.

Furthermore, these are loaded terms: 'Error' doesn't simply connote a problem,
it tells us the problem came from a programmer's misunderstanding. Likewise,
'Failure' indicates that the deficiency has made it's way into code and that
inhibits the software product from performing.

Conclusion: these terms are not common in my workplace, but we could work more
efficiently if they were in common use.

References
Burnstein, I. (2003), Practical Software Testing: A Process-Oriented Approach (Springer Professional Computing), Springer .
