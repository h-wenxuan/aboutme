---
title: "Quiz App"
excerpt: "Created a fun quiz app with Andriod Studio <br/><img src='/aboutme/images/mainpic.png' style='width:300px; height:auto;'>"
collection: portfolio
---

My friend and I developed a quiz app using the knowledge we gained from our previous project, leveraging the Tomcat Apache server for backend management and SQL for database operations. To bring our app to life, we used [Android Studio](https://www3.ntu.edu.sg/home/ehchua/Programming/android/Android_HowTo.html), which provided a robust environment for directly writing and testing our code, bypassing the need for VS Code.

Our database tables include:
1. User Table: This table records the names of all students who have attempted the quiz.
2. Response Table: This table logs each student's responses, allowing us to compile the data into a graphical format that can be displayed within the app
![Databasetable]({{ site.baseurl }}/images/tables.png)

**Backend Java Codes**

All backend logic is housed within the com.example.myquestiongame package under the Java folder of the app. A typical activity setup includes the super.onCreate(savedInstanceState) method, ensuring that each activity initializes correctly. The setContentView(R.layout.activity_main) method is then used to bind the activity to its respective XML layout file, stored in the res/layout folder. The XML files define the user interface components and layout.
![basicode]({{ site.baseurl }}/images/basiccode.png)

**Login Page**

The login page is designed to prevent multiple logins from the same user, ensuring data integrity. In MainActivity.java, the setOnClickListener() method is used to handle button clicks, connecting to the Tomcat server via the URL: "http://10.0.2.2:9999/clicker/storename?name=" after the button 'Let's Go!' is pressed. Futhermore, in the code, the 'sendRequest()' method is responsible for sending HTTP requests to the server. Upon receiving a response, 'handleResponse()' then processes the data and updates the UI or navigates to the next screen. To enhance user experience, we also integrated background music that plays during app usage.
![userlogin]({{ site.baseurl }}/images/sameuser.png)

**Question Pages**

The quiz questions are managed in 'FirstQuestion.java', where four buttons are provided, each linked to a specific URL that loads when clicked. This setup allows for seamless interaction between the user and the server as answers are submitted.

**Graph Pages**

After a user submits their answer, their response is recorded in the database. This data is then compiled into a graph, which is displayed on the subsequent screen via FirstGraph.java. If a user answers correctly, their score is updated and visible within the app.
![graph]({{ site.baseurl }}/images/graph.png)

**End of Quiz**

After the quiz has ended, the app tallies the student’s score, displaying it before returning them to the main page. 
![fullapp]({{ site.baseurl }}/images/fullapp.png)

**Future Improvements**

To further enhance the app, we’ve identified a few areas for improvement:
1. UI Enhancements: Instead of displaying the question answers above the buttons, we could place them directly on the buttons themselves. Additionally, incorporating more images would make the user interface more engaging and visually appealing.
2. Security Improvements: Introducing a PIN system would restrict access to the quiz, ensuring that only students with the correct PIN can participate. This feature would enhance the security and integrity of the quiz.
