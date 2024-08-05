---
title: "Game E-shop"
excerpt: "Created a gaming e-shop with both frontend and backend features <br/><img src='/aboutme/images/gameshoppic.png' style='width:300px; height:auto;'>"
collection: portfolio
---

My friend and I developed an online game purchasing website using Apache Tomcat, SQL, Java, HTML, and CSS. The project involved setting up databases, creating server-side functionality with Java, and designing a user-friendly interface with HTML and CSS.

**Creating our databases**

We utilised this [guide](https://www3.ntu.edu.sg/home/ehchua/Programming/sql/MySQL_HowTo.html) to launch our database server and establish three essential tables: 
1. Games Table: Stores details of all games available for sale, including game titles, developer, prices, and available stock.
2. Member Login Table: Maintains login information for all members, storing usernames, passwords, and other relevant details to manage user authentication and authorization.
3. Purchases Table: Records customer purchases, including customer details, purchased game titles, quantities, and customer contact information.
![Database]({{ site.baseurl }}/images/databases.png)

**Java Servlet Programming**

We continued our server-side development by downloading and configuring [Apache Tomcat](https://www3.ntu.edu.sg/home/ehchua/Programming/howto/Tomcat_HowTo.html). After familiarising ourselves with VS Code, we wrote Java Servlets to handle various functionalities of our website. [View our code here.](https://github.com/h-wenxuan/gaming-eshop/tree/master)

**Homepage**

The homepage serves as the main navigation hub for users. It is implemented with a simple design, allowing users to access [homequerymv.html file](https://github.com/h-wenxuan/gaming-eshop/blob/master/homequerymv.html), where we use addEventListener to manage button interactions. 
![Nextpage]({{ site.baseurl }}/images/nextpage.png)
This file is pivotal in ensuring users can easily navigate to different sections of the website. Additionally, we added background music to enhance the user experience. On the homepage, users will find three primary buttons:
1. Menu: Directs users to the e-shop where they can browse and purchase games.
2. Member Login/Register: Allows users to log in or sign up for membership.
3. About Us: Provides information about our website and the team behind it.
![Homepage]({{ site.baseurl }}/images/homepage.png)

**Membership Login/Register**

Our login page is designed for simplicity and ease of use. New users are required to register, providing their username and password, which are validated against our userpass table. This registration process enables us to send personalized promotions and news to our members. If users enter incorrect login details, they receive an error message. We also ensure email and phone number inputs are valid. Upon successful login, users can view and verify their information. The code for these functionalities is in [LoginServlet.java](https://github.com/h-wenxuan/gaming-eshop/blob/master/WEB-INF/classes/LoginServlet.java) and [SignUpServlet.java.](https://github.com/h-wenxuan/gaming-eshop/blob/master/WEB-INF/classes/SignUpServlet.java)
![Login]({{ site.baseurl }}/images/loginall.png)

**Game E-shop**
The game e-shop is the core feature of our website. Users can browse available games, and upon selecting a game, they are redirected to a checkout page. Here, they provide their name, email, and phone number, which helps us track orders. Once an order is submitted, it is reflected in our 'order' table, and the available stock of the purchased game is automatically updated. The code managing these processes can be found in [QueryServlet.java](https://github.com/h-wenxuan/gaming-eshop/blob/master/WEB-INF/classes/QueryServlet.java) and [ConfirmServlet.java.](https://github.com/h-wenxuan/gaming-eshop/blob/master/WEB-INF/classes/ConfirmServlet.java)
![purchase]({{ site.baseurl }}/images/checkout.png)

**Future Improvements**

To enhance our gaming e-shop, we have identified several areas for improvement:
1. Security: It would be better to implement password hashing to protect user credentials, making the system more secure against potential attacks.
2. User Experience: It would be better to streamline navigation between pages and enhance the overall usability of the website, ensuring a smoother and more enjoyable shopping experience.
3. Feature Enhancements: We can considering adding more features, such as personalized game recommendations, a more dynamic user dashboard, and enhanced search and filter options for easier game discovery.
