---
layout: post
title:  "Denyhosts instructions (updated)"
date:   2015-01-22 17:59:21 -0800
categories: Fedora systems
---
[Steve Jenkins][jenkins] did a fine write up on the subject of denyhosts in 2010.

Here are a few notes about the command sequence that is needed now:

Install denyhosts:

`# yum install denyhosts`

Don't lock yourself out:

`# vim  /var/lib/denyhosts/allowed-hosts`

Enable the service:

`# systemctl enable denyhosts.service`

Start the service:

`# systemctl start  denyhosts.service`

Verify that it is started:

`# systemctl status denyhosts`

Watch it in action:

`# tail -f /var/log/denyhosts`

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[jenkins]: http://www.stevejenkins.com/blog/2010/11/how-to-install-denyhosts-to-block-ssh-attacks-on-rhel-6-centos-5-5-fedora-14/
