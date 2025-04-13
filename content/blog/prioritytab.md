+++
author = "Prince Sharma"
title = "I built a chrome extension to finally close my 100+ open tabs and get stuff done"
date = "2025-04-13"
description = "Built a simple todo app extention, it got featured on producthunt, heckernews and reddit"
tags = [
    "projects","build"
]
+++

> I vibe coded a chrome extention that helped me organis my task better at work and help me get stuff done faster
> In this post I described how i built it, what I learned coding with AI
> Also, I'm at episode 605 of onepeice now, so you can guess why the late post :)

Top 3 posts on r/deveopersindia for a day : [Reddit Post](https://www.reddit.com/r/developersIndia/comments/1jy0wtp/i_built_a_chrome_extension_to_finally_close_my/?sort=new#lightbox)

I used to have 100s of tabs open — half were tasks, the rest were links I didn’t want to lose.

Now, if something’s quick (like replying to an email), I just do it and close the tab.If it’s a task that’ll take time, I add a one-line note with a link (if needed) to the To-do tab.If it’s not a task but something I want to read or save, I add it to the Links tab — and close the tab.

This small workflow has been a game-changer.

I finally feel okay closing tabs and can focus better.The to-do list forces me to pick just one thing to work on.When I mark a task done, I can even add a link — super useful for things like code reviews or docs I’ve created.

It helps me track what I’ve done and where the work lives.

Would love for you to check it out and let me know what you think! 🙌

[Crome Webstore Link](https://chromewebstore.google.com/detail/prioritytab/aadejinhokcmkpbcofpmoccicpmelkfa)

---

## Table of Contents

- [Screenshots](#some-screenshots-of-the-app)
- [My process of building the todo app](#my-process-of-building-the-todo-app)
- [How i got the idea of building this todo app](#how-i-got-the-idea-of-building-this-todo-app)
- [Version 1 of the input i gave to cusrsor](#version-1-of-the-input-i-gave-to-cusrsor)
- [Added some improvements](#added-some-improvements)
- [Hyperlink support when creating new tasks](#hyperlink-support-when-creating-new-tasks)
- [Rabbithole of implementing more features : Subtask support](#rabbithole-of-implementing-more-features--subtask-support)
- [Ideating names, marketing content and chrome listing content with AI](#ideating-names-marketing-content-and-chrome-listing-content-with-ai)
- [Chrome listing got rejected the first time](#chrome-listing-got-rejected-the-first-time)
- [Some examples of ridiculous errors that i got due to AI editing the code](#some-examples-of-ridiculous-errors-that-i-got-due-to-ai-editing-the-code)
- [purchased cursor pro and added some more improvements](#purchased-cursor-pro-and-added-some-more-improvements)
- [How this has helped me with my office works](#how-this-has-helped-me-with-my-office-works)
- [What's next?](#whats-next)


---

### Some screenshots of the app

Homepage
![homepage](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/homescreen.png)

Todo Tab
![Todo tab](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/todotab.png)

Links Tab
![Links tab](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/linkstab.png)

## My process of building the todo app

1. I created a todo file with the details on my requirments for what i want to build
2. Gave the requments to v0 and asked it to generate a user frindly UI for this app
3. I created the first version using cursor agent editing on it's own
4. Keep on refining the app wih cursor adding new features
5. Bug fixes become increasingly difficult with AI as the codebase increases.
6. In these cases it's easier to feed the files to gemeni 2.5 pro and ask what to fix, to get specific gudance on what code to update. You should understand some of the code for this to work
7. Ask questions about the block of code you think will need fixing understand the context and apply the fix

#### How i got the idea of building this todo app

*inspired by how blot maintains their todo task*
https://blot.im/news 
I really liked how the author here manintais a single todo file for all of his product/business task at one place. This is really easy to undersatnd and I belive having a single todo list over time forces you to focus on important tasks among all the things you could be doing.

*Solving my own problem*
Also at the time of building this I had 100+ tabs open on my work chrome profile, 300+ on my personal account and 1200+ tabs open on my mobile phone. So you can guess that there was a problem of me opening something and then never getting to it. Since I had too many things to work on i get overwemled and then procastinate and do not do anything. Hvaing this single list would help me fix this problem. Hence you can say I'm solving my own problem. The scope of this work related task fiorst but later I'll move on to get my personal task organised as well, maybe soe changes will be required to the app then 

![Links tab](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/inspiration.png)

#### Version 1 of the input i gave to cusrsor
<details>
<summary>Version 1 raw prompt</summary>

I want to build an chrome extention to track To do items for your daya to day tasks.
This is a chrome extention. Once the user installs this extention. The todo page is open whenever the user open a new tab on their chrome browser. 
This todo page contains the below 
It's a simple app with ony two sections:
    1. To do 
    2. Done
The To do section is the list of items that you can keep adding to
At the very top there's a text feild to add these items
All new items are added at the top of the list and the old items keeps moving down once any new items is added
The todo section takes more part of the UI (as shown in the screenshot)
You can add items like bullet points, add some like in the items (like youtube link, email thread link that you want to look at, etc)
You can add subitems for a given task, in this case the subitems becomes the tasks that you can individulally mark done. Once all the subitems for a given task is marked as done the task itself is moved to the done side
When marking the items as done you can  link the item to the doc that you prepaded for the item, the link to the github commit you made to fix some issue, or simply the link to the email thread that you replied to or maybe not add link at all. 
Adding links when marking an item as done is optional

Adding a new todo items should be as simple as editing a emply bullet point at the top with teh place holder text "add new tasks here"
Editing any exisisting task should be as simple as clicking on the bullet point the user wants to edit and then editing the text
When the user ckiks on existing tasks and stars editing, he sould see a button to dellete the task on the right end of teh task, it should be a subtle delete option on teh right following the design standard described below

The todo items should be stored locally in the users machine, which is persistent even if the user reloads
The user can also at any point download their data as a todo.txt file and done.txt file using a button on the UI
Both of these will be simple txt file for example below (for the screenshot attached)
todo.txt
```
Are there any missing templates because of the switch from lowercase to true case?

Fix issues with menu links based on case

Fix issues with bad permalinks based on case

Fix template partial embeddings which no longer work because of switch from lowercase to true case:
- e.g. {{> /pages/home.txt}} when pages is really Pages
- we should resolve the case-insensitive path to file when saving a template and parsing its partials
```
Similar file will be donloaded for done.txt

Benefits of this to do app vs others or why this would work
This is a simple ist of tasks that you can keep adding to
The task that you add latest 
There are a variety of complicated tools to track tasks but this is the most simplistic of them all where you get a single view of all the tasks that you need to work on and teh tasks that you have completed.
If the items sits in the todo list for a long time, new items will be added above which are nore important and the old task will move to the bottom so that it does not take your attention or stop you from what you are working on currently


UI guidelines:
I want to keep the UI very simpleistic and minimilistic so that the user can very easily add new items ion the todo section
Moving an item from todo section to done section should also be very easy (with an option to add an optional link)
There should be an option to switch to dark mode or ligh mode
Use the simplistic design style that I have provided in the screenshot as example (ligh blue, white for light mode and similar for dark mode)

1. Update this to Follow the design exactly how it is in the screenshot attached including text size, etc. There should be a left pannel which has a tab to do which opens this page and other options are Links (coming soon) , Notes (comming soon)
2. Adding subtasks should work if the user edits the task goes to new line and then enters Tab, this hould add sub bullets to the task and add subtasks as visible in the screenshot attached
3. Think of a more subtle and minimilistic way to marking a task as done, ask for the link when marking the task as done, but this should not be a popup, rather a inline way of addng link optionally which is minimilistic


I want you to create a chrome extention from scract for this, created neccerady files, folders etc

I added the blot screenshot here so that it knows what kind of UI i'm expecting

</details>

#### Added some improvements 

1. When the user hovers over an existing task in the todo section, the circle bullets should change to show a tick mark there which gives the user a visual feedback that he can click on the circle bullets to mark a task as done. 

2. currently When a new task is added the user is required click on add new task again to enter the next task, it should automatically be selected, so that the user can add multiople tasks and enter

Build with cursor by Prince Sharma (@astronautprince)

1. Let add some sample task by default that explains the user on how to use the product.
    1. These are sample task to help you understand the product
    2. Add a new task by simply clicking the above text area and start editing, once you're done press enter to add the task
    You can mark any task as done by clicking on the grey circle, when you hover over a task you'll see a tick mark to mark the task as done
    3. When marking the task as done, you can add links for the comleted task optionally. These can be link to the github commit you pushed, email thread that you replied to, or maybe a google doc / google sheet you created for the task, or maybe a jira ticket youb created. You can link them here so that it's easier to find what has already been comleted to share with poeple, etc
    you can delete a task easily by clciking on the x on the right side, this is visible 
    All your tasks are  stored locally on your browser private to yourself.
    You can download your data by cliking on download data button, this will download two files todo.txt with all your todos and done.txt with all you done tasks
    Switch between dark mode and light mode by clicking on the button on the top right

Sample done tasks
1. This is an explample of how a done task looks like, you can click on the link for more details or click on the spehere again to undo if you moved the task to done by mistake
2. We belive task management should be plainsimple, this is an efforts towars the same. You can remove these now by clicking on the x on the right and get started 
3. Lastly you can share any feedback at princesharma.pri@gmail.com

#### Hyperlink support when creating new tasks

> Adding hyperlink support in the task listing was really tricky, I struggled explaining what i wanted to implement to the AI. (maybe this step can be optimised? like talk to gemeni explain what i want to change then ask it to come up with a detailed prompt for the LLM)
> I wated a lot of time here getting this to work right, will improve on my next project (coming soon ...)


1. When adding a new task the should also be able to add link in the tasks by selecting some words and then using cntrl + k to link a certain selction to a link

I want you to add the support for linking a selection to some external url when creating a new task. Just like when we edit in google doc you can select a text and press cntrl + k to link that text to some url. Once linked the text changes to blue color and underlined. when user clicks on this text again they can see the url and clcik the URL to open the url in new tab
When these task gets added to the done section the text where url is linked is preserved. and clicking on the text which is blue and underlined opens the url in new page. hovering on these underlied text shows the URL that is inked to the text. think throughly and implement this functionality for this app. keep the minimilisting desig guidles in mind and build a seamless user experice 

Improve the UI to have a line connecting the circles on the done section, 

Add a homeoage? people might now want to shaow their todos on every new tab, there should be some home page with link to the todos page
What should be there on this homepage?
Hello Prince, today's Tuesday 29th March, what are you upto?
faviourite quotes from mivies, etc
Boxes with TO ds, links, Notes, etc

#### Rabbithole of implementing more features : Subtask support

> Then I went don the rabbithole of implementing new features like adding subtask support, again i struggled a lot here to exolain the AI exactly what i want to implement, and it kept making mistakes, this part was really frustating
> finally I decided to not build this feature since it's only a marginal iprovement and not that useful anyways
> look at how i tried to expolain this to the AI below, it was really painful!

iteration 1:
Now i want you to add the feature of adding subtasks for a given task. This should work both when user is adding a new task and when the user is editing an existing task. When the user adds a new task and presses tab it sould add a sub bullet for this eixtsing task. This task then turn into a task which has sub tasks and the circle to makr this as done disabppears, rather these circle appes for all the sub tasks added. And when the user marks all the subtasks under a task as done it is moved to the done section. Also, the tasks with sub tasks should support expand and collapse (there can be and arrow at these kind of tasks)
follow the minimilistic UI and UX guidelines and implement this in a seam less way

Only one level of subbullet is supported

Iteration 2:


Now i want you to add the feature of adding subtasks for a given task. Sub task should work seamlessly similar to how it works on google doc bullet pionts, the user can add a new items press enter and then go to the next item and press tab that moves the item as a indedted sub bullet. Simailrly the user experice should be seamless here as well, the user can add new task go the the previous task and press tab to move it as a subtask of the previous task.
When user clicks on some sub task they can edit it, if thet press enter new subtask is added at the top of this task as a subtask and the user should be able to type this new sub task similar to how they add a new task
When the presses tab for any existing task it sould be moved as a sub bullet for this eixtsing task above that task. This parent task then turn into a task which has sub tasks and the circle to mark this as done disabppears, rather these circle appears for all the sub tasks added. And when the user marks all the subtasks under a task as done it is moved to the done section. Also, the tasks with sub tasks should support expand and collapse (there can be and arrow at these kind of tasks)
follow the minimilistic UI and UX guidelines and implement this in a seam less way

Only one level of sub bullet is supported

DO NOT BREAK ANY EXISTING FUNCTIONALITY

> When working on this I wasted a lot of API calls and the AI actually broke many of the existing features like below

There are a few issues still:
When I presses enter for a subtask, a new subtask is created but i'm not able to edit the new subtask items, i should be able to edit and add the task that i want to add. think throughly and implement this

Collapse is not working for the tasks with subtasks

marking any task as done is not working, this was working earlier. please fix this

> i did a lot more of this but not including here since i hope you get the point
> Decided to Abandoned the subtask feature for now, going to launch with what is built

#### Ideating names, marketing content and chrome listing content with AI

I have built a simple todo app which is a very easy to use minimalistic todo app that is agin different from what's out there in the market. I'm sharing more details below now help me come up with the marketing material for listing this chorme extension on chrome web store

Suggest the 
Name of the app
A one or two line description of the app (link an elevator pitch focusing on why this todo app willl help users get task done and how this is different than traditional todo apps)
Overview: A short 4-5 bullet points and some lines on overview of this app (make sure this if optimised so that if the user reads this description he is convinced to install the app)

description and features of the to do app

Description:
1. This is a minimilistic todo app that opne up on your new tab, with quick access to your to so items. 
2. We follow a single to do list with most recent items added on top, this method help in forcing the users to prioritize which task to pick up first restricting the attention to only a few tasks ata time. If the task get ignored for too long iot will move to the bottom and out of focus and hence menaing the task is not important
3. simuktaneouasly the user can keep marking items as done
4. When creating the task the user can add links using cmd k and when marking a task as done, you can add the link to the artifcat that you worked on for the given task so that it's accessible always

Benefits of this to do app vs others or why this would work
This is a simple ist of tasks that you can keep adding to
The task that you add latest 
There are a variety of complicated tools to track tasks but this is the most simplistic of them all where you get a single view of all the tasks that you need to work on and teh tasks that you have completed.
If the items sits in the todo list for a long time, new items will be added above which are nore important and the old task will move to the bottom so that it does not take your attention or stop you from what you are working on currently

Securinty and privacy
This is built with security and privacy in mind
All the tasks are stored in your local chrome storage and never sent to any servers outside of your computer
The user can download the tasks at any point of time using the download data button
there is no telemetery, or user analytics collected prserving full user privacy

#### Chrome listing got rejected the first time


Can you make the below changes:
1. Remove the google search from the home page rather add a quote of the day section in place of the search bar, which should be editable and shouls follow the same minimal design practice. Have the initial quote as "Having no doubt ! That makes you strong !" - OnePeice and show people some helpful nudge showing that ethy van edit this quote and add their own. Make sure you follw the minimal design practice when designing this. 

2. Can you add a slight blueish higlhigt when someone has clicked on the task to edit and the task is on focus. So that the users has some feedback on which task they are editing. make sure this also follos the minimal desgin guidelies. 

3. After adding hyperlink in the tasks, the left arrow, roight arrow, etc keys don't work. The user has to click someplace else to go back to editing. Can you fix this? 

Update the task selection UI, so that it's background color changes or highlights once setected

Genrate the thumbnail images for this app
Get the name, description, etc finalised 
Publish on chrome store

#### Some examples of ridiculous errors that i got due to AI editing the code

![Error 1](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/error1.png)

![Error 2](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/error2.png)

#### purchased cursor pro and added some more improvements

> I tried to not pay for customer by using multiple different personal emails, but cursor has a limit on number of free trails on a device mac address level, hence rather than running this on a new VM i decided to pay the $20
> i also had to pay the $5 chrome developer enrollment fees for some reason

I want you to add a few improvements here:

1. Add the functionality to import todo.txt and done.txt , as of now the app supports the functionality to export all your todos and done items as two seperate files todo.txt and done.txt . Now i want to add the functioanlity so that user can upload these files in the same format as sownloaded and then import all their esisting todo items and done items. Thsi should work seamlessly, the hyperlink in a todo item should also get imported and also the links for done items should also get seamlessly imported

2. I want you to add the Links section support, I'm describing the use case below and user needs, etc you should follow minimal design standards as folowed throughout this app (chrome extention) and build a minimal user experice that allows user to organise their links
-  the user can organise liks mainly into below types
    - Bookmark kind of Links that the user will want to store and might want to visit from time to time. for eg. for a PM working in a tech firm might have links like: a google sheet link for thier roadmap, google doc lins for their PRDs that they are working on, A google sheet with product improvement feedback from GTM team or othe stakeholders, etc . Basically these are the Links that the user want to store in like a bookmarked links kind of section so that they can easily visit these from time to time. When user is entering these links he should also add a title for thse links so hat it's easily able to idenitfy based on the title hey give, and the title will link to the actual document
    - To read links / Reading lists : These are the type of links that the user wants to visit and read once he has time ton go through these. examples can be a link to an email thread, some internal tech doc that they need to read, some tech blog, etc 
    - Archived links are all the liks that the user archives from the above two list or he can add new links directly in this section, it's okay if this sectionis somewhat hiden because user wants tio store these links but might not visit them regularly

When adding any new link the user can add a title for the link and optinally a short description of the link

Remember the design for this new Links feature should be minimal, so showing a preview of link is not required, similarly other things that take up users attention but is not really need should not be includd in the UI, The UI should be a clean and simple where addign new links should be really easy and accessing already saved links should also be very easy

The export data feature now should also support exporting this links section as a seperate file links.txt which has organised links, user should also be able to import this file to import previous links

Now based on these requiemtents and design guidelines design a minal link management feature in this ap, which opens up when user clicks on links tab

DO NOT BREAK ANY OF THE EXISTING FUNCTIONALITY

#### How this has helped me with my office works

> I got to close most of my open tans thanks to this extention! 
> I have a much cleaner workflow now where i only concentrate at one task at a time and get things done faster
> All my to read links (some of the links are probably open for more than 3 years) are now closed tab with the peace that I know i have added them to a signle to do list and I'll read them when they show up on the top os my to do list.
> This made me realise there are only so many things I can do at a time! Hence laster focus is the most important thing!

![Work 1](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/work1.png)

![Work 2](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/work2.png)

![Work 3](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/work3.png)

![Work 4](https://raw.githubusercontent.com/Prince-sharma/blog/main/data/images/prioritytab/work4.png)


### What's next?

1. Share this with 10-12 collegues and get then to install the app and wrote reviews
2. validate if the problem I identified really exists
3. Talk to people to see if they really find this app useful
4. Once I know that this is a real problem, and incorporated some basic feedback launch this on product hunt
5. Make the listing page more appealing, so that new people can trust this enough to install
6. The images are too small and blurry, maybe do not include actual screenshots and rather focus on the value proposition. so that the user has enough details to install and has no privacy concerns ,etc. 
7. when they install they'll see the product anyways!