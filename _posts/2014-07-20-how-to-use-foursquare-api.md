---
id: 9
title: How to use Foursquare API
date: 2014-07-20T06:00:00+00:00
author: Qoyyuum
layout: post
guid: http://blog.qoyyuum.me/?p=9
permalink: /how-to-use-foursquare-api/
blogger_blog:
  - qoyyuum.blogspot.com
blogger_author:
  - Abdul Qoyyuum Haji Abdul Kadir
blogger_permalink:
  - /2014/07/how-to-use-foursquare-api.html
blogger_internal:
  - /feeds/1705353048896399216/posts/default/3806924388794069223
categories:
  - Android
tags:
  - android
  - app
  - coding
  - computer
  - design
  - framework
  - Graphical user interface
  - JavaScript
  - Programming
  - project
  - prototype
  - web
  - web adventure
  - Web application
---
## What is an API?

<div>
  API stands for Application Programming Interface. It&#8217;s simply a way to get information and pass information to trusted partners.
</div>

<div>
</div>

<div>
  You can view what it is via the video below.
</div>

<div style="clear: both; text-align: center;">
</div>

<div style="clear: both; text-align: center;">
</div>

<div style="clear: both; text-align: left;">
  So now that&#8217;s out of the way, let&#8217;s look at an API. Do note, that not all APIs are alike but they construct the same. To use an API, one must first understand about URLs.
</div>

<div style="clear: both; text-align: left;">
</div>

<a name='more'></a>
  


<h2 style="clear: both; text-align: left;">
  It&#8217;s all in the URL
</h2>

<div style="clear: both; text-align: left;">
  Unified Resource Location is what it stands for. A standard URL that we all know goes like this:
</div>

<div style="clear: both; text-align: left;">
  <a href="http://www.foursquare.com/">www.foursquare.com</a>
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: left;">
  I&#8217;ll be using Foursquare as an example for this quick tutorial.
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: left;">
  The API&#8217;s URL looks something like this (<a href="https://developer.foursquare.com/start/search" target="_blank">as taken from their </a><a href="https://developer.foursquare.com/start/search" target="_blank">docs</a>):
</div>

<div style="clear: both; text-align: left;">
</div>

> **https://api.foursquare.com/v2/venues/search?client\_id=CLIENT\_ID&client\_secret=CLIENT\_SECRET&v=20130815&ll=40.7,-74&query=sushi**

<div style="clear: both; text-align: left;">
  To access any information stored by those programs (like Facebook or Yahoo or Google), we would need to gain access by using any constructed URL with parameters. These are known as endpoints.
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: left;">
  So by following the API URL above, let&#8217;s break it apart:
</div>

<div style="clear: both; text-align: left;">
</div>

<blockquote style="clear: both; text-align: left;">
  <p>
    <b><span style="font-size: large;">https://api.foursquare.com/</span></b>
  </p>
</blockquote>

<div style="clear: both; text-align: left;">
  This is where they store their API information. Pretty standard.
</div>

<div style="clear: both; text-align: left;">
</div>

<blockquote style="clear: both; text-align: left;">
  <p>
    <b><span style="font-size: large;">/v2/</span></b>
  </p>
</blockquote>

<div style="clear: both; text-align: left;">
  This is their API version. If they do any huge API update, this needs to be updated to their latest version.
</div>

<div style="clear: both; text-align: left;">
</div>

<blockquote style="clear: both; text-align: left;">
  <p>
    <b><span style="font-size: large;">/venues/search?</span></b>
  </p>
</blockquote>

<div style="clear: both; text-align: left;">
  This is their API function. I&#8217;ll be leveraging their search queries instead of the explore or other API functions. After the search is a question mark (?), which means that starting after this is where we put in our parameters for the kind of information we want to get from their huge database of venues.
</div>

<div style="clear: both; text-align: left;">
</div>

<blockquote style="clear: both; text-align: left;">
  <p>
    <b><span style="font-size: large;">client_id=CLIENT_ID&</span></b>&nbsp;
  </p>
</blockquote>

<blockquote style="clear: both; text-align: left;">
  <p>
    <b><span style="font-size: large;">client_secret=CLIENT_SECRET</span></b>
  </p>
</blockquote>

<div style="clear: both; text-align: left;">
  Before accessing any API of any website, <a href="https://foursquare.com/developers/apps" target="_blank">one must first register a developer&#8217;s account with them</a>. From there, the developer will have access to an API console where he/she can get the system-generated Client ID and Client Secret. This is unique to each developer who wants access to Foursquare&#8217;s API.
</div>

<div style="clear: both; text-align: left;">
</div>

<div style="clear: both; text-align: left;">
  So by getting those information, the developer will have to replace the &#8220;CLIENT_ID&#8221; and &#8220;CLIENT_SECRET&#8221; with their own. It looks something like this:
</div>

_client_id=4FOMOGGWG3M1PFEIAJ3IOY5V2TJ1EKEK12HD0ZNQGSUDHI3D_ 

<div>
</div>

<div>
  And in between those 2, we use an ampersand (&) to string them in the URL. This is what separates parameter values but still be part of the URL.
</div>

<div>
</div>

> **<span style="font-size: large;">v=20130815</span>**

<div>
  According to the docs, this is known as<a href="https://developer.foursquare.com/overview/versioning.html" target="_blank"> versioning</a>. Basically we also need to know when was its last version and to make sure that the data is up to date with the latest API version.
</div>

<div>
</div>

> **<span style="font-size: large;">ll=40.7,-74</span>**

<div>
  Those are double L&#8217;s (ll). Which stands for Latitude and Longitude. Again, according to the docs, this is required for venue searching. We can replace this by grabbing the user&#8217;s location (using HTML5 API) and pass it to this parameter/endpoint.
</div>

<div>
</div>

> **<span style="font-size: large;">query=sushi</span>**

<div>
  Then lastly, we have the user&#8217;s query. This is pretty straightforward that when the user asks to find all locations that has anything to do or about &#8220;sushi&#8221;, it displays them. We can replace this by grabbing the user&#8217;s input and then pass it to this parameter/endpoint.
</div>

<div>
</div>

<div>
  So if I wanted to find all places that has something about &#8220;Ayam Penyet&#8221; or &#8220;Nasi Katok&#8221;, the query would look something like this:
</div>

<div>
  <i>query=ayam%20penyet</i>
</div>

<div>
</div>

<div>
  or
</div>

<div>
</div>

<div>
  <i>query=nasi%20katok</i>
</div>

<div>
</div>

<div>
  The %20 means <i>space</i> in URL, since we can&#8217;t allow spaces in between endpoints or even parameter values. Everything must come together like a big happy family.
</div>

<div>
</div>

## Let&#8217;s Recap

<div>
  <b>https://api.foursquare.com/v2/venues/search?</b>
</div>

<div>
  This is our standard URL. Rarely changes. Only after the question mark that we specify and filter the kind of information we want to get.
</div>

<div>
</div>

<div>
  <b>client_id=CLIENT_ID&client_secret=CLIENT_SECRET</b>
</div>

<div>
  This is required. Rarely changes. Need to have in all URL passing. So add that as a standard.
</div>

<div>
</div>

<div>
  <b>v=20130815&ll=40.7,-74&query=sushi</b>
</div>

<div>
  The v is for versioning and as mentioned, it is a requirement to state when was the latest API version. The ll is the map coordinates in latitude and longitude. Lastly, the query to filter the venues by its description.
</div>

## Our End Result

<div>
  So after putting all this together, what do we get?
</div>

<div style="clear: both; text-align: center;">
  <a href="http://i0.wp.com/blog.qoyyuum.me/wp-content/uploads/2014/07/4sq.png" style="margin-left: 1em; margin-right: 1em;"><img alt="Foursquare's Response after putting it in the URL" border="0" src="http://i0.wp.com/blog.qoyyuum.me/wp-content/uploads/2014/07/4sq.png?resize=640%2C340" title="" data-recalc-dims="1" /></a>
</div>

<div>
  It looks intimidating to anyone who&#8217;s not really familiar in using Javascript arrays or learnt how to use Object Oriented Programming.
</div>

<div>
</div>

## Let&#8217;s Read It!

<div>
  If you aren&#8217;t dizzy yet, let&#8217;s continue by breaking down the resulting page that we have by referring to the docs (again).
</div>

<div>
</div>

<div>
  Here is a small excerpt of the result that I keyed in the URL:
</div>

<div>
</div>

<div>
  {&#8220;<span style="background-color: cyan;">id</span>&#8220;:&#8221;503fb602ebca66a84f0287e8&#8221;,
</div>

<div>
  &#8220;<span style="background-color: cyan;">name</span>&#8220;:&#8221;Mighty Quinn&#8217;s BBQ&#8221;,
</div>

<div>
  &#8220;<span style="background-color: cyan;">contact</span>&#8220;:{&#8220;phone&#8221;:&#8221;2126773733&#8243;,&#8221;formattedPhone&#8221;:&#8221;(212) 677-3733&#8243;,&#8221;twitter&#8221;:&#8221;mightyquinnsbbq&#8221;},
</div>

<div>
  &#8220;<span style="background-color: cyan;">location</span>&#8220;:{&#8220;address&#8221;:&#8221;103 2nd Ave&#8221;,&#8221;crossStreet&#8221;:&#8221;at E 6th St&#8221;,&#8221;lat&#8221;:40.7275189451569,&#8221;lng&#8221;:-73.98867130279541,&#8221;distance&#8221;:3209,&#8221;postalCode&#8221;:&#8221;10003&#8243;,&#8221;cc&#8221;:&#8221;US&#8221;,&#8221;city&#8221;:&#8221;New York&#8221;,&#8221;state&#8221;:&#8221;NY&#8221;,&#8221;country&#8221;:&#8221;United States&#8221;,&#8221;formattedAddress&#8221;:[&#8220;103 2nd Ave (at E 6th St)&#8221;,&#8221;New York, NY 10003&#8243;,&#8221;United States&#8221;]},
</div>

<div>
</div>

<div>
  Take note of the highlighted words in <span style="background-color: cyan;">light blue</span> above. These are the field names and the information that goes along with it. Now, let&#8217;s look at the docs about this venue response.
</div>

<div>
</div>

## Venue Response

<div>
</div>

<div style="clear: both; text-align: center;">
  <a href="http://i0.wp.com/blog.qoyyuum.me/wp-content/uploads/2014/07/4sq-response.png" style="clear: left; float: left; margin-bottom: 1em; margin-right: 1em;"><img alt="Venue Response Docs by Foursquare" border="0" src="http://i0.wp.com/blog.qoyyuum.me/wp-content/uploads/2014/07/4sq-response.png?resize=640%2C456" title="" data-recalc-dims="1" /></a>
</div>

<div>
  Matching to the docs, we can identify what these are.
</div>

<div>
</div>

### id

<div>
  The id is a string identifier. This is where Foursquare keeps the venues unique in their database.
</div>

<div>
</div>

### name

<div>
  The merchant or the user who checked in or made this venue on foursquare gave it this name.
</div>

<div>
</div>

### contact

<div>
  All the contact information stored in one object. Self-explanatory, I hope.
</div>

<div>
</div>

### location

<div>
  This is where we get more than just the address. We also get the latitude, longitude and distance between the venue and the user&#8217;s geolocation.
</div>

<div>
</div>

### And more

<div>
  There&#8217;s more to it per venue stored in by Foursquare. All a developer needs to do is study it.
</div>

<div>
</div>

## Conclusion

<div>
  So now that we have the result, we just need to display them properly. Pretty straightforward but that&#8217;s just me using Foursquare&#8217;s API. There were also complaints that there are some APIs don&#8217;t exactly work the same, simply due to either a technical error or that the technical documentation wasn&#8217;t clear enough on how to use these endpoints.
</div>

<div>
</div>

<div>
  Have a read through at any API docs or look at the API doc that I was referring to here:<br /><a href="https://developer.foursquare.com/docs/venues/search">https://developer.foursquare.com/docs/venues/search</a>
</div>

<div>
</div>

## Happy App Building!