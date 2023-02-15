![GitHub Repo stars](https://img.shields.io/github/stars/NullPounce/K12-Education-Focus-Scripts?style=social)
![GitHub all releases](https://img.shields.io/github/downloads/NullPounce/K12-Education-Focus-Scripts/total) 
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FNullPounce%2FK12-Education-Focus-Scripts&count_bg=%237E2676&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Views&edge_flat=false)](https://hits.seeyoufarm.com)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/NullPounce/K12-Education-Focus-Scripts) 
![GitHub](https://img.shields.io/github/license/NullPounce/K12-Education-Focus-Scripts) 
    


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/NullPounce/K12-Education-Focus-Scripts">
    <img src="https://cdn-icons-png.flaticon.com/512/7481/7481956.png" alt="Logo" width="150" height="150">
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

























# Tampermonkey Anti Rushing Script (with a time out :)
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


