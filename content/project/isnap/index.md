---
title: "iSnap: Data-driven Hints for Block-based Programming"
summary: iSnap supports students automatically with hints, feedback and self-explanations.
tags:
- Computing Education
- Educational Data Mining
- Hints
date: "2018-01-01T00:00:00Z"
authors:
- Thomas W. Price
- Samiha Marwan

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  # caption: Photo by rawpixel on Unsplash
  focal_point: Smart


links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
url_code: "https://github.com/thomaswp/iSnap"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

# Overview

[Snap](http://snap.berkeley.edu) is an online, bock-based programming environment designed by researchers at UC Berkeley to make programming more accessible to novices. iSnap augments the environment with intelligent features including logging and data-driven hints.

iSnap is a project out of the HINTS lab in collaboartion with the [Game2Learn](http://eliza.csc.ncsu.edu) lab at North Carolina State University, with lead development by [Thomas Price](go.ncsu.edu/twprice). A public mirror of iSnap is available on [GitHub](https://github.com/thomaswp/iSnap), but it may be behind the development branch demoed here until features are ready for release.

The iSnap project has also produced various papers and public datasets, which can be found [below](#datasets).

The construction of a Snap program and the corresponding evaluation.

### Data-driven Hints

<a name="hints" class="anchor"></a>

Using data collected from real students working on programming assignments, we are able to generate on-demand, next-step hints for students who get stuck on these assignments. The _SourceCheck_ algorithm matches students' code to previously observed code from students who successfully completed the assignment and recommends an edit based on how those students progressed.

<img src="error-check.png" class="gif" alt="Snap checking an error"/>

See an explanation of iSnap's help features below, or try them out yourself at the [iSnap demo](https://go.ncsu.edu/isnap). Select any assignment and test out the hints.

When a student needs help, they can ask iSnap to check their work. To start off, it shows two colors:

*   Blocks that are highlighted in <span style="border: 2px solid #ff00ff; padding:4px; font-weight: bold">magenta</span> probably don't belong in a solution.
*   Blocks that are highlighted in <span style="border: 2px solid #ffff00; padding:4px; font-weight: bold">yellow</span> probably do belong in the solution, but may not be in the right place.

Hovering over a yellow-highlighted block will show where it can be moved.

If a student requests a next-step hint, iSnap also adds:

*   Blue <span style="color: blue; font-weight: bold; border: solid blue 2px; padding: 0 5px">+</span> buttons and input outlines <span style="border: 2px solid blue; padding: 0 5px"> </span> indicating where new blocks can be inserted

Clicking a button or highlighted input will show a next-step hint, comparing a student's current code to iSnap's suggested code. If the suggestion is followed, the button or input outline disappears, indicating the student has successfully followed the hint.

#### Previous Version of iSnap Hints

The above demo shows off iSnap's newest hint interface, but much of the earlier research with iSnap used a simpler hint interface, based on the Contextual Tree Decomposition (CTD) algorithm. The assignment asks you to create a guessing game, in which the computer stores a random number and then repeated asks the player to guess it, telling them if they are too high, too low or correct.

<img class="gif" src="ask-hint.png" height="150px">

When a student is stuck, they can request a hint with the click of a button.

<img class="gif" src="get-script-hint.png" height="200px">

<img class="gif" src="get-block-hint.png" height="200px">

Students can request hints about whole scripts or individual blocks.

### Logging

<a name="logging" class="anchor"></a>

iSnap logs all actions taken by students in the environment, as well as snapshots of students' code as they work. Logs can be saved to a database for future analysis, review or grading.


**Note**: this is a demo site and does not include actual student data.

<img src="logging.png">

iSnap offers a basic interface to navigate and view the logs it generates.

