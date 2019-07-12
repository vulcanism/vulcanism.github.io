---
layout: post
title:      "Sinatra Project"
date:       2019-07-12 14:45:32 -0400
permalink:  sinatra_project
---


When I first saw that we were approaching the next project in the curriculum, I remember feeling uneasy. The first project had ended up being much more anxiety-inducing and complicated than I expected, and while I was determined to face this one head-on, I worried about getting hopelessly stuck on a new problem every day.

As it turned out, my first issue wasn't related to the actual coding at all. Shotgun, one of the most important gems we'd been using throughout the Sinatra unit, didn't work on Windows. Go figure. So, one day went towards trying to deal with that, first by installing an alternative gem that supposedly functioned in the same way. When that only sort of half-worked, I ended up following a guide to get a Linux shell set up on my PC, allowing Shotgun to function. I made a note to myself to get started on the next project early in case there are similar issues.

Finally, I was ready to set up my app. Thanks to a former Flatiron student, I was able to clone the Corneal gem, which handled created all the basic files and folders for me. I'd decided that my subject would be books this time around—when my project was finished, users would be able to sign up, add books to their collection (as well as edit or delete them), and view what books other users had recently added.

I started my process by creating and migrating one table for users and one for books, setting up dependencies with each. From there, I went into my "Views" folder and added some of the files I knew I'd need, such as a login and signup page for users, and an index that displays all books.

From there, I set up a couple of helper methods to make future coding easier: one to check if a user was logged in, and one to identify the current user. Later on in the process, I'd also end up adding two additional helper methods: `#valid_username?` and `#valid_book?` The first was to make sure each username was unique, as well as that the field wasn't left blank, and the second simply checked if any book parameters had been left empty.

With my helpers in place, I began stubbing out some basic routes in my UsersController. To my surprise (and relief), I found that I was having a *much* easier time with this project than the previous one. When I encountered errors, they didn't take hours of testing and head-scratching to solve. I'm sure part of that comes from experience, but the Fwitter lab ended up being incredibly helpful throughout the process.

Once I had my signup, login, and logout routes built out, I put together the necessary forms in each respective `.erb` file. For some reason, I didn't think to test my login function at this point; after I confirmed that the signup and logout worked, I moved along. This was a mistake, because my login actually *wasn't* working, and I wouldn't notice until almost a week later. Whoops.

After that, I moved onto building out my BooksController routes, such as `post /books/new`, and `get /books/:id`. When errors cropped up, I was able to fix them and keep going, rather than spending an entire afternoon trying to solve one problem. As a result, I actually ended up finishing earlier than I expected!

I never thought I'd have time to try the "bonus challenge" included with any project, but I decided to try with this one. The `sinatra-flash` gem ended up being less tricky to work with than I expected, and while I might've been able to do more by playing around with the CSS stylesheet, I'm happy with the result. Overall, this entire project has proven to be a nice confidence boost for me; I feel like I'm really starting to see tangible progress in my learning experience.
