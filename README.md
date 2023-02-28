![GitHub Repo stars](https://img.shields.io/github/stars/NullPounce/K12-Education-Focus-Scripts?style=plastic)
![GitHub all releases](https://img.shields.io/github/downloads/NullPounce/K12-Education-Focus-Scripts/total) 
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FNullPounce%2FK12-Education-Focus-Scripts&count_bg=%237E2676&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Views&edge_flat=false)](https://hits.seeyoufarm.com)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/NullPounce/K12-Education-Focus-Scripts) 
![GitHub](https://img.shields.io/github/license/NullPounce/K12-Education-Focus-Scripts) 
    


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/NullPounce/K12-Education-Focus-Scripts">
    <img src="https://github.com/NullPounce/K12-Education-Focus-Scripts/blob/main/ezgif-5-90a6697098.gif" alt="Logo" width="150" height="150">
  </a>

  <h3 align="center">Anti Rush School Focus Scripts</h3>

  <p align="center">
    anti rushing and focus scripts for K12 🧠💪⌚️
    <br />
    <a href="https://github.com/NullPounce/K12-Education-Focus-Scripts/releases">View Release</a>
    ·
    <a href="https://ko-fi.com/pounce">Support Me</a>
    ·
    <a href="https://github.com/NullPounce/K12-Education-Focus-Scripts/issues">Request Feature</a>
  </p>
</div>



# Does you're child rush through online school? No Longer!

https://www.youtube.com/watch?v=q7C8CjstWb4























# Tampermonkey Anti Rushing Script (with a time out :)

- UPDATE: Go-Back-URL-Alert-Counter.txt is now more accurate and the cancel button closes but still counts towards it counting it, over 100+ lines of code, i'll clean this up if i see any stars, traffic etc enjoy
![2023-02-15-11-06-25](https://user-images.githubusercontent.com/28081004/219085743-2d2b2c7e-4fbb-47f1-9ebf-2296622116a4.gif)

the match line currently sets this to work on all sites for you're student

# This Will
- If the user changes the URL more than two times within 10 seconds, the script displays a confirmation popup with the message "You are changing pages too fast. Please slow down and focus."

- If the user clicks "OK," the script goes back one page in the browser history. If the user clicks "Cancel," the script also goes back one page.

- If the user triggers this warning five times, a non-closeable popup will be displayed for 15 seconds, with the message "⌚️Time-Out: You are lucky to be doing school at Home on a computer💻. Wait longer before changing pages."

# Making Changes

# Changing The Set Time For Timeout
  
  just change 15000 which is 15 seconds in milliseconds to
 ```
 }, 30000);
 ```
 for a 30 second timeout
```
uncloseablePopup.appendChild(message);
                    document.body.appendChild(uncloseablePopup);
                    setTimeout(() => {
                        document.body.removeChild(uncloseablePopup);
                        uncloseablePopup = null;
                        popupCounter = 0;
                    }, 15000);

```






# change how many times the url needs to be changed
just chage the 2 to the amount you need
```
if (urlChanges >= 2) {
```













# changing url change alert on X amount of seconds (default is alert on 2 url changes within 10 secs)
edit the number 5000 which is 10 seconds to another ml number like 15000 for 15 seconds
although as you can see it needs to be half
```
 } else {
        urlChanges = 0;
        if (!timerId) {
            timerId = setTimeout(function() {
                urlChanges = 0;
                timerId = null;
            }, 10000);
        }
    }
}, 5000);
```

if you right click on the page and inspect element
in console.logs, in the filter type in: pop
now you will see how many times there was a pop up




# URL


if you want to change the script to only work on certain pages or only k12 pages you can change:
```
// @match        https://learnx-svc.k12.com/*
```



# 3 versions

- URL-Changer-Alert-Counter.txt
 this version removes the go back a page functionality

- Go-Back-No-Popup.txt
this version just goes back a page without notice if going too fast

- Go-Back-URL-Alert-Counter.txt

my default method which shows a pop up with ok/cancel that goes back 1 page saying slow down etc then on 5 alerts does a time out






# Q&A and you're issues or problems with this here

- Will you update this more?

Yes in the future when I have time; like sound alerts or having it show how many pop ups in the gui instead,
think the pop counter resets on refresh so i'll have to change that, maybe remote alerts.
  plan on making more scripts as well, for example my kid has a bad habbit of stairing at the shedule instead of clicking on a class,
  so later you'll find a script that kicks them into class etc etc :) happy schooling!

- I would instead get more materials for the kid to learn on their own instead of limiting the progress.

yes, we provide as much as we can after school for study, teacher can only come back to the kids screen so often to say stop rushing and skipping. if i sit there the whole time it would just become worse or start something. this is meant for kids who mostly are just in there room alone with a school chromebook, mine isnt lol teacher behind a pc with 30 kids aint enough to watch mine and a lil click of stop sharing is all it takes, i seen in class though all the other kids are in a bed room with the door shut. many tasks will mark complete even if you are in a click click next done kinda mood, schools not done til 3:30 why are you done at noon? well I got all my stars............ 


- You need to encourage and challenge them, not discourage and bore them.

against school rules for the parent to sit with the child during online school in some schools, can be in the same room of course. great idea i'll add a simple math problem inside the alert haha (too much), i've already removed the given answers on my kids school so we cant cheat here and made many emojis fall down the screen on correct answers. they have these chrome mascot addons that have health bars that change if you do certain things as a fun motivational incentive.


- This seems like a great way to stop them from learning anything

Ha how? what child can read a whole paragraph let alone a sentence on each page in under 10 seconds, the on screen reader button takes just as long, you reading every page you wont even notice like what.


- What are their grades? If they are "rushing" through the homework and scoring good grades, maybe they are just smart. Putting a time governor on them would only hurt, not help.

On the other hand, if they are not getting good grades and have trouble focusing, this might help. I'm not an educator or child development expert, so I don't really know.


don't expect a parent having a kid with good grades using this script, i've noticed the kid reading more of each page and grades have improved just over a week of use, this may not be for all I highly agree. Ha this post got banned just because people don't agree with it, okay so what it works on my kid and the teacher put it on kids chrome books who have a rushing problem and their grades are better too, don't like it don't use it lol these people.


- A script that just times how fast you change pages doesn't motivate to read more careful but to click slower and spend the waiting time doing something else.


depends on the kid, designed to show a alert on 2 url changes within 10 seconds and even then it gives you leeway then a timetable full screen pop up, works on like 20 something different kids with a rushing problem

# credits

- icon
https://www.flaticon.com/authors/kerismaker

- Tampermonkey
https://www.tampermonkey.net/



# Donate![icon](https://user-images.githubusercontent.com/28081004/214497772-e0d74e0c-66ca-4e1c-a88f-d0709b62890d.png)💜
for more scripts or ways to keep your child focused and allow me the time to do so please give a star or consider
giving me a visit over on kofi

<a href="https://www.buymeacoffee.com/NullPounce"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee <3&emoji=&slug=NullPounce&button_colour=BD5FFF&font_colour=ffffff&font_family=Comic&outline_colour=000000&coffee_colour=FFDD00" /></a>

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/X8X6I1K9I)


