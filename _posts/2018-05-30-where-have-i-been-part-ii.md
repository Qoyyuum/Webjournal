---
layout: post
title:  "Where have I been? (Part 2)"
date:   2018-05-28 12:12:00 +1000
categories: blog
---

# A Year Gap

So what's that big gap in between 2016 and 2018? I got a job... I meant to post that I did managed to switch to a different company. Something way more suited for my speed and skills and the opportunity to grow. I work for a FinTech company that implements card payments into systems, existing or new. I was hired to maintain the existing systems. Learning the ropes, there's a whole new side to other than app/site development.

## What have I learnt?

Not spilling all of the company secrets but I'm somewhat a SysAdmin to [DevOps](https://en.wikipedia.org/wiki/DevOps) but not exactly DevOps yet. The work has me maintaining a High Availability system that has dreplicated streaming databases of PR, DR and Test environments for multiple clients that has the company's FinTech implemented. All of this is logged by `rsyslog` installed in every host of each environment. Passwords are extremely long and complicated (like 20-25~ characters long, jumbled in alphanumeric and special characters) and stored in a self-hosted Password Manager. The whole thing is RedHat based so there's loads of `yum` commands at the beginning of each projects. Configuration management for each host is handled by [Puppet](https://puppet.com/) and maintained in a versioning tool, [Gitlab](https://about.gitlab.com/installation/)

The whole system and environments are monitored for any issues by a monitoring tool, [Nagios](https://www.nagios.com/products/nagios-xi/) and security intelligence and event management with [AlienVault](https://www.alienvault.com/products/ossim) would help track for any hackers and other nasty programs that might break into the system.

But I have to keep my eyes and ears open on the tickets generated by Nagios to [RequestTracker](https://bestpractical.com/request-tracker/).

I don't really have to touch the application because, it doesn't fail/break at all.

## Oh and I have just fixed this Webjournal

It was broken for over a year. Didn't bother fixing it because I couldn't be bothered. But now I did. The problem was actually simple. The site route doesn't match with the `_config.yml` file where the `baseurl: ""` part was, what I assumed just enter `baseurl: "Webjournal"` but that didn't work. Apparently, it doesn't need it as a string? But just as `baseurl: Webjournal` and that fixed the whole CSS problem.

## What's next?

I have my Fedora set up, a good job that I appreciate and happy with and a family to support. I don't know what's next. I'll just wing it but at the same time, do a really good job at what I do, learn everything, be an expert, and contribute to open-source community with what I know (while not giving away company secrets, of course).
