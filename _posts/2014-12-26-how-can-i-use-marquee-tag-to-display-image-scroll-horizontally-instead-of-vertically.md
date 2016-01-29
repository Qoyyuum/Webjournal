---
id: 531
title: How can I use marquee tag to display image scroll horizontally instead of vertically?
date: 2014-12-26T11:22:56+00:00
author: Qoyyuum
layout: post
guid: http://blog.qoyyuum.me/?p=531
permalink: /how-can-i-use-marquee-tag-to-display-image-scroll-horizontally-instead-of-vertically/
videourl:
  - 
categories:
  - Quora
---
Answer by Abdul Qoyyuum :

> There are 2 ways to fix this problem as far as I know:
  
> 1. Don&#8217;t use **li**
  
> All li elements are displayed as a **block** in its own row and not inline. That&#8217;s how lists are supposed to work. Instead, change it to use something else like a **span** or **div** instead. Or just the **img** on its own.
  
> 2. Add CSS
  
> You can trick it out by adding the following properties to the **li** in CSS like so:
> 
> <table class="codeblocktable">
>   <tr>
>     <td class="linenos">
>       <pre>1
2
3
4
</pre>
>     </td>
>     
>     <td class="code">
>       <div class="codeblock">
>         <pre><span class="">li {
</span></pre>
>       </div>
>       
>       <div class="codeblock">
>         <pre><span class=""> float: left;
</span></pre>
>       </div>
>       
>       <div class="codeblock">
>         <pre><span class=""> display: inline;
</span></pre>
>       </div>
>       
>       <div class="codeblock">
>         <pre><span class="">}
</span></pre>
>       </div>
>     </td>
>   </tr>
> </table>

<span class="qlink_container"><a href="http://www.quora.com/How-can-I-use-marquee-tag-to-display-image-scroll-horizontally-instead-of-vertically/answer/Abdul-Qoyyuum-Haji-Abdul-Kadir">How can I use marquee tag to display image scroll horizontally instead of vertically?</a></span>