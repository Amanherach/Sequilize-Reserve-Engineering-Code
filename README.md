# Sequilize-Reserve-Engineering-Code

## Description
Reverse engineer the starter code provided and create a tutorial for the code.

In the `Develop` folder, there is starter code for a project. Begin inspecting the code to get an understanding of each file's responsibility. Then, in a Google Doc, write a tutorial explaining *every* file and its purpose. If one file is dependent on other files, be sure to let the user know.

At the end of the tutorial, add instructions for how you could now add changes to this project.

## Password Authentication 
This app allows users to create an account, log into the account and sign back out securely. All user data is stored in a MySql database.

## User Story
```
AS A user, I want to be able to safely log in to "X",
I WANT to know my personal details are safely stored
SO THAT I don't have to worry about using "X"
```
## Google Doc Link
- [Google Doc Link] (https://docs.google.com/document/d/1lBgC3nMUGx9IvkLQnrmuI1H0spFpgcRe0XT_5zu3w0Q/edit)

## Tech Used
* BCRYPTJS
* EXPRESS
* EXPRESS-SESSION
* MYSQL2
* PASSPORT
* PASSPORT-LOCAL
* SEQUELIZE

## Installation
**Step 1 - Create a mysql db called "passport_demo" and git clone repo**
```
git clone https://github.com/achaudhry93/Sequilize-Reserve-Engineering-Code
```
**Step 2 - Go into the config file, open config.js and insert your personal data ie username, password etc**
```
config.js 
```
**Step 3 - Open terminal in current repo and run "npm i" to install all node packages**
```
npm install
```
**Step 4 - While in terminal, run "node server.js" and you will successfully connect to server**
```
node server.js
```
**Step 5 - Open browser and put "http://localhost:8080" in search bar**
```
"http://localhost:8080"
```
**Step 6 - enjoy using the app!**
```
```
## Files Explained 
CONFIG

  MIDDLEWARE
  
  isAuthenticated.js { 
  restricts routes that user is not allowed to visit if not logged in. if user is logged in, it continues with request };
    
  config.json {
  connection configuration to connect to server };
  
  passport.js {
  contains javascript logic that tells passport we want to log in with an email address and password, requires models files };

  MODELS

  index.js {
  connects to database and imports users log in data, requires config.json };
  
  user.js {
  requires "bcrypt" for password hashing. this makes our database secure even if compromised. Here we have JS that defines what is stored on our database };

PUBLIC 
login, members, signup.html {
these files are the general front-end framework layout of the page setups, each requires corresponding js file and style sheet in public folder };

  style.css {
  general styling of html sheets };

  login, members, signup.js {
  general javascript functionalities of button, forms and inputs as per html sheet requires };
  
ROUTES

  api-routes.js { 
  contains routes for signing in, logging out and getting users specific data to be displayed client side, requires passport.json file in config folder };
  
  html-routes.js {
  routes that check whether user is signed in, whether user already has account etc and sends them to the correct html page, requires isAuthenticated.js file in config folder };
  
package.json {
contains all package info, node modules used, version info etc };

server.js {
requires packages, sets up PORT, creates express and middleware, creates routes and syncs database / logs message in terminal on successful connection to server };

DB 
    schema.sql for quick run/insert of the listed database in step 1 installation.

## Repository

  - [Project Repo] (https://github.com/achaudhry93/Sequilize-Reserve-Engineering-Code)