---
layout: post
title:  "Financial Trend Analysis"
date:   2014-08-11 08:42:21 -0800
categories: selenium testing
---
Purpose - to visualize spending habits and identify trends. 

Basic process overview

- gather data files from various locations
- process data files into one format
- perhaps [date, transaction amount, name]
- graph the unified data
- first pass just graphs all the transactions
- at a later point we could make improvements to the graph

Bash file to parse a bank export:

{% highlight bash %}
#!/bin/bash

INPUT=bank_datafile.csv
OLDIFS=$IFS
IFS=,
[ ! -f $INPUT ] && { echo "$INPUT file not found"; exit 99; }
while read date no description debit credit
do
       if [ ${#credit} -gt 0 ] ;then
        amount=$credit
    else
        amount=$debit
    fi

    echo $date,$( printf "%.2f" $amount ),$description
done < $INPUT
IFS=$OLDIFS
{% endhighlight %}

Remove the double quotes and multiple spaces:

{% highlight bash %}
$ sed -i.bak 's/"//g' pre_parsed_datafile.csv
$ sed -i.bak ’s/  / /g’ pre_parsed_datafile.csv
{% endhighlight %}

Read the parsed file and print data:

{% highlight python %}
import csv
import datetime
import time

with open('cleaned_transaction.data', newline='') as f:
    reader = csv.reader(f)
    for row in reader:
        date_str = row[0]

        date_num = datetime.datetime.strptime(date_str, "%m/%d/%y")
        seconds_since_epoch = time.mktime(date_num.timetuple()) * 1000
        print(seconds_since_epoch,",", row[1])
{% endhighlight %}

Plot arrays of data:

{% highlight python %}
import matplotlib.pyplot as plt
x = [1378191600000.0 ,1378191600000.0 ,1378105200000.0 ]
y = [-9.89,-10.48,-5.69]
plt.plot(x,y,'ro')
plt.show()
{% endhighlight %}

![Financial analysis](/assets/screenshot.jpg)
