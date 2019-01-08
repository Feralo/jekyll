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
