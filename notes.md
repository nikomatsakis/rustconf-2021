# Goals of the talk

* 2020 has shown that Rust has great promise, and we are positioned to grow like never before
* Rust could be big, way bigger than we ever dreamed
    * Rust could be the default language for anything that runs at scale
    * Anything where reliability is king
* To get there, we have to focus relentlessly on the user experience
    * Whole product: not just the language, but the tooling, the libraries
    * We have to drive down the cost of adoption
* We need to up our game as a community
    * Need to be able to do more things at once, while staying coherent *and focused*
    * Vision docs, engagement
    * Support our contributions by engaging companies in new ways
        * Foundation
        * Teams
* Benefit, if we get there
    * Massive influx of resources
    * Safer internet
    * Save the planet

# Narrative v1

* Banner year for Rust!
    * Launched Foundation
    * Have teams at major companies
    * Rust in the linux kernel
* Is this...it? Did we... make it?
* What was the ur-goal of Rust?
* Rust's charter
    * Great power of C, C++
    * Great feel of JavaScript, Ruby, or Python
* Cheesy graph
    * C/C++
    * JavaScript
    * BANG: Rust
* You can start to see that
    * Tenable story
* This is how Rust should FEEL
    * Reliable
    * Performant
    * **Empowering**
* But let's get real
    * C/C++
    * JavaScript
    * WHIMPER: Rust-- definitely better, but not there
* Survey data
    * Some people just can't learn Rust
* Rust: language where you have the hangover first
    * Rust today IS Reliable, Performant, Empowering --- once you learn it
    * Commonly hear people tell me
        * At first I used Rust for X
        * But then I rewrote my Python/Ruby/whatever script into Rust
        * Got to use awesome packages from cargo
        * It's great
* Goals of Rust
    * [x] Prove it can work 
    * [x] Get adoption 
    * [ ] Industry f!@#!$! standard <--- not there yet
    * Reality:
        * If we want to really get there, we have to do better. A lot better.
* To get there:
    * Today:
        * Productive in Rust in 3 months
    * Goal:
        * Productive in Rust in 3 weeks
* What would that do?
    * Redefine *who* does systems programming
    * Redefine what systems programming *even is*
* What would that be like?
    * Fucking great, that's what
    * More ideas
* What does it take?
    * We need to be **focused**
    * We need to be **creative**
* Focused and creative
    * Always ask ourselves, "Does this create the experience that we want?"
    * Rust is trying to square a circle, it's hard. Really hard.
    * Have to work backwards and forwards at once.
* What does it take?
    * We need to be **focused**
    * We need to be **creative**
    * We need to be **think broadly**
* Go back to tenable. Look at this blog post.
    * Look at all the pieces there
    * In order to even do this experiment
        * Rust
        * Cargo
        * Ecosystem pieces
    * We need to think about the journey and put it all together
* What does it take?
    * We need to be **focused**
    * We need to be **creative**
    * We need to **think broadly**
    * We need to **be brave**
* Being brave
    * Third rails of Rust
* So what does Rust in 2024 feel like?
* Been working on Async Vision Doc, let's look at that
    * Async functions everywhere
        * Today: poll methods
        * Tomorrow: async methods
    * Parallel async iterators
        * (that work)
    * Scopes
* But also:
    * Tooling
    * Documentation
* Does this mean we lose what Rust is?
    * Au contraire. Achieving all this requires a bunch of work to get done
        * Type alias impl trait
        * Impl trait in traits
        * Generic associated types
        * Const generics
* So here's to the next 3 years
    * It's been a wild ride
    * Buckle your seat belts, because it's going to get even crazier

# Narrative v0

...

* Simple equation: cost to adopt &lt; savings from Rust
* What is this cost?
* Learning curve
* Goal: Productive in Rust in 3 weeks
* How do we get there?
    * We need to **up our game**
    * Need to be **focused**
    * Need to be **creative**
* Look beyond the language
    * Look end-to-end, at the "whole cost"
    * Tooling, lessons, source of people
* Process: forming a vision
    * Understand the problem holistically
    * Envision the future you want
    * Figure out the right first step to take you in that direction and do it
* Process: forming a vision
    * loop:
        * Understand the problem holistically
        * Envision the future you want
        * Figure out the right first step to take you in that direction and do it
* Async Vision Doc
    * Trying this out for Async Rust
* Understanding the problem
    * Talked to a lot of people, a lot I didn't know
    * Troublesome patterns
         * Portability yes
         * But also cancellation, nested awaits
    * But also gaps:
        * Tooling, documentation, patterns
* Planning the future
    * "It it compiles, it works"
    * "Tooling to be envious of"
    * "Consolidated documentation that covers xxx"
* Taking our first steps
* Does this mean that we never get core improvements?
    * *New users* vs *Experienced users*
    * A real tension, but this is not a zero sum game
        * First steps for async Rust include some fundamental improvements
            * For example: type alias impl trait, generic associated types
        * The focus on ergonomics benefits everyone
* Example: Accessibility
    * Curb cuts, etc
    * But more than that.
        * It's like, in order to do the curb cuts, had to develop new core technology, which then enables all kinds of other things.
* But don't get me wrong
    * There IS tension
    * CTC
* Secret weapon: open source
    * Let customers help themselves
    * But we have to improve our ability to do that cohesively
    * Tools:
        * Initiative process
        * Creating more written guidelines and principles
        * Engaging companies to hire and support Rust contributors

# XXX

* Idea: link back to the original messaging
    * For Rust to succeed, we need to have 
    * 

# Some notes and possible sources to remember

* https://medium.com/tenable-techblog/optimizing-700-cpus-away-with-rust-dc7a000dbdb2
    * authored by https://askldjd.github.io/resume/