---
id: 550
title: Using Inline CSS vs Block CSS Displays
date: 2014-12-30T17:09:39+00:00
author: Qoyyuum
layout: post
guid: http://blog.qoyyuum.me/?p=550
permalink: /using-inline-css-vs-block-css-displays/
videourl:
  - 
categories:
  - Programming
  - Quora
tags:
  - CSS
---
I don&#8217;t know why but the WordPress Share function at Quora.com doesn&#8217;t seem to work. So I&#8217;m copying and pasting it here.

* * *

# Question : How do I add navigation on one side and content on the other?

Details of the Question:

This is my HTML: <span class="qlink_container"><a class="external_link" href="http://pastebin.com/4j5BeuE6" target="_blank">[HTML] Default &#8211; Pastebin.com</a></span>
  
This is my CSS: <span class="qlink_container"><a class="external_link" href="http://pastebin.com/rRg9EpSU" target="_blank">[CSS] DefaultCSS &#8211; Pastebin.com</a></span>

<div>
  <img class="landscape qtext_image zoomable_in zoomable_in_feed" src="http://qph.is.quoracdn.net/main-qimg-69b7d09735b74954b9fd36378785fb20?convert_to_webp=true" alt="" />
</div>

I want my webpage to look similar to this, in which way would I have to change my CSS in order to make it like that? Also, how do I remove the bullet points?

<!--more-->

* * *

## The Answer (<a href="http://www.quora.com/How-do-I-add-navigation-on-one-side-and-content-on-the-other" target="_blank">link</a>)

So let&#8217;s start with the easy part.

**Removing Bulletpoints**
  
To remove bullet points, you just need to change the list-style to none, like so:

<table class="codeblocktable">
  <tr>
    <td class="linenos">
      <pre>1
2
3
</pre>
    </td>
    
    <td class="code">
      <div class="codeblock">
        <pre><span class="">li {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class=""> list-style: none;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
    </td>
  </tr>
</table>

**Tuning your HTML**
  
Using the table tag in HTML is actually the quickest way to achieve that kind of layout that you wanted. But nowadays, designers go for div and specify width in CSS instead of tables. So remove all tables in your HTML. And while we&#8217;re at it, I saw this:

<div class="codeblock inline_codeblock">
  <pre><span class="">&lt;div class="mainContent"&gt;</span></pre>
</div>

I don&#8217;t see any CSS in relation to that class, so to speed up the loading of the page (slightly), let&#8217;s remove that too.

**Fixing up your CSS**
  
I have changed the following:

  * All of that padding of _different dimensions_ in one line is great but I don&#8217;t see the need to specify on both _sides_ for _navigator_ class and _content_ class. So I made it specific to _padding-left_.
  * The content class&#8217;s float should be _left_ instead of _right_. Float right still works but it just looks odd across multiple screen sizes.
  * The content class&#8217;s display should be using _inline css_ instead of _inline-block._ An inline-block would take up the whole row, thus moving the content element, down on to its own new row.
  * Lastly, I added a _width_ to the _content_ class so that the browser understands how big this box is and can and should fit next to the navigator. **Pro tip**: you can set this to _max-width,_ so it will only size up to that amount of width and shrink automatically on any screen sizes.

<table class="codeblocktable">
  <tr>
    <td class="linenos">
      <pre> 1
 2
 3
 4
 5
 6
 7
 8
 9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
</pre>
    </td>
    
    <td class="code">
      <div class="codeblock">
        <pre><span class="">body {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    font-size: 15px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">#header {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    background-color: #000000;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    padding: 20px 200px 20px 200px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    margin: 10px 200px 10px 200px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    text-align: center;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    color: white;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    font-family: Impact, 'Times New Roman', sans-serif;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    font-size: 30px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">#header:hover {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    color: #BABABA;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">#navigator {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    text-decoration: none;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    float: left;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    list-style: none;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    padding-left: 100px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">#navigator a {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    color: white;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    background-color: #19D1BC;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    margin: 2px 0px 2px 0px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    padding: 5px 10px 5px 10px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    text-align: center;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    text-decoration: none;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    float: left;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    width: 150px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    list-style: none;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">#navigator a:hover {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    background-color: #118C7E;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    font-size: 17px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">.content {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    max-width: 400px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    float: left;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    display: inline;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">    padding-left: 50px;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class=""> </span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">li {
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">  list-style: none;
</span></pre>
      </div>
      
      <div class="codeblock">
        <pre><span class="">}
</span></pre>
      </div>
    </td>
  </tr>
</table>

Have a look at my CodePen. <span class="qlink_container"><a class="external_link" href="http://codepen.io/Qoyyuum/full/myrQgZ/" target="_blank" data-tooltip="attached">A Pen by Abdul Qoyyuum</a></span>
  
The only thing left to do is to adjust the sizes on the width, padding and margin of each until satisfied.