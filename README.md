# PIANLY

![logo](./)

# Introduction

## The Project
Almost everyone wants to learn a new musical instrument and improve on their technical abilities. There are certain challenges that comes with this;
- The difficulty to find what to to learn.
- The search for a tutor and mentor
- The ability to stay consistent.
- This is why we created **PIANLY** to ease your learning of musical instruments.

[**PIANLY**](https://pianly.com/) is a site for learning instruments! Tutors can create a profile and start swiping through for instrument they are experts in. If you want to learn an instrument, they can "like" their profile, and schedule a confortable time to learn that instrument.

Other features include: editing the instrument's profile, time schedule for learning , and a "ratings" button to see the rankings of tutors.

## The Context
This project is our Portfolio Project, concluding our Foundations Year at Holberton School . We were able to choose who we wanted to work with and what we wanted to work on, as long as we present a working program at the end of the three weeks of development.

# Tutorial

## Take a tour of the deployed version at pianly
-> [**Pianly**](https://pianly.com/)

Here is a little preview of our main feature, the search for a tutor section:

![swiping](./public/icons/browse_no_text.png)

Here is a simple flow for the user experience on Pianly:

![user-flow](https://i.imgur.com/hRxU79B.jpg)

## Run Pianly with Vue-CLI
Installing the programs necessary to view this project is pretty simple!

We'll be using [`npm`](https://www.npmjs.com/get-npm) to install Vue and Vue-CLI. First clone this repo, then navigate to the root and [install Vue](https://vuejs.org/v2/guide/installation.html) by executing this command:
`pianly$ npm install vue`

Once that has finished, [install Vue-CLI](https://cli.vuejs.org/guide/installation.html) with this command:
`pianly$ npm install -g @vue/cli`

In case there are any missing dependencies, please execute `pianly$ npm install` to get them. If there's an error, it should return the specific command you need to enter.

Once this is all done you're ready to run **Pianly**! Still in the root of this directory, simply execute `pianly$ npm run serve` and give it a few seconds to get started. Once it's up, you can open your web browser and enter `localhost:8080`. This will allow you to try out **PuppR**!

When you are finished simply go back to your terminal and hit `ctrl + c` to quit the program.

## Known bugs
* Some transitions are not as fluid as expected, and due to API calls lag can be a bit off.
* Issue when viewing on mobile. Many of the assets become squished vertically.

# Architecture

## Overview
Our web app is a single-page app, with navigations coded mainly in JavaScript and Vue. **Pianly** is front-end heavy, meaning that we focused our time and energy in developing a simple but easy to use and fun app. We designed most of the User Interface, using plain CSS and some native Vue transitions and animations. We also incorporated some BootstrapVue elements which offered a simple solution for some features like image uploading.

![infra](https://i.imgur.com/fSbo6ho.jpg)

## Vue.js
For this project, we decided to focus on learning a new front-end framework. Following the advice of mentors and professionals, we chose to learn and use Vue.js.

Every different section of the app is a Vue component, and all the components can be found in the directory [src/components/](./src/components/). The main component "App" is defined in [App.vue](./src/App.vue), and is the entry point of the app.

All the components are linked together thanks to a VueRouter instance, defined in [index.js](./routes/index.js). Each component is linked to a route, which path is appended automatically at the end of our URL.

The [main.js](./src/main.js) file contains the instanciation of the Vue for the entire app, as well as the config options, database session and authentication session.

Another interesting point about Vue.js is that it allowed us to use a store, defined in [store.js](./src/store.js). This store is a front-end store that keep strack of the state of components and data throughout the app. This is were the data from our database requests is stored and updated before going back in the database. This store also allows to not pass props from each component to all its children components, and to access data from anywhere without having to use and event bus.

### List of components

These components make up what a user experiences when they check out **PuppR**. Each component contains the code for a specific page of the app. These components can be located in [src/components](./src/components).

| Component | Description |
|-----------|-------------|
| [Landing.vue](./src/components/Landing.vue) | The landing page a user sees when they navigate to **Pianly**. |
| [Login.vue](./src/components/Login.vue)   | The login page. There's a link to go to the Signup page if a user hasn't signed up. |
| [Matches.vue](./src/components/Matches.vue) | Page where users can see the other users they've matched with. A match occurs when two users have liked each other. |
| [Navbar.vue](./src/components/Navbar.vue) | The navigation bar that appears at the top of most every other component |
| [Settings.vue](./src/components/Settings.vue) | Users can change their email address, display name, city, and zip code on this page. |
| [Signup.vue](./src/components/Signup.vue) | Signup page for users who do not have an account. It asks for a valid email address and for them to make and confirm a password. |
| [Swiping.vue](./src/components/Searching.vue) | The main page of **Pianpy** where users can see another tutor's profile and choose whether to 'like' or 'pass.' |
| [UserProfile.vue](./src/components/UserProfile.vue) | Similar to Settings.vue, on this page the user can change their profile information with their preferences in instruments |

### Authentication
As our app connects people and tutors, authentication is a necessity. Firebase provides a straightforward and easy-to-implement solution so we can focus on designing an accessible app. Users simply sign up with an existing email address and a password of their choice. Firebase Authentication does the heavy lifting to make sure users are authentic.

### Cloud Firestore
The obvious choice for storing users' information. It provides straightforward implementation for users to upload their photo and a relatively quick way to call and display these images for users to sift through.

# Acknowledgments

* Cohort 15 and all Holberton students - For your friendship, invaluable support, and insight not only for this project, but over the last year.

* YOU - For reading this documentation and testing out **Pianly**. We hope you enjoyed the ride!

# Related projects

* [AirBnB Clone](https://github.com/beautyscribbles/AirBnB_clone): a simple web app made in Python, Flask, and JQuery.

* [Simple Shell](https://github.com/trinixei/simple_shell): a command line interpreter that replicates the sh program.


## The Team
We are instruments enthusiasts who are passionate about coding but also like to keep it fun!

* **Florence Hanson** [@florencelhanson](https://twitter.com/florencelhanson) - A very talented Software Engineer.
* **Fatoumata Sarr** [@oumoukhalil](https://github.com/oumoukhalil) - 

Follow us for more social and tech related awesomeness!

