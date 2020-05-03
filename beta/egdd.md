# Asymptotic Explorer 

## Elevator Pitch

An interactive website that gives a semi-technical introduction to how asymptotic analysis (Big O notation) is used in the context of analyzing algorithms. Nothing like this currently exists online, and there is an established learning need for CS students to learn Big O notation; so this would be a fruitful venture.

This is why I'm asking for a small seed investment of 2 million dollars.

## Influences (Brief)

- *3Blue1Brown*:
  - Medium: Video
  - Explanation: 3B1Bs videos have an an emphasis on storytelling. His way of tackling this complex math problems and clearly defining the problem and "next steps" makes you feel like you could have derived complex things on your own.
  - https://www.youtube.com/watch?v=OkmNXy7er84
- https://explorabl.es/:
  - Medium: *Games*
  - Explanation: I like the way many of these "explorable explanations" are formatted. The way I see it, it's moreso like a textbook chapter but with friendlier prose and lots of interactive examples in the place of where figures would be.
- These French Quantum Physics Videos:
  - Medium: *Video*
  - Explanation: I really dig the minimalist graphical aesthetics and sound design in these videos for some reason. I think it'll fit the theme of the game well.
  - https://www.youtube.com/watch?v=DC0U5viudt0

## Core Gameplay Mechanics (Brief)

Gameplay is a strong word, its more-so having a bunch of sliders and knobs you can twiddle and tweak to see how these various components interact. This is further detailed below but using the mouse the learners will be able to

- Drag and drop items in order
- Drag sliders that represent dynamic variables

# Learning Aspects

## Learning Domains

- Asymptotic Analysis/Big O Notation
  - In the context of algorithm analysis

## Target Audiences

While I am making this specifically for CISC320, I hope that it is also useful for curious individuals interested in the mathematical formalism behind algorithm analysis.

## Target Contexts

This is designed to be a public website that can be accessed whenever. It can be used as a supplement for an algorithms course, but can also be consumed standalone.

It's format suits itself to be played individually and in one sitting.

## Learning Objectives
- Explain why Algorithms are best *generally* described using limiting behavior rather than other metrics
- Describe when asymptotic analysis is *not* useful 
- Formally define Big O, Omega, and Theta 
- Given polynomial/exponential functions f(x) and g(x), Formally prove that function f(x) is:
  - O(g(x))
  - Ω(g(x))
  - Θ(g(x))
  - All by finding the appropriate constants and values of N

## Prerequisite Knowledge

- Basic familiarity with high school algebra
- Basic knowledge of how a program takes in input of various size and acts on that data

## Assessment Measures
As we discussed, it's probably going to be a canvas quiz of some sorts. The original Big O quiz can serve as our pre-test.

Some example questions (not final or complete in any means)

**Prove Big O Relations**

Pretty much identical to what you gave on the quiz.

**Select all that apply type question**

f(x) = n^3-10n

  - O(2^n)
  - O(n^3)
  - Ω(n)
  - Ω(n^3)
  - Θ(n^3)

**When not to use Big O**

Give some general reasons why an algorithm in a "slower" complexity class might be better to use in practice than one in a "faster" complexity class.


# What sets this project apart?

- I have yet to see a nice interactive that deals with Big O notation. A lot of the online resources I see are static websites or videos
- As shown, we have a learning need for proving Big O notation.
- Computer Scientists are scared of math, and this experience will hopefully ease this transition


# Player Interaction Patterns and Modes

## Player Interaction Pattern

This is a single player game that will orginize itself into sections containing prose and interactive objects. In order to go on to the next section, the learner will have to complete a given interactions (Think minigames).

I'm taking a different approach to this compared to a traditional game, so I hope deviating from the template EGDD will be okay. 

Here's the situation, we know that :

- This is *hopefully* going to be a real world intervention
- Our target audience being anxious CS upperclassmen who already have too much on their plate
- The subject material doesn't lend itself well for gameification.

Therefore, I'm going to make this more of an *explorable explanation*. Like a lecture, or a really conversational textbook. There will be short, interactive portions interspersed with the prose. Fun gameplay really isn't really the goal here; more so interesting an engaging learning. 

So I'm going to break from the template a little and dump the main narrative and gameplay mechanics in one section.

1. Introduction
    - The Big Question: How do we compare algorithms?
    - In most cases, we want to make sure that our algorithm is as fast as possible given the size of the input data.
2. Just Time It!
    - The first assumption would be to time how long an algorithm runs for different sizes of input.
    - **Problem:** Different computers run at different speeds. So there really isn't any sort of frame of reference.
    - **Interactive:** There is a table the different running times of the same algorithm for two computers. Some sort of slider or number that you can change that will change the clock speed of one of the computers. 
3. Counting Steps
    - So instead of using the actual time, we can instead count how many operations the algorithm does.
    - Brief RAM Model of Computation. (From now on, functions will refer to how many steps an algorithm takes based on it's input size)
    - "Now, it's pretty easy to see how these algorithms grow based on the size of the input"
    - **Interactive:** Players are given pairs of functions, and prompted to compare which ones are smaller for a "very large" N. These will be simple polynomials/exponential.
4. Why We Can't Use Straight Functions
    - Wait a second, how do we "compare" functions. We can't compare functions like we compare numbers... or can we? In the previous exercise, there was a sense of intuition on how n^2 would be much larger than x.
    - **Problem**: How do we formalize this notion of functions being "better" than eachother
5. Asymptotic Analysis: Big O
   - (I'm really thinking of an intuitive, 3B1B way to show how the mathematics of Big O come out naturally, see notes below. For now assume I have some stellar prose that at the end of it; the learner will think that they could have derived Big O notation thyself. If you're confused on what I'm talking about, please watch more [3B1B](https://www.youtube.com/watch?v=spUNpyF58BY)
   - The prose will take a simple example, such as f(x)=x^2-10 and prove that it is O(x^2). It will go through the process of finding an n_0 and a C. 
   - It will also discuss that f(x) is also O(x^3), O(2^n)
   - **Interactives**
     - *There's going to be small mini problems working up to a full Big O proof. I think the main rub is since the student's are asked to find two variables (C and n), they get really confused. But I'm sure if you started them off with; here's a C, find N (and vice versa), you can build it up nicely.*
     - Given C, find an n_0 such that for all n > n_0; f(x) <= C\*g(x)
     - Given n_0, find a C such that for all n > n_0; f(x) <= C\*g(x)
     - Find a C and n_0 to show that all n > n_0; f(x) <= C\*g(x)
     - All of the paramaters will have sliders so that you can twiddle with the values
     - On the side to all of this, there will be a reactive graph that will show g(x), f(x), and where they intersect (n > n_0). I would like to implement shading to show for when n >n_0. Hopefully this reactive graphs will help the student gain an intuition
6. Same as Above, but with Big Omega
7. Same as Above Above, but with Big Theta
   - For now, these two should be similar enough in interactive. The prose will be different, but I have to ruminate on those a bit more.
8. Why Big O Sucks
   - An explanation for why Big O is not actually the thing to use all the time. It is a good yardstick; but shouldn't be treated as gospel.
9. Conclusion
10. **Bonus**: Sandbox Mode
   - A big com


*Sidenote: If I was teaching Big O my own way, I would instead teach it in almost reverse of what the formalism states. f(x) is O(g(x)) iff for any constant multiple c\*f(x) <= g(x) for n > n_0. I feel like this formulation encapsulates the entire concept of "no matter how much you scale f(x), it will always be eclipsed by a g(x) with no constants.*

*Or, maybe we can frame it as with x and x^2, no matter how hard you scale down x^2, at some point, **at some point it will go higher than x**.*

*However, I'm afraid of confusing students with this rouge way of teaching it.*


# Procedures/Actions

This game will mostly likely use only the mouse to drag sliders and pick up and drop objects/tiles.

# Rules

N/A

# Objects/Entities

- Need to find a nice, dynamic graph library
- Probably some good UI elements too that I can place where needed

## Feedback

- In the sections where they have to find correct constants or values of n, there will be a reactive graph to the side of the screen
- That graph will be colored red/green based off of the value that they pick and if it is correct

# Story and Gameplay

## Presentation of Rules and Content

As I've said for probably the billionth time, I like the 3B1B style where you're teaching a topic in a storylike manner. You are not telling someone "you need to know these concepts and formula", you instead guide them through scenarios where these concepts and formulas come naturally.

If you've ever heard of the storytelling principle "show, not tell", that's pretty much how I want to present the content. So while there might be a bit more prose than other games, it won't be like a textbook (hopefully).

## Story (Brief)

*The Summary or TL;DR version of below*

## Storyboarding

- The left side shows what I think the general layout of the page will be, prose interrupted by little mathematical sections
- Top Right shows what I think the dynamic graphs will look like in the Big O sections. There's a slider for c down below, which will scale the graphs. In addition, n_0 is highlighted, and any values greater than n_0 is shaded in
- Bottom right shows the "sorting" minigame, where they are asked to guess based on intuition which functions are larger for a large N

![image](./story.jpg)

# Assets Needed

## Aethestics

Slick and minimalist type aesthetic. Nothing fancy and over the top, but a webpage design that is sleak and unintrusive.

## Graphical

There's not going to be too much in the way of grap*Give a sense of the aesthetics of your game, the spirit and atmosphere. Use descriptive, evocative words that can help the reader understand the emotional response of your game.*hics. A lot of the material will be presented though prose and dynamic graph plotting. Maybe I'll include some self-drawn cartoonish images relating to the subject to break up the prose if it becomes too dense?

## Audio
- Music List
  - Since this is more of a focused dive into a topic and not a game, the music will most likely be some light, synthy ambient music that's not too busy.
  
- Sound List (SFX)
  - *UI Sounds*: Various types of unintrusive clicks or blips when interacting with UI objects


# Metadata

* Template created by Austin Cory Bart <acbart@udel.edu>, Mark Sheriff, Alec Markarian, and Benjamin Stanley.
* Version 0.0.3
