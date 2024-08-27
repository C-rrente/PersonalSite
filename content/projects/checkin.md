+++
title = "QI Check in System"
date = 2022-10-01
description = "Check in system developed for the Qualcomm Institute Makerspace"
image = "./checkin-assets/checkin-main.jpg"
+++

<img src="/yo.jpg" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto"> 

Upon arriving to UC San Diego, I decided to start looking for student jobs to keep myself 
afloat while in school. I ended up getting a job at a new developing makerspace in the Qualcomm
Institute on campus.

After a few weeks of 3d printing, laser cutting and learning some woodworking and metalworking, I 
was given the task of continuing a project that my boss had started.

The project was to create a check in system for students and staff to use that used an RFID reader that 
he made. This device consisted of an ESP-32 connected to an NFC card reader that would send the information
over serial. He wanted the users to be able to make accounts via a GUI after scanning their card so their 
account would be linked to their ID.

Knowing very little about software design I embarked on this learning experience in October of 2022.

Unfortunately, I was incredibly stressed at the time with school and my home life so I was making slow progress
but still progress.

<img src="/og-main-page.jpg" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto"> 

<img src="/og-no-account.jpg" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto; padding-top: 5px"> 

Regardless, I taught myself a large amount of Python and learned tkinter from scratch. I eventually
got scanning to work and it could create an entry in a Google Sheet where our data was going to be stored.
I also created a working GUI with buttons, titles, images, messages and entry boxes.

At this point I had also began to implement a way to use the magswipe that were embedded in our ID cards.
My boss was able to create a Python script that pulled user information from our school's database in a way
that was secure. I linked this script to a magswipe reader and allowed students to easily fill their information.

The reason behind the students using the RFID tag in their ID card was for the future implementation of Fabman devices.

![](/fabman.jpg)

These devices act as remote switches for heavy machinery, and the company hosts an account system where you can give people 
access to certain devices. I started work on implementing the Fabman API into the system allowing the backend to automatically
create the new user a Fabman account and have their card work with Fabman devices, and if a user had an account before this implementation
it would make them a Fabman account as well.

The idea moving forward was to have checkboxes for each user on the Google Sheet so any staff could give user's access given they met the
criteria. So me and another newly hired programmer developed a script that would give a certain user access based on their selected checkboxes.

Over this time I had been making consistent updates, bug fixes and improvements. I had my own trello board where my team members could bring issues
to my attention and I could create a plan on how to fix it.

After a while, and starting in the summer of 2023 a designer, who was also a student with me, decided to redesign the GUI into something more pleasing.
And since traffic was low in the space, I could spend time organizing code and refactoring a lot of things that I messed up while learning Python.

[Sual Jimenez](https://sauljimenez.com/qualcomm-makerspace-check-in-overcomplicated) 
Led the design of the GUI and we met often with other staff and came up with a design that was more pleasing and more effective.
I've included a more in depth page Saul made going over his design process for the GUI.

<img src="/new-main.jpg" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto; padding-top: 5px"> 
<img src="/new-account.jpg" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto; padding-top: 5px"> 

These are just a few of the 10 pages that were made to accommodate the new design.

After he had finished the pages, I began to look for a way to take his designs from Figma. We ended up 
finding a [tool](https://github.com/Axorax/tkforge) that converted his designs into tkinter code.

This made it much easier for me to implement these designs and make them functional. This task, however, was
still a major challenge.

When creating this a lot of the code used for the system was in just one file, as I didn't know much about
Python's file separation and the proper way to make projects. So my biggest task was essentially 
rewriting the system to fit neatly into separated files that were organized and easy to modify.

This took me a month or two of just spending hours refactoring the code and testing it to ensure I didn't break anything
at the end of the day.


<img src="/og-github.jpg" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto; padding-top: 5px"> 

This is what the file system looked like before I organized everything. Where basically the entire system ran
through the single checkin.py file.

<img src="/new-github-main.jpg" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto; padding-top: 5px"> 
<img src="/new-github-src.png" alt="Image of Check in" style="display: block; margin-left:auto; margin-right:auto; padding-top: 5px"> 

And this is what it looked like after I had finished reorganizing and implementing each page.

Overall I learned so much from this project, my Python skills have improved tremendously, I can make GUIs
somewhat comfortably and I gained social skills from working in a team that I'd never had before.

This system is still running in the DIB and since my leaving, has been implemented in two more facilities
on UCSD's campus.
