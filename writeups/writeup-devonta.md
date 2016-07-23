# Delectable-Woylie Project Writeup:
## - Devonta Harris


## What I did:
> In this team project, I was required to build two portions of the overall UI we were assigned:

### The skills section:

![skills](writeups/skills.PNG)

> This section was a bit tricky because of the graphs. In the beginning, I used a jQuery plugin to accomplish the task, it worked, but I couldn't configure it the way the design looked so I had to scrap it and build it from scratch.

> I also learned quite a bit about cross browser inconsistencies. For example, Firefox didn't display the height of any of the bars while other browser did. Upon research I found that I had to explicitly set a `height` on the `<li></li>` element containing the bar for it to work in Firefox.

### Social media:

![social-media](writeups/socialmedia.PNG)


> The social media section also came with it's own challenges and cross browser inconsistencies. In particular, when coding the custom scrollbars. I found out that it was pretty straight forward to do in Webkit browsers (Chrome and Safari) with the help of these properties (There's more, but those weren't needed for this project.):

* `-webkit-scrollbar`
* `-webkit-scrollbar-thumb`

> Creating the same effect in other browsers is really complex and requires some CSS hacks in order to make things work properly.


## The learning process:

> Building these components was extremely beneficial because it served as a major learning experience. 
> To build out this project we used a couple of tools:

* Git
* Gulp
* Materialize Grid
* Pug
* Stylus
* Font Awesome
* Browsersync

> I was already acquainted with some of these tools like Pug (Jade), Gulp, Git, and Font Awesome, however I haven't used them in quite a while so I had to relearn how to used them. Tools like Stylus, Materialize Grid, and Browsersync I'd never used before.

> In the beginning it was pretty tough to get used to the workflow, but with the encouragement and help of my partner Oleg and some additional research I rapidly began to love and understand the usefulness of such a workflow. I liked it so much that I'm taking out time to thoroughly understand how they really work so I can add them to my workflow.
