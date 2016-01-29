---
id: 162
title: 'Error: Child Returned Status'
date: 2012-02-07T11:51:00+00:00
author: Qoyyuum
layout: post
guid: http://blog.qoyyuum.me/?p=162
permalink: /error-child-returned-status/
blogger_blog:
  - qoyyuum.blogspot.com
blogger_author:
  - Abdul Qoyyuum Haji Abdul Kadir
blogger_permalink:
  - /2012/02/error-child-returned-status.html
blogger_internal:
  - /feeds/1705353048896399216/posts/default/5765166530940797936
tags:
  - linux
  - ubuntu
  - xampp
---
I entered this command into the terminal:  
tar xvfz xampp-linux-1.7.3a.tar.gz -C /opt

And I get:  
tar (child): xampp-linux-1.7.3a.tar.gz: Cannot open: No such file or directory  
tar (child): Error is not recoverable: exiting now  
tar: Child returned status 2  
tar: Error is not recoverable: exiting now

I tried sudo to it and it still doesn&#8217;t work. What do I do?