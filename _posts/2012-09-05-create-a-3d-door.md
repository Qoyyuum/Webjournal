---
id: 52
title: Create a 3D Door
date: 2012-09-05T08:34:00+00:00
author: Qoyyuum
layout: post
guid: http://blog.qoyyuum.me/?p=52
permalink: /create-a-3d-door/
blogger_blog:
  - qoyyuum.blogspot.com
blogger_author:
  - Abdul Qoyyuum Haji Abdul Kadir
blogger_permalink:
  - /2012/09/create-3d-door.html
blogger_internal:
  - /feeds/1705353048896399216/posts/default/8209486576678545969
categories:
  - Uncategorized
tags:
  - 3D modeling
  - Blender
  - Games
  - project
  - prototype
---
<div style="clear: both; text-align: center;">
  <a href="http://i2.wp.com/blog.qoyyuum.me/wp-content/uploads/2012/09/a-door-able-in-3D-by-Qoyyuum.png" style="margin-left: 1em; margin-right: 1em;"><img alt="Lame pun or awesome? Made this door in Blender, an open-source 3D maker to model and create 3D objects. Later will be used as Assets in Unity 3D platform." border="0" src="http://i2.wp.com/blog.qoyyuum.me/wp-content/uploads/2012/09/a-door-able-in-3D-by-Qoyyuum.png?resize=640%2C330" title="" data-recalc-dims="1" /></a>
</div>

Guess what I made recently? A 3D Door in blender. Not really a big fan in making these things but since <a href="http://maps.google.com/maps?ll=4.89028333333,114.942216667&spn=10.0,10.0&q=4.89028333333,114.942216667%20(Brunei)&t=h" rel="geolocation nofollow" target="_blank" title="Brunei">Brunei</a> doesn&#8217;t really have a <a href="http://www.break.com/c/pop-culture-videos/video-games/" rel="break nofollow" target="_blank" title="Video Games">video game</a> company or group, might as well try a simple <a href="http://en.wikipedia.org/wiki/Platform_game" rel="wikipedia nofollow" target="_blank" title="Platform game">3D platformer</a> game.

Made the 3D door with 2 mesh objects. A cube and a cylinder.

## The Door

Enter Edit mode and select the cube. Press &#8220;/&#8221; on the numpad to focus. Select the top 4 vertices and drag &#8217;em upwards. Deselect all and select the front face of the cube and move inward, making the door looking thin. Door is done.

## The Door Handle

<div>
  Enter Edit mode and select the cylinder. Press &#8220;/&#8221; on the numpad to focus. Deselect and select the top face of the cylinder. Drag &#8217;em upwards.&nbsp;This part is the hard one. Press &#8220;E&#8221; to extrude the top part a little bit. While the top part is selected, drag it towards the y-axis or x-axis. Rotate to make the selected face parallel to the body. Deselect and select the top part of the door handle bar (from the extruded area to the edge). This part is the easy one. Press &#8220;SHIFT + D&#8221; to duplicate. Drag it to the bottom part of the cylinder. Rotate on x- or y-axis. Drag to fit.
</div>

<div>
</div>

<div>
  What I should have done:
</div>

<div>
  <ul>
    <li>
      Select the bottom face of the duplicated object;
    </li>
    <li>
      Press &#8220;SHIFT + S&#8221; for snapping options.
    </li>
    <li>
      Select &#8220;Cursor to Selected&#8221;
    </li>
    <li>
      Switch to Object Mode by Tabbing
    </li>
    <li>
      Press &#8220;SHIFT + CTRL + ALT + C&#8221; to set &#8220;Origin to 3D cursor&#8221;.
    </li>
    <li>
      At the cylinder, press &#8220;N&#8221;
    </li>
    <li>
      Under Mesh Display > Dimensions, Select Face and make sure it faces outwards. Otherwise, press &#8220;W&#8221; for Specials. Select &#8220;Flip Normal&#8221;.
    </li>
    <li>
      Drag the duplicated model to the bottom cylinder and it will snap into place.
    </li>
  </ul>
  
  <div>
    And that&#8217;s it. This is just one asset to be used in Unity 3D platform. Now I got a few other 3D models to create.
  </div>
</div>

<div>
</div>

<div style="margin-top: 20px; overflow: hidden;">
  <h4>
    Related articles
  </h4>
  
  <ul style="margin: 0; overflow: hidden; padding: 0;">
    <li style="background: none; display: block; float: left; font-size: 11px; list-style: none; margin: 2px 10px 10px 2px; padding: 0; text-align: left; vertical-align: top; width: 84px;">
      <a href="http://dreamsgate.wordpress.com/2012/08/22/book-review-blender-3d-basics-by-gordon-c-fisher/" rel="nofollow" style="border-radius: 2px; box-shadow: 0px 0px 4px #999; display: block; padding: 2px; text-decoration: none;" target="_blank"><img src="http://i1.wp.com/blog.qoyyuum.me/wp-content/uploads/2012/09/108223574_80_80.jpg?w=676" style="border: 0; display: block; margin: 0; max-width: 100%; padding: 0; width: 80px;" data-recalc-dims="1" /></a><a href="http://dreamsgate.wordpress.com/2012/08/22/book-review-blender-3d-basics-by-gordon-c-fisher/" rel="nofollow" style="display: block; height: 80px; line-height: 12pt; overflow: hidden; padding: 5px 2px 0 2px; text-decoration: none;" target="_blank">Book Review: Blender 3d Basics by Gordon C. Fisher</a>
    </li>
    <li style="background: none; display: block; float: left; font-size: 11px; list-style: none; margin: 2px 10px 10px 2px; padding: 0; text-align: left; vertical-align: top; width: 84px;">
      <a href="http://www.omgubuntu.co.uk/2012/08/blender-and-ubuntu-creating-tv-advert-magic-in-brazil" rel="nofollow" style="border-radius: 2px; box-shadow: 0px 0px 4px #999; display: block; padding: 2px; text-decoration: none;" target="_blank"><img src="http://i1.wp.com/blog.qoyyuum.me/wp-content/uploads/2012/09/noimg_7_80_80.jpg?w=676" style="border: 0; display: block; margin: 0; max-width: 100%; padding: 0; width: 80px;" data-recalc-dims="1" /></a><a href="http://www.omgubuntu.co.uk/2012/08/blender-and-ubuntu-creating-tv-advert-magic-in-brazil" rel="nofollow" style="display: block; height: 80px; line-height: 12pt; overflow: hidden; padding: 5px 2px 0 2px; text-decoration: none;" target="_blank">Blender and Ubuntu Creating TV Ad Magic in Brazil</a>
    </li>
    <li style="background: none; display: block; float: left; font-size: 11px; list-style: none; margin: 2px 10px 10px 2px; padding: 0; text-align: left; vertical-align: top; width: 84px;">
      <a href="http://dreamsgate.wordpress.com/2012/08/01/blender-3d-basics-by-gordon-c-fisher/" rel="nofollow" style="border-radius: 2px; box-shadow: 0px 0px 4px #999; display: block; padding: 2px; text-decoration: none;" target="_blank"><img src="http://i2.wp.com/blog.qoyyuum.me/wp-content/uploads/2012/09/103963267_80_80.jpg?w=676" style="border: 0; display: block; margin: 0; max-width: 100%; padding: 0; width: 80px;" data-recalc-dims="1" /></a><a href="http://dreamsgate.wordpress.com/2012/08/01/blender-3d-basics-by-gordon-c-fisher/" rel="nofollow" style="display: block; height: 80px; line-height: 12pt; overflow: hidden; padding: 5px 2px 0 2px; text-decoration: none;" target="_blank">Blender 3D Basics by Gordon C. Fisher</a>
    </li>
    <li style="background: none; display: block; float: left; font-size: 11px; list-style: none; margin: 2px 10px 10px 2px; padding: 0; text-align: left; vertical-align: top; width: 84px;">
      <img src="http://i1.wp.com/blog.qoyyuum.me/wp-content/uploads/2012/09/109004531_80_80.jpg?w=676" style="border: 0; display: block; margin: 0; max-width: 100%; padding: 0; width: 80px;" data-recalc-dims="1" />Beginning Blender: Open Source 3D Modeling, Animation, and Game Design
    </li>
  </ul>
</div>

<div style="height: 15px; margin-top: 10px;">
  <a href="http://www.zemanta.com/?px" title="Enhanced by Zemanta"><img alt="Enhanced by Zemanta" class="zemanta-pixie-img" src="http://i1.wp.com/blog.qoyyuum.me/wp-content/uploads/2012/10/zemified_h.png?w=676" style="border: none; float: right;" data-recalc-dims="1" /></a>
</div>