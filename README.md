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
The video demo for each game should be uploaded directly to the GitHub repository in the "gamedesign" directory or to an external video hosting platform (e.g., YouTube). The demos from the Summer 2024 cohort are currently hosted on Glitch, which seems to be shutting down in the near future, so these demos may need to be relocated to an alternate site. You can edit the content for each game under the ```<div class="gamedesign">``` element (examples shown below) and the name of the cohort directly above it.
```
<h5>GAME NAME</h5>
<p>by STUDENT NAMES</p>
<video width="100%" height="100%" controls>
  <source src="ROUTE TO VIDEO" type="video/mp4"> // e.g., src="demo1.mp4"
Your browser does not support the video tag.
</video>
```
OR
```
<h5>GAME NAME</h5>
<p>by STUDENT NAMES</p>
<iframe width="100%" height="650"
  src="LINK TO VIDEO"> // e.g., src="https://www.youtube.com/embed/XXX">
</iframe>
```
Placeholder images should be similarly uploaded to the GitHub repository or an alternate site of your choice. Example formats are shown below.
```
<h5>GAME NAME</h5>
<p>by STUDENT NAMES</p>
<img src="ROUTE TO IMAGE" alt="ALTERNATE TEXT"> // e.g., src="image1.jpg"
```
OR
```
<h5>GAME NAME</h5>
<p>by STUDENT NAMES </p>
<img src="LINK TO IMAGE" alt= "ALTERNATE TEXT"> // e.g., src="https://XXX"
```
If you are uploading the files directly to GitHub, you may choose to create a folder for each cohort to store them in. In this case, be sure to include the name of the directory in the route to the video or image (e.g., ```src="summer2026/image1"```).

## Adding a Podcasting Cohort
The content for each podcast can be edited under the page's ```<div class="podcontent">``` elements. This includes the title, hosts, sources anchor, cover art, blurb, and audio recording for each podcast. The cover art and audio recordings must be uploaded to either the repository's "podcasting" directory or to an external platform, with the same guidelines from the Game Design section applying. The format for each podcast is shown below.
```
<div class="podcontent">
  <h5>PODCAST TITLE</h5>
  <p>Hosts: STUDENT NAMES | <a href="sources.html#ANCHOR">Sources</a></p>
  <img src="ROUTE OR LINK TO COVER ART" alt="ALTERNATE TEXT">
  <p>BLURB</p>
  <audio controls>
    <source src="ROUTE OR LINK TO AUDIO RECORDING" type="audio/TYPE">
    Your browser does not support the audio element.
  </audio>
</div>
```
Each podcast should be contained within its own ```<div class="podcontent">``` element so that it can be searched for independently from the other podcasts. The anchor in the sources link should uniquely match the anchor you give the podcast in the "sources.html" page. The sources for a new cohort can be added at the bottom of the existing "sources.html" page (but within the ```<div class="bodd">``` element) under its own heading. The correct format is shown below.
```
<h4 id="firstline">COHORT, <em>FEATURED EXHIBITION</em></h4>
<p>COHORT BLURB</p>

<h5 id="ANCHOR 1">PODCAST 1 TITLE</h5>
<p>SOURCE 1<a href="LINK TO SOURCE 1">LINK TO SOURCE 1</a></p>
<p>SOURCE 2<a href="LINK TO SOURCE 2">LINK TO SOURCE 2</a></p>
// et cetera

<h5 id="ANCHOR 2">PODCAST 2 TITLE</h5>
<p>SOURCE 1<a href="LINK TO SOURCE 1">LINK TO SOURCE 1</a></p>
<p>SOURCE 2<a href="LINK TO SOURCE 2">LINK TO SOURCE 2</a></p>
// et cetera

// et cetera
```
You can edit the title and blurb for the gallery page under the ```<div class="bodd">``` element in the appropriate ```<h4>``` and ```<p>``` tags.