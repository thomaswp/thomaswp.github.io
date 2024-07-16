---
title: 'Home'
date: 2023-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: hero
    content:
      title: Thomas W. Price
      text: Educations Innovations Portfolio
      # primary_action:
      #   text: Resume
      #   url: uploads/resume.pdf
      #   icon: document-arrow-down
      secondary_action:
        text: Contact
        url: /#contact
        icon: envelope
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
        - title: Hi, I'm Thomas 👋
          text: "I build educational products that **reimagine the way that people learn to program** so they can:"
          feature_icon: chevron-double-right
          features:
            - Express themselves and their values with programming.
            - Build an intuitive understanding of concepts quickly.
            - Benefit from cutting edge, evidence-based learning support.
          # Upload image to `assets/media/` and reference the filename here
          image: cta/thomas.jpg
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-900"
      spacing:
        padding: ["1rem", 0, "1rem", 0]
  - block: markdown
    id: teaching
    content:
      title: Teaching Innovations
      text: >
        I design curricula and tools that make learning programming engaging and authentic, like the examples below!
        {{< icon name="chevron-double-down" >}} {{< icon name="chevron-double-down" >}}
    design:
      spacing:
        padding: ["5rem", 0, "5rem", 0]
  - block: cta-image-paragraph
    content:
      items:
        - title: Making Games
          text: My "Bounce!" curriculum covers all the basics of programming by making a popular casual game.
          feature_icon: play
          features:
            - Lessons cover loops, variables, functions and conditionals.
            - Students write almost 100% of the code, so they own their work.
            - Final game looks polished and professional, in just 4 lessons.
          # Upload image to `assets/media/` and reference the filename here
          image: cta/bounce.png
          button:
            text: Learn more
            url: project/bounce/
        - title: Making Simulations
          text: I extended a popular novice programming environment with a Physics API allowing for easy simulations.
          feature_icon: rocket-launch
          features:
            - Jump straight into exploration and skip the set-up.
            - Learn how planets orbit, or make a physics-based game.
          # Upload image to `assets/media/` and reference the filename here
          image: cta/physics.png
          button:
            text: Learn more
            url: project/snap-games/
        - title: Making Music
          text: TraceNote lets students learn to trace code intuitively by playing music.
          feature_icon: musical-note
          features:
            - Learn the fundamental CS skill of code tracing.
            - No numbers or math - just music!
            - Build an intuitive understanding of code before a class.
          # Upload image to `assets/media/` and reference the filename here
          image: cta/tracenote.png
          button:
            text: Learn more
            url: project/tracenote
        - title: Making a Difference
          text: In my Machine Learning class, students solved a real-world problem for the NC State Climate Office to identify erroneous instrument readings.
          feature_icon: globe-alt
          features:
            - A real dataset with 8M+ instances and heavy class imbalance.
            - Students competed on a leaderboard to build the best model.
            - The winners were hired to build a production model.
          image: cta/econet.png
          button:
            text: Learn more
            url: project/econet
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-900"
  - block: markdown
    id: tech
    content:
      title: Learning creatively. Learning effectively.
      text: I build innovations that motivate students and support their learning as they tackle complex projects.
    design:
      spacing:
        padding: ["5rem", 0, "5rem", 0]
  - block: cta-image-paragraph
    id: support
    content:
      items:
        - title: Interactive Lectures in the IDE
          text: I developed a novel way to deliver short lectures *in the student's programming environment*.
          feature_icon: code-bracket-square
          features:
            - Pause at any point and edit the code.
            - Mini coding assigmnets embeeded in the lecture.
            - Comprehension questions keep students engaged.
          # Upload image to `assets/media/` and reference the filename here
          image: cta/videos.png
          button:
            text: Learn more
            url: project/snap-replay/
        - title: Automated Hints and Feedback
          text: I developed data-driven hints and feedback that support students when they get stuck, using data from prior students.
          feature_icon: star
          features:
            - Pause at any point and edit the code.
            - Mini coding assigmnets embeeded in the lecture.
            - Comprehension questions keep students engaged.
          image: cta/isnap.png
          button:
            text: Learn more
            url: project/isnap
        - title: Code that Explains Itself
          text: I created a code visualization tool that directly links each line of code students write to output they see.
          feature_icon: play-circle
          features:
            - Visualize iteration, even with complex nested loops.
            - See how variables changes throughout execution.
            - Easily debug issues in your code.
          image: cta/explainable.png
          button:
            text: Learn more
            url: project/explainable
        - title: Adaptive A/B Testing to Improve Learning
          text: "My team won the <ins>[$1M XPRIZE Digital Learning Challenge](https://www.xprize.org/challenge/digitallearning/articles/xprize-and-the-institute-of-education-sciences-announce-winners-of-1m-digital-learning-challenge)</ins> to modernize the use of
          experimentation in education."
          feature_icon: adjustments-horizontal
          features:
            - A/B testing reveals effective instructional design.
            - Adaptive experimentation maximizes student benefit.
            - Supports personalized learning at scale.
          image: cta/ab-testing.jpg
          button:
            text: Learn more
            url: project/ab-testing
        - title: Learning Program Design
          text: Jigsaw lets students design a function before they write code to implement it, so they can focus on learning important programming design patterns.
          feature_icon: puzzle-piece
          features:
            - Compose solutions out of common code "patterns" like `filter`.
            - Visualize how code executes with different inputs.
            - Use your design to solve the problem with code.
          image: cta/jigsaw.png
          button:
            text: Learn more
            url: project/jigsaw
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-900"

  - block: stats
    id: outcomes
    content:
      items:
        - statistic: "$4.8M+"
          description: |
            Grant funding
            to support my work
        - statistic: "65+"
          description: |
            Peer-reviewed papers
            on education innovation
        - statistic: "5k+"
          description: |
            Students impacted
            by my work
    design:
      spacing:
        padding: ["2rem", 0, "2rem", 0]
  - block: features
    id: expertise
    content:
      title: Expertise
      text: I bring core capabilities to my work to create high-impact educational innovations.
      items:
        - name: Full-service Problem Solving
          icon: light-bulb
          description: I wear all the hats -- need finding, ideation, design, prototyping, user testing, deployment and evaluation.
        - name: Evidence-based Practices
          icon: magnifying-glass
          description: I build on research to create innovations with real, measuable learning and engagement.
        - name: Rapid Prototyping and Iteration
          icon: bolt
          description: I go from an idea to a fully-interactive prototype quickly, and pivot when ideas don't work.
        - name: A/B Testing and Experimentation
          icon: adjustments-horizontal
          description: I use experiments to compare ideas and make data-backed design choices that *work*.
        - name: User Testing
          icon: user-group
          description: I run detailed user testing to understand learners' mental models and extract design insight.
        - name: Technical Innovation
          icon: code-bracket
          description: I've made <ins>[custom interpreters](project/tracenote/)</ins>, <ins>[redesigned IDEs](project/snap-replay/)</ins>, and built <ins>[data-driven models](project/isnap/)</ins> -- whatever innovation I needed to build the best learning experience.
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-900"
      # Reduce spacing
      spacing:
        padding: ["0rem", 0, "0rem", 0]
  - block: testimonials
    content:
      title: "Student Feedback"
      text: ""
      items:
        - name: "Undergraduate student, Computer Science Principles"
          text: Dr. Price was always prepared for class with a presentation, Tophat, and usually lab activity... The interactive videos for homework were very helpful, and this class is one of the few I think that truly benefit from the 'flipped classroom'.
        - name: "Graduate student, Automated Learning and Data Analysis"
          # Upload image to `assets/media/` and reference the filename here
          # image: "testimonial-1.jpg"
          text: "Dr. Price was respectful to students throughout the course and always looking for feedback. He excelled in translating very difficult to understand topics of machine learning into easily understandable presentations even for students not of a machine learning background. His PowerPoints were extraordinarily clear and well created and care in every aspect of the course was shown."
        - name: "Undergraduate student, Automated Learning and Data Analysis"
          text: One of the strongest teachers I've ever had. He's consistently prepared for class with in-depth knowledge about every subject we cover...  If you have a system where teachers train other teachers, letting Dr. Price run that would be a great idea.
    design:
      spacing:
        # Reduce bottom spacing so the testimonial appears vertically centered between sections
        padding: ["0rem", 0, 0, 0]
  # - block: cta-card
  #   id: contact
  #   content:
  #     title: Contact
  #     text: If you want to work with me, get in touch!
  #     button:
  #       text: Contact
  #       url: contact/ # TODO!!
  #   design:
  #     card:
  #       # Card background color (CSS class)
  #       css_class: "bg-primary-700"
  #       css_style: ""
  - block: resume-biography
    id: contact
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: >
        Reach out by [Email](mailto:twprice@ncsu.edu) or [LinkedIn](https://www.linkedin.com/in/thomas-w-price/) if you'd like to discuss a collaboration!
      # Show a call-to-action button under your biography? (optional)
      # button:
      #   text: Download Resume
      #   url: uploads/resume.pdf
    design:
      # css_class: dark
      css_class: "bg-gray-100 dark:bg-gray-900"
      spacing:
        padding: ["1.5rem", 0, "3rem", 0]
      # background:
      #   color: black
        # image:
        #   # Add your image background to `assets/media/`.
        #   filename: bg-triangles.svg
        #   filters:
        #     brightness: 1.0
        #   size: cover
        #   position: center
        #   parallax: false
---
