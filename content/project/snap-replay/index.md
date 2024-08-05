---
title: "In-IDE Programming Videos for True Active Learning Online"
summary: ''
date: 2023-08-15
authors:
  - admin
tags:
  - Curriculum
  - Block-based Programming
show_featured_image: false
---

Instructional videos are an important part of online learning that can support asynchronous courses, distance education, and -- in my case -- a flipped classroom, where students learn at home and then do hands-on labs in class when I can support them.

One challenge: videos can be pretty dull, and it's easy for students tune out. For programming in particular, [it's helpful for students to program alongside the instructor](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008090), as advocated for by [Software Carpentry](https://carpentries.org/).

After teaching during the pandemic, I set out to create a better form of online video that would be as effective as -- or maybe even more effective than -- a live classroom lecture. I wanted to create videos that would:
* Engage students in the most effective forms of learning, like actively answering questions and constructing their own knowledge.
* Prompt the student to explore and understand the code the instructor was sharing.
* Create the feeling of a 1-on-1 tutoring session, with the instructor right next to the student.
* Cover 100% of my introductory programming sequence, from loops to lists.


### Snap Videos

The results is Snap Videos, which isn't a video player at all. Rather, it's a way of recording and replaying instructional content *in the student's programming environment*!

For a student, the video plays almost like any other, with the instructor live coding. The difference is that any time a student wants to run, modify or explore the instructor's code, all they have to do is start editing it:

{{< video src="pause-edit.mp4" controls="yes" >}}

Notice that in the video that there are two cursors: the larger one is controlled by the instructor and moves as the "video" plays. The other is the student's, who pauses the video and then proceeds to edit for a bit, before starting the video again.

{{< button text="Try Snap Videos!" url="https://isnap.csc.ncsu.edu/public/snap-playback/" >}}

{{% callout note %}}
Snap Videos works best in Chrome. The videos are listed in the order I use them in class, and complement the [Bounce curriculum](../bounce/) well.
{{% /callout %}}


### Seamless Slides

Live coding is great, but sometimes there is information that is better communicated to the student using slides. Snap Videos uses [reveal.js](https://revealjs.com/) to seamlessly switch back and forth between slides and codes.

{{< figure src="slides.png" class="gif" >}}

The slide code is quite simple:

```markdown
## The Repeat Block

The `repeat ___` block repeats all actions inside of it, in order, a number of times.

![](img/repeatAB.png)

**Example**: *This code will say*: `ABABAB`.
```


### Active Learning

Pausing a video to edit the code is a neat trick, but without proper prompting, my research shows that students won't use it very often (we're just too used to sitting back and watching a video). Snap Videos includes 3 majors ways to prompt students to engage more deeply with the material.

#### Modify Questions

As an instructor, my favorite feature of Snap Videos is the *modify questions* (named for the "modify" step of the [Use, Modify, Create framework](https://dl.acm.org/doi/10.1145/3304221.3319786)). The instructor asks the student to update some existing code that they have created during live coding.

Because the video is taking place in the student's editor, the student already has the instructor's starting code and just heard the instructor's explanation of it. The student just has to modify it.

{{< figure src="modify.png" >}}

The student can check whether their output matches a correct solution before proceeding, and optionally watch the instructor walk through the solution.

This programming practice, immediately following learning a concept, is a great way to cement learning, and it's something I do in my live lectures as well.

{{< figure src="modify-check.png" >}}

(My Ph.D. students and I have explored [auto-grading in Snap](https://dl.acm.org/doi/10.1145/3430665.3456367), but to make the authoring burden lower, I decided to allow students to check their own work - few seem to abuse that power.)


#### Pause and Reflect

A more informal way to prompt students to explore the code is with pause and reflect questions. In these, the instructor asks the student to make a prediction before code is run, writing that prediction into a box. The student can then run the code to check their work, and continue the video for an explanation. Making predictions is a powerful tool for learning because it engages the learner to make sense of what they've learned and test their mental model of the concept.

#### Multiple-choice Comprehension Questions

The instructor can also insert basic multiple-choice questions, which the student has to answer correctly before proceeding.

{{< figure src="mcq.png" >}}

These questions are built in reveal.js as well - the instructor just has to add a little HTML markup to give the slide an ID (`q1`), so Snap Videos knows to treat it accordingly.

```markdown
---
<!-- .slide: id="q1" -->
## Knowledge Check: Repeat
What will the following code say when it runs?

<div class="container">
<div class="col">
![](img/q1.png)
</div>

<div class="col quiz">
[A) One Two Three Four](#/a)
[B) One Two Three Four One Two Three Four](#/b)
[C) One Two Two Three Three Four](#/c)
[D) One Two Three Two Three Four](#/d)
</div>
</div>
```

If a student chooses an incorrect answer, the instructor can provide an explanation on the relevant slide.

{{< figure src="mcq-hint.png" >}}

### Student Impact

I've been using Snap Videos in my class (and a colleague's section) for a few years now, and students have received the videos very well. Praise for the videos often shows up unprompted in end-of-semester evaluations. For example:

> The interactive videos for homework were very helpful, and this class is one of the few I think that truly benefit from the 'flipped classroom'.

### Recording

Recording is about as simple in Snap Videos as it is for any other screen-recorded lecture. After making slides in reveal.js, the instructor simply walks through their lecture. In recording mode, Snap Videos adds a few buttons to trigger Pause-and-Reflect, control slides (minimizing, maximizing, advancing), trigger modify or MCQ questions, and to mark the end of a modify question explanation.

Afterwards, Snap Videos downloads the audio and .json files that define a video, which can be uploaded to the video server (or controlled with Git, as I prefer to do).

### Under the Hood

So how does it work? Making something like this for textual programming isn't so hard, and in fact [Khan Academy already does it](https://www.khanacademy.org/computing/computer-programming/programming/drawing-basics/pt/making-drawings-with-code).

But doing this with a block-based programming environment like Snap<em>!</em> is much harder. In textual code, we can simply replay the state of a text box, but with Snap, I had to make a way to record each action the instructor took and replay them accurately.

This ended up being much more challenging that I imagined. Getting basic replay functionality worked pretty quickly. But making everything work, from custom blocks to lists, in the end required me to create custom recording and replay logic for 60 in-editor actions!

Additionally, playing those actions forward is one thing, but how about playing them backwards? It turned out to be much easier to allow backward scrubbing by restarting the video, and then rapidly playing it again from the video in a few seconds.

If I were to start this project over, I would likely opt for a hybrid model, recording a real video while also taking regular snapshots of code behind the scenes. This would allow the student to load from any point in the video, and do active learning exercises, without having to support full replayability.