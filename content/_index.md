---
title: 'Home'
date: 2023-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  # - block: about.avatar
  #   id: about
  #   content:
  #     username: admin
  #     text: Hello
  - block: hero
    content:
      title: Thomas W. Price
      text: Teaching Innovations Portfolio
      primary_action:
        text: See Projects
        url: project/
        icon: academic-cap
      secondary_action:
        text: Resume
        url: https://docs.hugoblox.com
    design:
      spacing:
        padding: [0, 0, 0, 0]
        margin: [0, 0, 0, 0]
      # For full-screen, add `min-h-screen` below
      css_class: "dark"
      background:
        color: "navy"
        image:
          # Add your image background to `assets/media/`.
          filename: bg-triangles.svg
          filters:
            brightness: 0.5
  - block: cta-image-paragraph
    id: philosophy
    content:
      items:
        - title: Hi, I'm Thomas
          text: I work to reimagine the way that people learn to program. What if learning to program meant...
          feature_icon: chevron-double-right
          features:
            - Expressing ourselves,
            - Connecting with our interests, and
            - Acting on our values?
          # Upload image to `assets/media/` and reference the filename here
          image: build-website.png
        - title: Making Games
          text: My "Bounce!" curriculum covers all the basics of programming by making a popular casual game.
          feature_icon: play
          features:
            - Lessons cover loops, variables, functions and conditionals.
            - Students write almost 100% of the code, so they own their work.
            - Final game looks polished and professional, in just 4 lessons.
          # Upload image to `assets/media/` and reference the filename here
          image: build-website.png
          button:
            text: Check it out
            url: project/bounce/
        - title: Making Simulations
          text: I extended a popular novice programming environment with a Physics API allowing for easy simulations.
          feature_icon: rocket-launch
          features:
            - Jump straight into exploration and skip the set-up.
            - Learn how planets orbit, or make a physics-based game.
          # Upload image to `assets/media/` and reference the filename here
          image: coffee.jpg
          button:
            text: Check it out
            url: project/snap-games
        - title: Making Music
          text: TraceNote lets students learn to trace code intuitively by playing music.
          feature_icon: musical-note
          features:
            - Learn the fundamental CS skill of code tracing.
            - No numbers or math - just music!
            - Build an intuitive understanding of code before a class.
          # Upload image to `assets/media/` and reference the filename here
          image: coffee.jpg
          button:
            text: Check it out
            url: project/tracenote
        - title: Making a Difference
          text: In my Machine Learning class, students solved a real-world problem for the NC State Climate Office to identify erroneous instrument readings.
          feature_icon: globe-alt
          features:
            - A real dataset with 500M+ and heavy class imbalance.
            - Students competed on a leaderboard to build the best model.
            - The winners were hired to build a production model.
          image: coffee.jpg
          button:
            text: Check it out
            url: project/tracenote
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-900"
  - block: markdown
    content:
      title: Learning creatively, Learning effectively
      text: I build innovations that motivate students and support their learning as they tackle complex projects.
  - block: cta-image-paragraph
    id: support
    content:
      items:
        - title: Interactive Lectures in the IDE
          text: I developed a novel way to deliver short lectures *in the student's programming environment*.
          feature_icon: code-bracket-square
          features:
            - Pause at any point and edit the code
            - Mini coding assigmnets embeeded in the lecture
            - Comprehension questions keep students engaged
          # Upload image to `assets/media/` and reference the filename here
          image: build-website.png
        - title: Automated Hints and Feedback
          text: I developed data-driven hints and feedback that support students when they get stuck, using data from prior students.
          feature_icon: star
          features:
            - Pause at any point and edit the code
            - Mini coding assigmnets embeeded in the lecture
            - Comprehension questions keep students engaged
          image: build-website.png
          button:
            text: Check it out
            url: project/isnap
        - title: Code that Explains Itself
          text: I created a code visualization tool that directly links each line of code students write to output they see.
          feature_icon: play-circle
          features:
            - Visualize iteration, even with complex nested loops
            - See how variables changes throughout execution
            - Easily debug issues in your code
          image: build-website.png
          button:
            text: Check it out
            url: project/explainable
        - title: Learn Program Design
          text: Jigsaw lets students learn to design a function before they write code to implement it, so they can focus on learning important programming design patterns.
          feature_icon: puzzle-piece
          features:
            - Compose solutions out of common code "recipes"
            - Visualize how code executes with different inputs
            - Use your design to solve the problem with code
          image: build-website.png
          button:
            text: Check it out
            url: project/jigsaw
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-900"
  - block: testimonials
    content:
      title: "Student course evaluation comments"
      text: ""
      items:
        - name: "Undergraduate student, Computer Science Principles"
          text: Dr. Price was always prepared for class with a presentation, Tophat, and usually lab activity... The interactive videos for homework were very helpful, and this class is one of the few I think that truly benefit from the `flipped classroom'.
        - name: "Graduate student, Automated Learning and Data Analysis"
          # Upload image to `assets/media/` and reference the filename here
          # image: "testimonial-1.jpg"
          text: "Truly, Dr. Price is the best educator I have had in my three years here at NCSU."
        - name: "Undergraduate student, Automated Learning and Data Analysis"
          text: One of the strongest teachers I've ever had. He's consistently prepared for class with in-depth knowledge about every subject we cover...  If you have a system where teachers train other teachers, letting Dr. Price run that would be a great idea.
    design:
      spacing:
        # Reduce bottom spacing so the testimonial appears vertically centered between sections
        padding: ["6rem", 0, 0, 0]
  
  - block: stats
    content:
      items:
        - statistic: "1M+"
          description: |
            Websites built  
            with Hugo Blox
        - statistic: "10k+"
          description: |
            GitHub stars  
            since 2016
        - statistic: "3k+"
          description: |
            Discord community  
            for support
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-900"
      # Reduce spacing
      spacing:
        padding: ["1rem", 0, "1rem", 0]
  - block: features
    id: features
    content:
      title: Features
      text: Build your site with blocks 🧱
      items:
        - name: Optimized SEO
          icon: magnifying-glass
          description: Automatic sitemaps, RSS feeds, and rich metadata take the pain out of SEO and syndication.
        - name: Fast
          icon: bolt
          description: Super fast page load with Tailwind CSS and super fast site building with Hugo.
        - name: Easy
          icon: sparkles
          description: One-click deployment to GitHub Pages. Have your new website live within 5 minutes!
        - name: No-Code
          icon: code-bracket
          description: Edit and design your site just using rich text (Markdown) and configurable YAML parameters.
        - name: Highly Rated
          icon: star
          description: Rated 5-stars by the community.
        - name: Swappable Blocks
          icon: rectangle-group
          description: Build your pages with blocks - no coding required!
  - block: cta-card
    content:
      title: Build your future-proof website
      text: As easy as 1, 2, 3!
      button:
        text: Get Started
        url: https://hugoblox.com/templates/
    design:
      card:
        # Card background color (CSS class)
        css_class: "bg-primary-700"
        css_style: ""
---
