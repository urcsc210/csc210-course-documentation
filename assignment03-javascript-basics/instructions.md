# Assignment 3: JavaScript Basics

*Due: Thursday, September 10, 2020* 

Your assignment is to take your Assignment 2 files and install and customize an existing set of JavaScript code, and then improve upon it.

The main purpose of this assignment is to demonstrate how JavaScript can manipulate the DOM of a webpage.

*Note: do not use jQuery or any other library for this assignment.  You need to demonstrate your ability to deal with simple JavaScript by-hand before we move-up to libraries and plugins.*

## Steps


1. Download and extract [the starter file](scripts.zip)
2. Make a copy of your Assignment 2.  Call it **Assignment 3**.
   - If you're experienced with GitHub, this would be a "branch" (not required for this assignment)
3. Attach the extracted JS file to your **Assignment 3 HTML file**
4. Edit your **HTML file** and the **scripts.js** file

   - In your HTML file, add **IDs** where needed
   - In the **scripts.js** file, replace the blanks; get the JavaScript as-is to work with your HTML

*Completing the steps above correctly will get you 75% of your grade for Assignment 3.  Complete the following steps for the rest of your grade...*

### Optimize and Improve the JavaScript

- Edit the JavaScript to fix the **errors** seen in the console (10 points)

- Create new function(s) to *abstractualize* some of the procedures (5 points), and move the new functions(s) *outside* the anonymous **DOMContentLoaded** function that wraps all the JavaScript (10 points)

  - Note: it's a good practice to have a "main" function that calls everything else, even if it's necessary because you installed your scripts at the bottom of your HTML ...so leave the DOMContentLoaded function there anyway!

  - BTW - there are variations of that function, not just DOMContentLoaded...

    ```js
    window.addEventListener('load', function () {
      alert("It's loaded!")
    })
    ```
    
    ```js
    window.onload = function() {
      init();
      doSomethingElse();
    };
    ```
    
    ...and more - some work a little differently than others.  (See [MDN web docs, Window: load event](https://developer.mozilla.org/en-US/docs/Web/API/Window/load_event) for more information)

- Make any other improvements you can to refine and optimize the script; surprise me!  (Remember: no libraries like jQuery for this assignment) (5 points)

## Publish and Report your Work

Install your Assignment 3 webpage on the **class web server** using the FTP credentials below

Note: **everyone will use the same FTP account**. Be careful *not* to disturb other students' files!

```
FTP Server (a.k.a. Hostname): ftp.csc174.org   //yes ...csc174, not csc210!!!
FTP Port: 21
FTP Username: assignment03@csc174.org          //again, csc174
FTP Password: [see the #announcements channel in Slack]
```

- When you FTP-in to the account, **create a folder using your UR NetID** (e.g. rkostin) and place your webpage files in there

### Check Your Work

- Open a web browser and go to this web address, below, where “*username*” is your UR NetID  (example: **rkostin**) and "*filename*" is whatever you called your HTML file (example: **index**)

  `http://csc210.org/assignment03/username/filename.html`

If you did everything correctly, you should see your simple webpage with your name on it. 

### Report your Work

- In our CSC 210 section in Blackboard, in **Assignment 3: JavaScript Basics** , click the "Write Submission" button then in the text box...
  - Post the URL (not the actual files) to your webpage on the class web server 