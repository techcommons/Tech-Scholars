# Tech Scholars Digital Archive

## Instruction Manual
Any additions to the Tech Scholars website can be made directly through GitHub's user interface. However, this is a public repository, so you may also clone this project onto your local machine using the command below in your terminal. This would allow you to test your changes before committing them to GitHub, but you would first need to add an SSH key to your personal account if you have not already (you should not add an SSH key to a shared GitHub account). To view any changes made on your local machine, you would need to save your edits and refresh your browser. To synchronize any changes made on your local machine with GitHub, you would either need to share the repository with yourself and push or copy and paste your changes into GitHub's user interface.
```
$ git clone git@github.com:techcommons/Tech-Scholars.git
```

## Adding Any New Cohort
To add any new cohort to the website, start by duplicating an existing page into the appropriate directory. You can do this through GitHub's user interface by clicking into the "webdesign," "gamedesign," or "podcasting" folder. Then, press "Add file," click "Create new file," and name the file accordingly (e.g., summer2026.html). Copy and paste the HTML from another file located in the same folder into the file you have created and replace whatever necessary. Press "Commit changes..." to save the new file to GitHub.

Alternatively, you can do this on your local machine by moving into the correct directory within the cloned repository and making a new HTML file. Again, copy and paste the HTML from an existing page in the same directory, make any necessary changes, and commit and push your changes once you have finished. Terminal commands are shown below.

```
$ cd Tech-Scholars // this will move you into the site's directory
```
```
$ git pull // this will update your local repository with any remote changes
```
```
$ cd DIRECTORY // (e.g., cd webdesign) this will move you into your desired subdirectory
```
```
$ touch NAME.html // (e.g., touch summer2026.html) this will create a new file with its given name
```
```
$ open -e NAME.html // this will let you to edit the file
```
```
$ open NAME.html // this will let you view the file rendered in browser
```
```
$ git add NAME.html // this will add the new file to be committed
```
```
$ git commit -am "MESSAGE HERE" // this will create a new commit with your entered message
```
```
$ git push // this will push your changes to GitHub
```

When adding any new cohort to the website, be sure to update the navigation bar of every page. This includes the home page (index.html), the web design pages, the game design pages, and the podcasting pages (including podcasting/sources.html). You can copy the format of the current navbar as found in ```<div class="navbar">``` in any page. Commit and push your changes.

(1) A hypertext reference (href) includes ```DIRECTORY/``` before the name of the HTML file you are routing to when the file is located within a directory in the same location as the file you are editing (e.g., you are routing to a web design page from the home page). (2) An href includes ```../DIRECTORY/``` before the name of the file you are routing to when the file is located in a directory directly outside of where the file you are editing is located (e.g., you are routing to a web design page from a podcasting page). (3) Neither is needed when the file you are routing to is in the same location as the file you are editing (e.g., you are routing to a web design page from another web design page). Examples are shown below.
```
(1) <a href="webdesign/summer2025.html">Summer 2025</a>
```
```
(2) <a href="../webdesign/summer2025.html">Summer 2025</a>
```
```
(3) <a href="summer2025.html">Summer 2025</a>
```

## Adding a Web Design Cohort
Each link in a web design page is represented as an href attribute under the ```<div class="Webdeslist">``` element. Add or remove bullet points as necessary, and update the destination page and anchor text for each student. The format for a single bullet point is shown below. 
```
<li>
  <a href="DESTINATION LINK" target="_blank"><b>STUDENT NAME</b> - WEBSITE TITLE</a>
</li>
```
The links to the Tech Scholars' websites can be found in [CodeHS](codehs.com) (My Courses -> Cohort -> Roster -> Student -> Final Project -> Copy URL). Edit the name of the cohort directly above the ```<div class="Webdeslist">``` element. 

## Adding a Game Design Cohort
The video demo for each game should be uploaded directly to the GitHub repository in the "gamedesign" directory or to an external video hosting platform.

## Adding a Podcasting Cohort