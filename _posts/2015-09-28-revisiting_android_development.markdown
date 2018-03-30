---
layout: post
title: "Revisiting Android Development"
date: 2015-09-28
categories: Java Android
---
I recently had the opportunity to return to Android application development
(after a break of almost 4 years) with some new friends while studying the
software development process. Android development was not the focus of this
exercise, the application was merely one of the artifacts produced.

I had completely forgotten how verbose Java is! However, I was very glad to see
that JUnit is around to keep the testing goat happy... No, wait. The testing
goat is from Python.

Anyways, it's fun to stay up to speed with different languages and frameworks -
especially when you don't have to re-learn it all from scratch on your own.

Here are a few things that I found to be handy while I was working:

{% highlight bash %}
$ rm -rf ~/.android/avd/emulatorNameIWantToDelete.*
{% endhighlight %}

or however you might feel comfortable navigating to a hidden directory and
deleting something. It came in handy when I had a virtual device that always
thought it was still running.

{% highlight bash %}
$ git remote add upstream https://github.com/noah-de/ORIGINAL_REPOSITORY.git
$ git fetch upstream
$ git checkout master
$ git merge upstream/master
{% endhighlight %}



or however you might feel comfortable navigating to a hidden directory and
deleting something. It came in handy when I had a virtual device that always
thought it was still running.


The handy type check that is available to us in Python is a little more verbose
in Java:

{% highlight java %}
System.out.println(object.getClass().getName());
{% endhighlight %} 

Today I was asked why I ended all my lines with semi-colons - ehh... I have been
writing Java.
