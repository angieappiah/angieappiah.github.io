---
layout: post
title:      "The Rails Project"
date:       2020-07-16 02:18:59 -0400
permalink:  the_rails_project
---


Bibini Gh Tour Guide was built using Ruby on Rails, no scaffolding was used to build this project. The app allows a user to sign up using an email and password, or log in via Facebook. The app also helps users to create a travel plan, add tour and locations to their intended place of visit.
 
 I have learned a lot through transitioning into Rails. This post points out some of the cool features I learned
 
**Gemfile**
 
These are the gems I added to my gemfile.

gem ‘omniauth’
gem ‘omniauth-facebook’
gem ‘bycrypt’

I used Omniauth to authenticate with Facebook. OmniAuth is a gem for Rails that lets you use multiple authentication providers alongside the more traditional username/password setup. I run bundle install to update these gems.

I created a config/initializers/omniauth.rb file, that helps configure the authentication provider. this file contains ; 
provider :facebook, ENV['FACEBOOK_KEY'], ENV['FACEBOOK_SECRET']. The facebook_key and Facebook_secret are generated once you sign up as a facebook developer.


**Validations**

In my app/models/user.rb file I added validations and has_secure_password to authenticate against a BCrypt password to ensure that users have a name, email, and password and the email is unique to each user.  below is the validations I implemented in my project

class User < ApplicationRecord
    has_secure_password 
    has_many :tour_users
    has_many :tours, through: :tour_users

    validates :username, presence: true, length: { maximum: 50 }, uniqueness: true
    validates :password, :confirmation => true
    validates :email, presence: true, uniqueness: true
end

Creating The** Views**

The Views folder is where users interacts with my app. I used partials to simplify my views and to keep it DRY. 

**The Scope Method**
Scopes are custom queries, defined inside the models that queries data from the database. I used

scope :long_names, -> { where("LENGTH(name) < 30") } in my project, to give me all location names where the number of letters in their names are less than thirty.


Building everything from scratch was a bit challenging but I am glad I did because I learned a lot through the process, Also attending study groups provided a lot of great resources that helped me keep going.


