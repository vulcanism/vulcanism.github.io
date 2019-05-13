---
layout: post
title:      "Ruby CLI Project"
date:       2019-05-13 00:25:24 +0000
permalink:  ruby_cli_project
---


Where to begin with this whole experience! Without a doubt, this project was the most challenging thing I've had to do yet as part of the Flatiron curriculum, but I can also say it was the most rewarding.

I'll be honest, my process began with panic—it was a good thing we had three weeks to work, due to the timing of our break, because I spent an entire week frozen with anxiety. The project seemed like an impossible task, to the point where even trying to find a good starting point felt overwhelming. What eventually helped me the most was having a check-in call with our cohort's educational coach, Ann Heilman Murphy. She reassured me that most students got a little panicked when they saw the first project, and that there were plenty of resources available when I got stuck.

By then, I'd at least selected a topic for my project. I've always been a video game fan, so I decided to scrape a page that listed companion characters in Dragon Age: Inquisition. The first real challenge ended up being the task of setting up my local environment. I'd wasted hours struggling with the browser IDE, and there were so many different code editors that it was a struggle to figure out which one I should use. Thankfully, multiple people in my cohort willing to help, and suggested I use Visual Studio Code.

In order to get my gem set up, I followed along with Avi's "Daily Deals" walkthrough, which proved to be immensely helpful throughout my project. I figured I would need three files: a CLI, a scraper, and one for a companions class.

With the necessary files and classes created, I moved on to add some basic methods to each, just so they wouldn't be empty. For the CLI, I added simple `#start`, `#welcome`, and `#goodbye` methods, going off the "Daily Deals" video. From there, I created some empty methods I knew I'd need later in the other classes, such as `#initialize` for the Companions class and `#scrape_info` in my Scraper.

I began to build out my CLI by "stubbing out" code. For my `#options` method, which would eventually display my scraped data and allow a user to select from a list to know more details, I built a case statement that would simply output "1," "2," or call `#goodbye` based on my input.

My first real roadblock occurred when I tried scraping my webpage. I was inputting the code exactly as it appeared in Chrome's inspect window, but it wasn't working. After struggling for a while, I noticed that there would be open office hours soon, and with help from there, I was able to get my scraper functioning. `binding.pry` was my best friend! What really threw me for a loop was having to set up two `.each` methods, one nested inside the other. Since I was pulling data from a table, though, it made sense—one grabbed the HTML for the table, and the other went row by row to get the data.

After that, things became a lot easier. I referenced the Student Scraper lab to assign the data from my scraped hash to my Companions objects. My case statement from before became an if statement, and after asking for a little more help to get my CLI working how I wanted, I was pretty much done! All that remained was cleaning up the code.

Now that the project is complete, I can definitely say that I had no real reason to panic. Help was readily available for me every time I hit a wall, and I was never treated like I was dumb for being confused by something. I'm proud of what I've accomplished with this project, and learned a lot by building it.
