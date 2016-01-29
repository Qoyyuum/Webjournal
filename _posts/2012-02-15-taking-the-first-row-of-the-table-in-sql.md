---
id: 141
title: Taking the first row of the table in SQL
date: 2012-02-15T14:11:00+00:00
author: Qoyyuum
layout: post
guid: http://blog.qoyyuum.me/?p=141
permalink: /taking-the-first-row-of-the-table-in-sql/
blogger_blog:
  - qoyyuum.blogspot.com
blogger_author:
  - Abdul Qoyyuum Haji Abdul Kadir
blogger_permalink:
  - /2012/02/taking-first-row-of-table-in-sql.html
blogger_internal:
  - /feeds/1705353048896399216/posts/default/4225331055425020425
tags:
  - coding
  - xampp
---
My challenge for today was to take the first row of the database table and display it.

Here&#8217;s an example:

Customer Database in MYSQL and we&#8217;ll call this table : **CUSTOMER_MAST**

<table border="1" cellpadding="0" cellspacing="0">
  <tr>
    <th>
      Id
    </th>
    
    <th>
      Name
    </th>
    
    <th>
      Phone Number
    </th>
    
    <th>
      Address
    </th>
    
    <th>
      Date Registered
    </th>
  </tr>
  
  <tr>
    <td>
      1
    </td>
    
    <td>
      Abdul Qoyyuum
    </td>
    
    <td>
      +6738123456
    </td>
    
    <td>
      No. 9, Spg. 778, Jalan mata-mata
    </td>
    
    <td>
      2001-09-10 00:00:00
    </td>
  </tr>
  
  <tr>
    <td>
      2
    </td>
    
    <td>
      Noor Asrinah
    </td>
    
    <td>
      +6737891012
    </td>
    
    <td>
      No. 5, Spg. 81-72-23, Jalan Gadong
    </td>
    
    <td>
      2001-09-10 00:00:00
    </td>
  </tr>
  
  <tr>
    <td>
      3
    </td>
    
    <td>
      Abdul Aziz
    </td>
    
    <td>
      +6738877661
    </td>
    
    <td>
      No. 20A, Spg. 104-24, Jalan 60
    </td>
    
    <td>
      2001-09-10 00:00:00
    </td>
  </tr>
</table>

So what I want was to only display the first row. I don&#8217;t want to display the other two out but I wasn&#8217;t able to figure out how until I googled how to and here&#8217;s the solution:

`Select Name, Phone_Number, Address from (Select *, Rownumber() over (order by Id) a from CUSTOMER_MAST) where Id = 1`

_My work here is done&#8230;_