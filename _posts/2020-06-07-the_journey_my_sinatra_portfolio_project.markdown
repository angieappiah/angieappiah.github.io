---
layout: post
title:      "The Journey (My Sinatra Portfolio Project)"
date:       2020-06-08 03:56:39 +0000
permalink:  the_journey_my_sinatra_portfolio_project
---


Creating an Application to help business and service providers to display their products on a bigger platform that will attract larger audience was what I finally decided to do. I made a simple chart about how I want the whole idea to be executed.

Being mindful of the following key concepts; "sinatra, activerecord, rack, database tables and SQLite3,HTML, ERB (Embedded RuBy) and forms,MVCs- Model View Controllers,The mechanics of sessions, routes,RESTful Routes,CRUD- Create, Read, Update, Delete and password protecting", I began with setting up a development environment followed by Models.

Models:  The foundation for my app are 2 models; firstly,  a User class which would have_many :products and secondly, a product model which would belong_to the Users. 
Views: With the CRUD functionality in mind, I used ERB files to support creating new users and products, viewing your products , editing Only your products, and being able to delete  your product.

Controllers: There is a User Controller and a Product Controller which inherit from  Application Controller creating routes that correspond with the CRUD actions above

I learned that it is important to plan out the structure of your code before you start coding. I also enjoyed stylizing with CSS and being creative with my forms and layout

Please see my github repository: git@github.com:angieappiah/bibini-products.git



