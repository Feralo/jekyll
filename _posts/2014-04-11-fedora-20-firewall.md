---
layout: post
title: Basic setup of Fedora 20 firewall
date: 2014-04-11
categories: Linux Fedora
---
After almost a decade of using Centos and Red Hat, jumping into Fedora 20 can be quite a learning experience, let's take one step at a time.

To start with, firewall administration is now administered through zones which are administered with the firewall-cmd . In order to start making use of anything with a Linux command line utility, one must start by knowing the state of things:

{% highlight bash %}
$ firewall-cmd --state
$ firewall-cmd --list-all-zones
$ firewall-cmd --zone=public --list-ports
{% endhighlight %}

If you don't have the necessary ports open, they can be opened up explicitly:

{% highlight bash %}
$ firewall-cmd --zone=public --permanent --add-port=80/tcp
$ firewall-cmd --zone=public --permanent --add-port=22/tcp
{% endhighlight %}

or you can use the pre-defined zones:

{% highlight bash %}
$ firewall-cmd --add-service=http --permanent
{% endhighlight %}
