---
title: "Game E-shop"
excerpt: "Created a gaming e-shop with both frontend and backend features <br/><img src='/aboutme/images/gameshoppic.png' style='width:300px; height:auto;'>"
collection: portfolio
---

For this project, my friend and I utilised Apache Tomcat to create and store database with tables in SQL language needed for our online game purchasing website. For server-side functionality, we used Java code and for client-side interfaces, we went with HTML and CSS code to build a functional and visually appealing website.

**Creating our databases**

Refering to this [website](https://www3.ntu.edu.sg/home/ehchua/Programming/sql/MySQL_HowTo.html), we launched our database server and created databases with 3 tables. One for storing all the different games we have on sale, one for recording the items that customers buy and another for keeping track of all our customer's login information. 
![Database]({{ site.baseurl }}/images/databases.png)

**Java Servlet Programming**

Next, we got started on Java Servlet programming by downloading [Apache Tomcat](https://www3.ntu.edu.sg/home/ehchua/Programming/howto/Tomcat_HowTo.html). After configuring the Tomcat Server, we started writing Java Servlets in VS Code. [View our code here.](https://github.com/h-wenxuan/gaming-eshop/tree/master)
With a website, we definitely needed a homepage and we decided to go for something simple. In our GameHomeMultiValueServlet.java code, we can see that we are directing the users to /homequerymv.html where we have created our html file for our home page. In this html file, we have formatted the buttons to bring users to the next location with addEventListener as seen in homequerymv.html file. 
![Nextpage]({{ site.baseurl }}/images/nextpage.png)

On our home page, we have 3 buttons. One for bringing users into the game eshop to purchase the games and another for members to login or create a membership. There is also a about us page and we also added music for fun.
![Homepage]({{ site.baseurl }}/images/homepage.png)

With our membership login page, we kept it simple. If the user has not signed up yet, they are required to sign up and the username and password is check with our userpass table to ensure that we keep track of who are the members. This makes it easier for us to sent them promotions or news regarding our eshop. Furthermore, if memebers key in wrong password or username, they will be prompted with a error message and there will also be warnings for incomplete email and phone number. After they have successfully logged in, there will be a page to show their information for them to check. This code can be seen in the LoginServlet.java. 
![Login]({{ site.baseurl }}/images/loginall.png)

Moving on to our most important feature, the gameing eshop, 

In terms of improving our gaming e-shop, the security of our username and password definitely need to be improved as they was no hashing of password involved, making it vulnerable to attackers. Furtheremore, we could also improve on some of our features, and making it more seamless navigating between pages. 
