---
title: "Extending Block-based Programming with Physics!"
summary: ''
date: 2023-08-15
authors:
  - admin
tags:
  - Curriculum
  - Block-based Programming
show_featured_image: false
---

Snap<em>!</em> is a block-based programming language that lets students create expressive apps and simulations easily. This is especially powerful for non-Computer-Science majors, like those in my introductory course, who may want to apply programming to solve problems in their own domains.

I built this extension to Snap<em>!</em> to allow students to make accurate physics simulations and physics-based games. Making more advanced products can motivate students to learn programming, while also building an intuitive understanding of physics.

### Science Simulations

For example, a simple program can help students understand how the orbit of a planet is affected by its starting speed.

{{<figure src="orbit.png" class="gif" >}}

{{< button text="Try the Orbit Demo" url="https://isnap.csc.ncsu.edu/public/snap-games/snap.html#present:Username=thomaswprice&ProjectName=Solar%20Sim" >}}

{{% callout note %}}
If you want to see the code for any linked demo, press the {{< icon name="arrows-pointing-in" >}} button to exit full screen mode.
{{% /callout %}}

The code itself is straightforward to read and edit.

{{<figure src="orbit-code.png" >}}


By modifying 2 lines of code, students can experiment with escape velocity to build an intuitive understanding of it.

{{<figure src="escape.png" class="gif" >}}

### Open-ended Exploration

The physics engine, based on [matter.js](https://brm.io/matter-js/), is quite flexible, and allows students to create open-ended simulations. The extension takes care of the hard parts, like creating bounding boxes, so students can focus on their code.

{{<figure src="physics.png" class="gif" >}}

{{< button text="Try the Shapes Demo" url="https://isnap.csc.ncsu.edu/public/snap-games/snap.html#present:Username=thomaswprice&ProjectName=shapes!" >}}

### Physics-based Games

In my introductory programming class, students make an open-ended project that connects to their interests and addresses a problem they see in the world. Many create games, including fun and serious games. By leveraging physics, students can create more powerful games, like what they see on their phones and in their browsers.

My extension also adds camera controls and the ability to save and load levels, which allows Snap<em>!</em> to make far more advanced games than would otherwise be possible -- like this this Angry Birds inspired app!

{{<figure src="games.png" class="gif" >}}

{{< button text="Try the Angry Birds Demo" url="https://isnap.csc.ncsu.edu/public/snap-games/snap.html#present:Username=thomaswprice&ProjectName=Angry%20Brids%20Demo" >}}
