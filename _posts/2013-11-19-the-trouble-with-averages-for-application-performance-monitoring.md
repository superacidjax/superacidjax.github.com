---
layout: post
title: "The Trouble With Averages For Application Performance Monitoring"
description: ""
category: "Rails"
tags: [rails, performance]
---
{% include JB/setup %}

Most web application performance tuning starts with an almost obsession with
average response times. The problem with average response times is that we
tend to make the assumption that the average would be evenly distributed.
Yehuda Katz and Tom Dale from [Tilde](http://tilde/io) make an excellent point
about how this is wrong. If web application performance were distributed like
human heights were distributed, then it wouldn't be unusual to see a 12 foot
person occassionally on the street or a 2 foot person.

Using average response times is a bad idea because your responses aren't ever
distributed as a bell curve.

The reason the averages become useless is because the programming language you're
using is Turing Complete and has branches. As an example, the performance
characteristics of a cache hit versus a cache miss are completely different. So
in an If statement you have a cache hit, then it's going to be very fast, but
a cache miss would then result in the program doing some expensive computation,
however those two response times are averaged which gives you a completely
worthless number.

Instead, it's better to look at the average worst response time
(at the 95th percentile.) This would be the average worst response your users
would get.

For example, good performance is worthless if it's not consistent. So having
200ms, 200ms, 200ms is much better than having 50ms, 50ms, 1 second. The 95th
percentile measurement simply means that 1 out of 20 requests made by a user
will hit this worst response time. The 95th percentile isn't an outlier, it's
a slow request that your users will routinely hit. Which ultimately translates
into a degraded user experience that isn't reflected by using average response
time as a measurement.

## The Point

Chasing average response times can be helpful as a vanity metric, however it
doesn't actually measure how well your application is performing for each user.
If every 20th request is taking 5 seconds, those 200ms requests aren't very
appealing anymore, even though your average request time might only be 300ms.