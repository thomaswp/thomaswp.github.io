---
title: "TraceNote: Learn Code Tracing by Playing Music"
summary: ''
date: 2023-09-28
authors:
  - admin
tags:
  - Learning Tools
---

Code tracing is the ability to read code, understand how the program flows and variable values change, and predict program output. It is a critical skill that supports students' ability to write code.

It makes sense -- we teach students how to read *natural* language before we teach them to write. Why shouldn't it be the same for code?

But there's a big challenge to teaching code tracing: It's *tedious* for students, requiring them to carefully track variable values, and repeat the process until they build fluency.

What if students could learn to trace code in a way that was fun, and made it easy to build intuitive fluency in this critical skill?

### TraceNote

That's where TraceNote comes in. TraceNote is a demo I built to explore the question of how students could learn to trace code by playing music. In TraceNote, students learn to trace a simplified programming language that represents music. Students trace the program, and when it says to play a note, students play that note, using a gamepad or keyboard. Students can only play the correct next note in the tune if they've correctly traced the program so far.

Students don't have to know anything about musical notation. TraceNote uses arrows to represent notes, so playing {{< icon name=arrow-right >}} {{< icon name=arrow-down-right >}} and {{< icon name=arrow-down >}} will play three ascending notes in the tune's key. Here's a very simple example (sound on!).

{{< video src="basic.mp4" controls="yes" >}}

{{< button text="Try the TraceNote Demo" url="https://thomaswp.github.io/TraceNote/" >}}

{{% callout note %}}
TraceNote is still a demo, so there's no tutorial. You can select a tune to plan in the menu to the left, then press "Play" to hear it or "Start" to trace it. Use a gamepad or your keyboard arrow key to indicate what note you think comes next, and then press space to test if you're correct. You can press Stop if you want to stop or change songs.
{{% /callout %}}

Students can trace the code themselves, or see a worked example as the computer plays through it. If students get lost while tracing, or make a mistake, they can *retrace* their steps and try again.

{{< video src="error.mp4" controls="yes" >}}

### Iteration

We can easily introduce fundamental programming concepts, like iteration, with a small modification to the traced code.

{{< video src="repeat.mp4" controls="yes" >}}

### Variables

Tracing the value of variables is a key skill for novice programmers. Trace tables, where students keep track of the value of each variable as they walk through a program's execution, are a great way to do this... but they're also quite tedious for the student. In TraceNote, the trace table is automatically updated, but only *after* a student gets the next note right. This way, the student only has to keep track of variable changes since the last note in their heads -- the computer keeps track of the rest.

In TraceNote, we can indicate that a variable in incremented ⭮ or decremented ⟲ with the same rotational notation.

{{< video src="variables.mp4" controls="yes" >}}

### Functions and Lists

We can even introduce more advanced concepts like functions and lists!

In music, there are many common sequences of notes, like arpeggios, that start on a root note and then play a series of notes relative to it. Some of these "functions" are universal, and some are specific to a song.

{{< video src="functions.mp4" controls="yes" >}}

Lists represent an important challenge for code tracing. They can also represent sequences of musical notes that can be reused or modified.

{{< video src="lists.mp4" controls="yes" >}}

### Complex Tunes

Putting it all together, we can create "programs" for complex tunes, that the student can enjoy playing once they've gained fluency tracing code!

{{< video src="tune.mp4" controls="yes" >}}

### Implementation

TraceNote was built in TypeScript and features its own internal interpreter. Constructing a level means building the abstract syntax tree (AST) for that level. The code to construct the Arpeggio level above to teach functions looks like this:

```typescript
levels.push(new class extends Level {

    name = "Many Arpeggio";
    category = "Functions";
    arp = 'Arpeggio'

    override getMain(): Block {
        return new Block()
            .addCommand(new FunctionCall(this.arp, new Literal(1)))
            .addCommand(new FunctionCall(this.arp, new Literal(2)))
            .addCommand(new FunctionCall(this.arp, new Literal(3)))
            .addCommand(new FunctionCall(this.arp, new Literal(4)))
    }

    override addFunctions(program: Program) {
        program.functions.push(new FunctionDefinition(this.arp, [Note1Var], new Block()
            .addCommand(new Pick(new GetVariable(Note1Var)))
            .addCommand(new ChangeVariable(Note1Var, new Literal(2)))
            .addCommand(new Pick(new GetVariable(Note1Var)))
            .addCommand(new ChangeVariable(Note1Var, new Literal(2)))
            .addCommand(new Pick(new GetVariable(Note1Var)))
            .addCommand(new ChangeVariable(Note1Var, new Literal(3)))
            .addCommand(new Pick(new GetVariable(Note1Var)))
        ))
    }
});
```

{{< button text="Try the TraceNote Demo" url="https://thomaswp.github.io/TraceNote/" >}}


