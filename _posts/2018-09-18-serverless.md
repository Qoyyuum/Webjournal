---
layout: post
title:  "Serverless"
date:   2018-09-18 10:10:00 +0800
categories: blog
---

Have always been interested in #Serverless architecture. Today I learnt about [OpenStack](https://trystack.org/), an open source cloud operating system for any data center that wishes to become a private/public cloud. Skimmed through the docs to find that its very labour intensive. So that's a scratch in a dream but why though?

Serverless is sort of a buzzword and that many find that its really helpful for app developers. Bad news for system engineers though as their job has been replaced by such a service but only up to a small margin of the public job. 

Either way, I find it very beneficial because I don't have to worry or care about building up log routes, rotates, management, security patches, upgrades, backups, disaster recoveries, load balancing, and everything in between for scalability and optimization for running a high available app in any particular VM or container.

### AWS Lambda

I've been eyeing on using their Lambda service. I even tried to deploy a quick Django app to it to see if I can even deploy it right. Something about `You must specify a region` error that's preventing me from a successful deployment in using a `Zappa` service. Well that's annoying. I guess I'll have to try and deploy Django as much as I can and as easily as I can, the serverless way, if not Zappa.

Here's an [intro video](https://www.youtube.com/watch?v=plUrbPN0xc8) on using Zappa.

### Why Serverless?

Other than the benefits above, I won't have the luxury of time and effort to battle against server issues. Just focus on coding and adding new and exciting features to the app and keep on building.

Can't wait to try again later this weekend.