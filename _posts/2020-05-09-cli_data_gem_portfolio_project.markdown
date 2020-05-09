---
layout: post
title:      "CLI Data Gem Portfolio Project"
date:       2020-05-09 18:34:13 -0400
permalink:  cli_data_gem_portfolio_project
---

I started this project using "draw io" to build the concept I intended to execute.
![](Screen Shot 2020-02-12 at 4.45.00 PM/)

 I scraped the "touringghana" tour site for a lot of sites available when you travel to Ghana. There are a lot of people traveling to ghana each year for the "The Year of Return", so I thought this will be a good project to work on.


After getting the blueprint of the entire project, I planned out what I wanted the gem to do:

The User will input a number from a range of numbers to Launch the Program. Upon launching the program, the user should be presented with a list of popular sites to choose from. User can then select from the options displayed in a number to get more details. The User can also type "exit", to opt out if not interested.


I  created my gem (bibini) with Bundler and used gemspec file to add in the required information and dependencies like Nokogiri for scraping the website and pry for testing. I also updated the environment file to include all of the required gems and files

Methods used

CLI - this contains the methods that run the program
Scraper -  contains the scraper class that extracts all of the information from the "touringghana" site and creates new instances in the sites classes
sites - this class file stores all of the sites and the popular ones to display

Storage
  I pushed all my saved files and entire project to Github. I found this part very challenging, as I could not retrieve my saved files from Github. I had to write the code over and over again, until I realized I was missing a step that will fully commit my saved files.

Lessons learned
The excitement you get when you run the code and get the correct feedback is very fulfilling. Nonetheless having to deal with bugs, sites that are not scrapable among other errors that get you stuck can be frustrating. Through it all, I learned to give myself a break, refresh my mind and get back to fix it.




