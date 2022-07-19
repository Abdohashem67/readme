# Final Project

## Requirements

The final project is your opportunity to design and implement a dynamic website of your own. So long as your final project draws upon this course’s lessons, the nature of your website will be entirely up to you, albeit subject to the staff’s approval.

In this project, you are asked to build a web application of your own. The nature of the application is up to you, subject to a few requirements:

Your web application must utilize at least two of Python, JavaScript, and SQL.
Your web application must be mobile-responsive.
In README.md, include a short writeup describing your project, what’s contained in each file you created or modified, and (optionally) any other additional information the staff should know about your project.
If you’ve added any Python packages that need to be installed in order to run your web application, be sure to add them to requirements.txt!
Beyond these requirements, the design, look, and feel of the website are up to you!

## Distinctiveness and Complexity

My final project is a website called studemy which allows people asks a questions about somethimg they have a bug with this may be done in other websites but my website also have the feature to make chatting rooms and talk about speciefic topic,this project made by using django as a backend framework and JavaScript and HTML and CSS as a frontend programming languages also bootstrap nad fontawesome as frontend library. all of the inforamtion are stored in a database (SQLite by default).

my website is mobile responsive.

## Documentation

In this project i used all the techniques we had learnt in this course

### How to use ths project:

* Firstlty, create an account then you  will be redicted to the main page

* On the top of the main page there is a navbar contains 3 tabs :
    * Rooms : will hide the div is appearing to you by javascript (this is inthe code) and will show the div which contains the Rooms div which contains the room posts which contains :
        * A box which contains a button to Create a new room when you click on this button a form will appear to you asking you for the name of the room and the description of the room and also the topic which you want to talk about

    * Feeds : will show the question and also you can search for any question you want

    * Finally the logout icon which will make you logout




## Files

*  project : the main directory for the app

    * project/templates : contains all the appication pages
        * project/templates/main :
            * project/templates/main/index.html : contains the html of the first page which contains the website info and its features and more info about the features, I made this page responsive with desktop and tablet and mobile by css media query also i used javascript to switch between signin and sign up, also i used fontawesome icons to add some pics, lastely i used backend to make the user able to login to the site.

            * project/templates/main/main.html : contains the html and the javascript of the second page which is the page which the user can see all the questions which asked by the other students also the rooms which had been made by the students registered in the website , inthis page i used javascript to switch between the posts and rooms divs by the recieved value of type (which is by default "posts")

                * search section : this section simply used to search about the rooms /posts by the users's name.

                * posts section : this section shows the questions of the users also it contains a section which the user can ask a question by writing the question in the text area and then clicking post

                * rooms section : in this section you can see the rooms that made by the users also by clicking on the button "create room" at the top of this div a div will be shown which asks you to type the  name and the room topic and small description about the room, another feature that you can join any room you want and send a message about the room topic (i made this by using javascipt api fetch).


    * project/views.py : contains all the functions which used in the website

        * CustomSerializer : i used this class to custemize the Serializer to be able to serialize the forgien key with the speciefic field

        * validate_password : validate that the first password is equal to the second password

        * index : procces the login attempets that comes from the user by taking the username either from username field in the first form or the second (i made two forms one for desktop view and the second one is for the mobile view)

        * main : procces all the activities that comes from the main page (searching, loads the posts and rooms divs, posts messages to the rooms ,handels the paginator in the rooms div)

    * project/models.py : contains the 5 models which i used in this used

        * User : I didnot edit anything in the User model

        * Post : model for posts
        * Room : model for rooms
        * Topic : model for the room topics
        * Chat :  model for the room chats

    * project/urls.py : contains all appication Urls

* static : contains all the css files for the project and also the
javascript

    * static/page1.js : contains the javascript for the first page.

    * static/page1.css : contains the css of the first page
    * static/page2.css : contains the css of the second page which is the main page
    * static/imgs :
        * static/imgs/background.jpg : the image which used in the page1 as a background

## Installation

1. Cake and apply the migrations by running

    ``` bash
    python manage.py makemigrations

    python manage.py migrate
    ```
1. Create a superuser

    ```bash
    python manage.py createsuperuser
    ```
1. Run the server

    ```bash
    python manage.py runserver
    ```
1. Finally, goto the website and register

## Additional info

I used javascript inside the html file to benfit from the django tags
