# Studemy

## youtube vedio: https://www.youtube.com/watch?v=lerm1ku58AA&feature=youtu.be

## Introduction
### Purpose
Everyone experiences difficulties studying at one time or another, and overcoming these challenges is part of the learning process, particularly when there is a large workload. There are many ways to solve these difficulties, either by searching on the web or YouTube videos, but sometimes these methods do not work. Which makes the person who faces this problem resort to the way of talking with an expert in this field, which will cost him some money, and from here I started thinking about creating a project that allows all people to ask any question or any problem they face in any field, and they will be answered by some of the people that have this problem before, so that this project is available to everyone for free without any fees.
### Explaining the project:
Sudemy is a website that allows people to ask questions about any topic they have a bug, in which the user can ask other users about the problem he faces by sharing a post on the feed page where the users can see this post and answer his question, also studemy offers chatting rooms, which is very useful, which is helpful for a group project that users can make with their friends or with other users, the user can also interact with posts and book mark the post and also can delete it. I made more than one function to handle errors that may be made by the user while using this website.

## Distinctiveness and Complexity
I believe my project satisfies the criteria of distinctiveness and complexity because this project is to help everyone solve their studying problems. Anyone can use it for free. Some sites offer anyone to ask questions about any topic, but they don't have the feature of creating a room for any topic, but my project have.I faced many problems in creating this project, including the fact that I was studying at the university and based on my own creation of this project. I also encountered problems in coordinating the database and some problems related to programming that had been solved with seriousness and diligence..


#### Technologies:
* django as python back-end framework that helped me alot in developing this project To make it become the final form it is now.
* HTML, CSS, and JavaScript languages were used to design the front-end section of the project.
* Bootstrap and Fontawesome libraries were used to design the front-end section of the project.


## Files

* project: the main directory for the app

    * project/templates: contains all the application pages
    * project/templates/main :
        * project/templates/main/index.html: contains the html of the first page, which contains the website info and its features, and more info about the features. I made this page responsive with desktop, tablet, and mobile by css media queries; I also used javascript to switch between signin and sign up; I also used Font Awesome icons to add some pictures; and I used the backend to make the user able to login to the site.

        * project/templates/main/main.html: contains the html and the javascript of the second page, which is the page on which the user can see all the questions that have been asked by the other students and the rooms that have been made by the students registered on the website. In this page, I used javascript to switch between the posts and rooms divs by the received value of type (which is by default "posts").

            * search section: this section is simply used to search for rooms or posts by the users' names.

            * Posts section: this section shows the questions of the users and also contains a section in which the user can ask a question by writing the question in the text area and then post.

            * rooms section: in this section you can see the rooms that were made by the users. Also, by clicking on the button "create room" at the top of this div, a div will be shown that asks you to type the name, the room topic, and a small description about the room. Another feature is that you can join any room you want and send a message about the room topic (I made this by using the JavaScript API fetch).

    * project/views.py: contains all the functions that are used in the website.

        * validate_password: validate that the first password is equal to the second password.

        * index: process the login requests that come from the user by taking the username either from the username field in the first form or the second (I made two forms, one for desktop view and the second one for mobile view).

        * main: processes all the activities that come from the main page (searching, loading the posts and rooms divs, posting messages to the rooms, handling the paginator in the rooms div).

    * project/urls.py: contains all application's URLs

* static: contains all the CSS files for the project and also the javascript

    * static/page1.js: contains the javascript for the first page.

    * static/page1.css: contains the CSS of the first page.
    * static/page2.css: contains the CSS of the second page, which is the main page.
    * static/imgs :
        * static/imgs/background.jpg: the image used


## Models
I used 5 Models:
1. User: I did not edit anything in the user model.
1. Post: model for posts
1. Room: model for rooms
1. Topic: model for the room topics
1. Comment: model for commenting
1. Interactions: models for the reacting with the posts
1. Chat: model for the room chats

## Installation

1. Create virtual env and install requirements

``` bash
    py -m venv env

    pip install -r requirements.txt
```

1. Make and apply the migrations by running

``` bash
        Python manage.py makemigrations

        Python manage.py migrate
```
1. Create a superuser.
``` bash
       Python manage.py  createsuperuser
```
1. Run the server.

``` bash
        Python manage.py runserver
```
1. create account, and then you will be taken to the main page.

1. On the top of the main page, there is a navbar that contains three tabs:
    * Rooms: shows the div that contains the Rooms div, which contains the room posts, which contain:
    * A box that contains a button to create a new room When you click on this button, a form will appear asking you for room name, the description of the room, and the topic you want to talk about, and when you create the room you will be redirected to this room's chatting box and this room will be added to your joined rooms.

    * Feeds: will show the question, and you can also search for any question you want, and interact with the post, also you can comment on this post, you can save it and delete it.

    * Contact us : will show a page where the user can send a message telling his experience with the site

1. Finally, the logout icon will make you logout.
