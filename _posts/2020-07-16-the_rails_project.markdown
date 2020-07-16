---
layout: post
title:      "The Rails Project"
date:       2020-07-16 06:18:58 +0000
permalink:  the_rails_project
---


Bibini Gh Tour Guide was built using Ruby on Rails, no scaffolding was used to build this project. The app allows a user to sign up using an email and password, or log in via Facebook. The app also helps users to create a travel plan, add tour and locations to their intended place of visit

Creating The Application
$ rails new app_name
 
Installing the Required Gems
 
These are the gems I added to my gemfile.
gem ‘omniauth’
gem ‘omniauth-facebook’
gem ‘bycrypt’

Creating the Models
In my app/models/user.rb file I added validations and has_secure_password to authenticate against a BCrypt password to ensure that users have a name, email, and password and the email is unique to each user. 

Creating The Views
The Views folder is where users interacts with my app. I used partials to simplify my views and to keep it DRY. 

Building everything from scratch was a bit challenging but I am glad I did because I learned a lot through the process.
Stepping away from the computer and coming back with a clear head usually helped me keep going.


