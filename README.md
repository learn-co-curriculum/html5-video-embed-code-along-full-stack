# HTML5 Video Embed Code Along

## Objectives

1. Create an HTML5 Video element 

## Introduction

In this exercise you will code along with the video to review the HTML fundamentals you were introduced to in the previous lessons.

## Instructions

- Fork this repository on Github.
- Use Terminal to clone your forked copy.
- Then change directory into the repository folder.
- Code along with the provided video below and/or its supplementary reading located below the video. Code everything you see there. Feel free to stop, pause, rewind or fast forward through the content to keep pace.

*Note: In the video below at one point I will download source videos from [http://archive.org](http://archive.org), you can instead download the videos directly from the links provided below the video (to save time) instead. After downloading the videos from the direct links below, you will need to move them into a videos folder within this exercise, then you can skip to 4:30:00 in the video. This will also save you some time. The full instructions for moving the videos to the correct folder is listed below in the written instructions if you get stuck. Good luck!*

<iframe width="640" height="480" src="//www.youtube.com/embed/ymUxDt_mOxU?rel=0" frameborder="0" allowfullscreen></iframe>

[Click here to get the MP4 video linked to in the exercise](http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/real-estate.mp4)

[Click here to get the OGV video linked to in the exercise](http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/real-estate.ogv)

### Adding An HTML5 Video Player

In Terminal create a new feature branch called "promo-media" by typing `git checkout -b promo-media` and press return.

Next create an empty folder to place the videos inside of by typing  `mkdir videos` and press return.

At this point in the video above, I headed to [http://archive.org](http://archive.org) to download some place filler video. To save time you can download the videos from the links provided just below the video lecture above.

After downloading both videos let's move them into your "/videos" folder within this exercise so we can link to them in our HTML. Assuming your on Mac and your video files were downloaded to your "/Downloads folder" then, in Terminal type `mv ~/Downloads/real-estate.mp4 ~/Development/html5-video-embed-code-along-green-onion-<your-batch-name-here>/videos` and press return. Here you are replacing <your-batch-name-here> with the same name that matches the folder name you forked and cloned for this exercise. Then repeat on the other video `mv ~/Downloads/real-estate.ogv ~/Development/html5-video-embed-code-along-green-onion-<your-batch-name-here>/videos`. Your folder structure might be different especially if your on PC (Windows) instead of Mac. If your not sure exactly the location you can use Finder (Mac) or File Browser (Windows) to search for the files and drag and drop them into the videos folder for this exercises project folder.

To ove our files in Terminal we used the "mv" move command to move the downloaded videos from the folder where they have been downloaded into our project folder for this exercise. This command accepts two arguments the first is the location of the files we wish to move and the second argument is the location we are moving the files to. The arguments are simply separated by a keyboard space.

Now that our video files have been moved to our videos folder we want to bring up the index.html page in our code editor. At the very end of the page just below our `<p>` paragraphs, we are going to write a comment `<!-- promo video -->` and insert our `<video>` element like so,

```html
<!-- promo video -->
<video>...</video>
```

Inside the opening "video" tag let's add an attribute "controls" this will tell the browser to show the video player controls when the page loads.

```html
<!-- promo video -->
<video controls>
  ...
</video>
```

Next we need to provide the different video source files so that different browsers can load the video format that they prefer

```html
<!-- promo video -->
<video controls>
  <source src="videos/real-estate.mp4" type="video/mp4">
  <source src="videos/real-estate.ogv" type="video/ogg">
</video>
```

Inside our `<source>` elements we provide two arguments the first `src` tells the browser the relative path to the video file, the second `type` tells the browser the format of the video. Some browsers read the mp4 others webm or ogg format. For greater details on acepted video formats you can refer back to the prior lesson.

We also want to add some fallback support for older browsers that may not support the HTML5 video element. We do this by adding some instructions to update their browser below our source elements.

```html
<!-- promo video -->
<video controls>
  <source src="videos/real-estate.mp4" type="video/mp4">
  <source src="videos/real-estate.ogv" type="video/ogg">
  Your browser does not support HTML5 video. <a href="http://browsehappy.com/?locale=en" target="_blank">Please upgrade your browser</a>.
</video>
```

Save the file and preview in your browser the video should appear looking something like this,

<video controls>
  <source src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/real-estate.mp4" type="video/mp4">
  <source src="http://ironboard-curriculum-content.s3.amazonaws.com/front-end/lab-assets/real-estate.ogv" type="video/ogg">
  Your browser does not support HTML5 video. <a href="http://browsehappy.com/?locale=en" target="_blank">Please upgrade your browser</a>.
</video>

Looks good! Now we are ready to stage and commit our changes. Back in Terminal type `git add .` and press return. Then type 'git commit -m "add promo video to about page"' and press return. The push up your feature branch by typing `git push origin -u promo-media` and press return. Since we want to keep our work we can add it to our master branch. Type `git checkout master` and press return. Then type `git merge promo-media` and press return. Then push up the master branch by typing `git push origin master` and press return. Woot! all done.

After you finish, make sure you <a href="https://www.mozilla.org/en-US/firefox/new/" target="_blank">install Firefox</a> if you haven't already as it is required for the screenshot tests to run. Then, type `learn` command from Terminal to run local tests (Mac) or type `learn-test` for Windows.

After all tests are passing submit a pull request on Github and move on to the next lesson!

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/html5-video-embed-code-along' title='HTML5 Video Embed Code-Along'>HTML5 Video Embed Code-Along</a> on Learn.co and start learning to code for free.</p>
