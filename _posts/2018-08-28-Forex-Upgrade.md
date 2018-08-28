---
layout: post
title:  "Upgrading Forex"
date:   2018-08-28 15:42:00 +0800
categories: blog
---

For as long as I can remember, I have been taught to play in the Metatrader 4 world and script in Metaeditor with MQL4. After a long while, I have decided to try out MQL5 and Metatrader 5. Oh boy, did I regret tthe upgrade.

## MQL5 Community

But let's start with the community. I didn't spend any time here at all prior to this August 2018, but after browsing the Forums, Codebases, Market, and a few other things, I realize how cool the community is. Lots of good tips and tricks and pointers into using Metatrader 5. I guess you could say that was them trying to sell me to join Metatrader 5.

### Before joining Metatrader 5 platform

I was enjoying metatrader 4 but I saw some convenient stuff going on in Metatrader 5. The indicators are way more advanced than the ones in Metatrader 4. Building the bot in Metatrader 5 was, as they put it, able to build a quick one with just a few clicks here and there, and then run it. They were right, it was easy. I made a simple RSI bot that could give in a Profit factor of 1.08 after I optimize it for XM MT5 Servers.

The other fun stuff was using the SVN feature to host my code. So wherever I am, as long as I use a Metatrader 5 and login to the MQL5 Community in it, I can retrieve my codes back again and continue working on my template/script/indicator/Expert Advisor. SVN is basically git but for the more visual and mouse-clickers. No more running `git add . && git commit -m "some commit message" && git push` commands. It was neat.

I was and am trading manually and then realized that I can easily share my trading charts to MQL5 Community. Its as simple as a right-click "Save as Picture", and check the "Share to MQL5 Community" box. I guess you could say that this is becoming more of a social trader platform (which I enjoy).

### After joining Metatrader 5 platform

Its not the same as trading with TradingView though. I like the community there way better than MQL5. Lots of active chat and sharing analysis and such. Its way more fun. But meh, I can easily just switch between Metatrader and TradingView. Although, I am considering on looking at the different brokers that TradingView has available. I wish OANDA has an Islamic account. Makes way more fun with their API.

Speaking of API, XM still doesn't have any. Looking up over at earnforex.com lead me to look at RoboForex and OctaFX as potential API broker (potentially into cTrader, I guess). Imagine if I could just run a trading script on a Linux box, leave it running and just keep paying my Internet bill and top-up my electricity (or just hook up my Raspberry Pi to a Solar Powered Battery lol).

The Metatrader 4 may not have advance features as Metatrader 5 (easy way of registering a signal) but it does have easier way of scripting MQL4 in the Metaeditor. From a single line for a BUY ORDER in MQL4, its a 5 line code in MQL5. Thankfully, I only have to do it once. The rest is as simple as just importing into the `Include` folder (this can also be done in both platforms).

## MT5 > MT4, deal with it

Even with some disadvantages, MT5 still is better than MT4. Better performance, faster and much secure trades, etc. I'm still a long way from building a better trading bot but until I do, gotta keep trading.
