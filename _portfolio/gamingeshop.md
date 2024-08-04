---
title: "Game E-shop"
excerpt: "Created a gaming e-shop with both frontend and backend features <br/><img src='/aboutme/images/gameshoppic.png' style='width:300px; height:auto;'>"
collection: portfolio
---

For this project, my friend and I utilised Apache Tomcat to create and store database with tables in SQL language needed for our online game purchasing website. For server-side functionality, we used Java code and for client-side interfaces, we went with HTML and CSS code to build a functional and visually appealing website.

**Creating our databases**

Refering to this [website](https://www3.ntu.edu.sg/home/ehchua/Programming/sql/MySQL_HowTo.html), we launched our database server and created databases with 3 tables. One for storing all the different games we have on sale, one for recording the items that customers buy and another for keeping track of all our customer's login information. 
![Database]({{ site.baseurl }}/images/cleandataset.png)

**Java Servlet Programming**

Next, we got started on Java Servlet programming by downloading [Apache Tomcat](https://www3.ntu.edu.sg/home/ehchua/Programming/howto/Tomcat_HowTo.html). After configuring the Tomcat Server, we started writing Java Servlets in VS Code. [View our code here.](https://github.com/h-wenxuan/gaming-eshop/tree/master)
With a website, we definitely needed a homepage and we decided to go for something simple. In our GameHomeMultiValueServlet.java code, we can see that we are directing the users to /homequerymv.html where we have created our html file. In this html file, we have formatted the buttons to bring users to the next location with addEventListener as seen in homequerymv.html file. 
![Homepage]({{ site.baseurl }}/images/cleandataset.png)
