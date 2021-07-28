class: center
name: title
count: false

# RustConf 2021

<img src="content/images/mascot-lockup.svg"/>

.me[.grey[*by* **Nicholas Matsakis**]]
.citation[`https://github.com/nikomatsakis/rustconf-2021`]

---

# 2021

- Rust foundation launched! 🎉
- Platinum sponsors: 
  - AWS, Google, Huawei, Microsoft, Mozilla, Facebook

???

* 2021 saw Rust go from a project primarily supporting by one company, Mozilla, to having its own Foundation with, at current count, 6 platinum sponsors!
* These include many of the biggest names in computing.
* Not bad.

--
- Rust teams at many major companies!! 😲

???

* What's more, many of those companies have created their own Rust teams.

--
- Rust under consideration for the linux kernel 🤯

???

* And if *that* wasn't enough, what about Rust being considered for the linux kernel?
* So, given all that, I have one question for you...

---

# Are we there yet?

Is this... it?

???

* Is this it?

--

Did we... make it?

.p50[
![Ferris thinking](content/images/ferris_thinking.jpg)
]

.citation[
  From [rochacbruno/rust_memes](https://github.com/rochacbruno/rust_memes)
]

???

* Did we...make it?
* To answer that question, let's go back in time. What was the "ur-goal" of Rust? What did we set out to do when we started on this journey?

---

# Rust's charter

Deliver the

### Great power of C or C++

with the

### Great feel of JavaScript, Ruby, or Python

???

Rust's goal has always been to "have our cake and eat it to". We want to combine the great power of C++ with the high-level feeling of a language like JavaScript, Ruby, or Python.

---

# Cheesy graph

```
 ^  |
 |  |
 P  │ C++   
 e  │       
 r  │       
 f  │       
 o  │       
 r  │       
 m  │       
 a  │       
 n  │       
 c  │        
 e  │        
    │                JS, Ruby, Python
    └─────────────────────────────────
           Ease of use -->
```

???

So if we view this as a graph, we kind of have C++
way up there, really fast, but kind of hard to use
correctly.

Then we have JavaScript, Ruby, etc, way over there,
easy to use, but not all that fast.

---

# BAM: Rust

```
 ^  |
 |  |
 P  │ C++                   RUST
 e  │                     x
 r  │                   x 
 f  │                 x 
 o  │               x
 r  │             x
 m  │           x
 a  │         x
 n  │       x  
 c  │     x    
 e  │   x     
    │ x              JS, Ruby, Python
    └─────────────────────────────────
           Ease of use -->
```

.bam-rust[
  ![Rust logo](content/images/rust-logo-512x512.png)
]

???

And then we have *bam* Rust. Best of both, right?

---

# Let me tell you a story

### <q>Optimizing 700 CPUs Away With Rust</q>

> The Rust-based filter is much more efficient than the original implementation. With the ability to fully manage the heap allocations, Rust’s memory allocation for handling each datagram is kept to a minimum. This means that the Rust-based filter only needs a few MB of memory to operate. **As a result, we saw a 75% reduction in CPU usage and a 95% reduction in memory usage in production.**

.citation[
  [<q>Optimizing 700 CPUs Away With Rust</q>](https://medium.com/tenable-techblog/optimizing-700-cpus-away-with-rust-dc7a000dbdb2) -- Alan Ning, Tenable Techblog
]

???

When things are going well, this is actually exactly how Rust feels. This blog post by the folks at Tenable is a great example. They replaced some of their JavaScript code to process logs with Rust, and they saw a huge improvement in resource usage.

---

# It was even pretty easy to do

Article continues:

> With this small change, we were able to optimize away over 700 CPU and 300GB of memory. **This was all implemented, tested and deployed in a single sprint (two weeks).** Once the new filter was deployed, we were able to confirm the resource reduction in Datadog metrics.

.citation[
  [<q>Optimizing 700 CPUs Away With Rust</q>](https://medium.com/tenable-techblog/optimizing-700-cpus-away-with-rust-dc7a000dbdb2) -- Alan Ning, Tenable Techblog
]

???

What's more, it only took them two weeks to do it! Very nice.

---

# This is how should feel

???

This is exactly how Rust is supposed to feel when it's working well. It's supposed to be...

---

# Performant

> .font150[<q>It ran well right out of the box!</q>]

.center[
.p40[
![Run fast](content/images/run-fast.jpg)
]
]

???

Performant. You don't have to avoid fancy features like closures or iterators to get Rust programs to run quickly. In fact, using those features often works better than trying to write the code by hand.

---

# Performant

> .font150[<q>It ran well right out of the box!</q>]


> .font150[<q>Then I remembered `cargo run --release`, and it ran *really* well!</q>]

.center[
.p25[
![Run fast](content/images/run-fast.jpg) ![Run faster](content/images/run-faster.jpeg)
]
]

???

Though it does help to turn on optimizations.

Rust code should also be...

---

# Reliable

> .font150[<q>If it compiles, it works</q>]

.center[
.p60[
![Crossed wrenches](content/images/Reliable.jpg)
]
]

???

Reliable. When something compiles, if there's a bug, it's not because you don't understand Rust well enough, it's somewhere in the logic of your code. This means you can do things like a huge refactor, or making a loop run in parallel, and find that your code "just works".

Finally, when Rust is working well, it's...

---

# Above all: Empowering

> .font150[<q>Complex stuff feels easy</q>]

.center[
.p40[
![Empowered Person](content/images/Empowered.jpg)
]
]

???

Empowering. It makes using complicated, wizard stuff feel fun. Want access to that new, nifty kernel API? We got a crate that wraps it in up in a safe interface. Want to run code on an embedded device with no operating system? Go for it. And so on.

---
name: lets-get-real

# But let's get real

```
 ^  |
 |  |
 P  │ C++   
 e  │       
 r  │       
 f  │       
 o  │       
 r  │       
 m  │       
 a  │       
 n  │       
 c  │        
 e  │        
    │                JS, Ruby, Python
    └─────────────────────────────────
           Ease of use -->
```

???

OK, that's how Rust feels when it's working well. But let's be honest. It's not always like that.

---
template: lets-get-real

.bam-rust[
  ![Rust logo](content/images/rust-logo-512x512.png)
]

???

If we're shooting for the ease of use of JavaScript, we're not quite there.

---
template: lets-get-real

.transparent[
.bam-rust[
  ![Rust logo](content/images/rust-logo-512x512.png)
]
]

.whimper-rust[
  ![Rust logo](content/images/rust-logo-512x512.png)
]

???

We're more like here. We've got great performance. *Some things are easy*, but using Rust -- especially early on -- still means spending a lot of time "fighting the borrow checker" and learning the "tricks of the trade".

On the whole, you just can't claim that Rust is as easy to use as JavaScript or Python. Or even close.

---

# Learning Rust takes time

.center[
![Time to perceived user productivity](./content/images/8-How-Long-To-Be-Productive.svg)

(Rust 2019 Survey Results)
]

???

I mean, let's look at the survey results. This chart is from 2019 -- I didn't have ready access to a chart from 2020, but I'm sure the results are comparable.

Here, we asked people how long it took until they felt productive using Rust.

--

.lessthanamonth[![Arrow](content/images/Arrow.png)]

???

You can see there's a good chunk of people that pick up Rust fairly quickly. These might be the tenable folks: they're able to get productive in a month or so, and build from there.

Trust me, without all the hard work that we've put into careful design, error messages, documentation, and the like, this number would be a lot smaller.

--

.lessthanayear[![Arrow](content/images/Arrow.png)]

???

None the less, for even more people, getting productive in Rust was measured not in weeks, but in months. 

--

.notproductive[![Arrow](content/images/Arrow.png)]

???

In fact, there's a pretty decent chunk of people who claim they've never felt productive!

Now you might be thinking, I bet those people who don't feel productive are all beginners who just haven't learned Rust yet, right?

---

# Some folks *never* feel productive

.center[
![How long have "not productive yet" folks been learning Rust?](./content/images/22-unproductive-expertise.svg)

(Rust 2019 Survey Results)
]

???

Wrong.

We thought the same thing, so we looked at how long people who said they didn't feel productive had been using Rust.

--

.fewmonths[![Arrow](content/images/Arrow.png)]

???

For many of them, it's a few months. Now, you could call that a beginner, although I think it shoudln't take months to feel productive in a language.

--

.neverproductive[![Arrow](content/images/Arrow.png)]

???

But for most folks it was longer. Some of them had been using Rust for more than 3 years!

If we want to truly want people to feel as productive in Rust as they do in Python -- and I do -- we have got to do better. A lot better.

---

# Rust rocks 🎸...

???

The fact is, Rust really rocks...

--

## ...once you learn it 😬

???

...once you learn it! But that can be quite difficult.

---

# OMG so perfect

<br/>
<br/>
<br/>

<q>Rust: the language where you get the hangover first</q>

-- Old Rust proverb <sup>1</sup>

.citation[
  <sup>1</sup> The person who said this to me said it was a quote from somewhere, but they didn't know where. Searching the web has only turned up references to the Rust game. HALP!
]

???

I recently heard the best phrase ever to describe this. "Rust is the language where you get the hangover first". This is perfect on so many levels.

First, the obvious: that getting used to Rust takes time, but once you're past the hangover, you feel like you have a new pair of wings. It's a lot easier to build and maintain ambitious projects. And actually, not just ambitious ones. 

Once you've got your groove in Rust, it's really great! You can grab packages from cargo, write high-level code with iterators and closures a nifty APIs, and things run super fast!

I hear a lot of people saying "At first I used Rust to write the powerful project. But then I had this old script I had written and I needed to modify it. It seemed easier to just rewrite it in Rust. The code is about the same length, but now it runs faster, and I'm not afraid to come back to it and change it later."

And this is exactly why this metaphor is awesome: it works the other way, too. In a lot of languages, everything feels great at first, but the hangover comes when you try to manage the maintenance.

---

# Don't know if you heard...<sup>1</sup>

We're the <q>most loved</q> language on Stack Overflow for like 100 years running now.<sup>2</sup>

Just sayin'.

.citation[
  <sup>1</sup> Actually, I'm pretty sure you did. That's the joke. Get it? See??? <br/>

  <sup>2</sup> Oh dear! This slide is sure to bring bad luck. No way that we will win next year *now*.
]

???

And I think this is why Rust keeps winning the "most loved" question on stack overflow year after year. The question asks people using Rust if they want to keep using Rust -- and they do!

---

# Just don't look at "most popular"

| Language | Percent |
| --- | --- |
| 1. JavaScript | 67% |
| 2. HTML/CSS | 63% |
| 3. SQL | 54% |
| 4. Python | 44% |
| 5. Java | 40% |
| ... | ... |
| 19. Rust | 5% |

Upside: Lots of room to grow!

???

Of course, it you look at the other questions, Rust doesn't do as well. When it comes to the widely used, we come in at 5%. Which is actually pretty good -- much better than I ever expected. But I think Rust deserves to be used more.

---

# Are we there yet?

???

So to come back to my original question. Are we there yet? No, not yet, but we've come a long way.

--

* 2015: Prove it can work ✅

???

If you think back to 2015, when we shipped 1.0, we showed that Rust actualy *can work*. This what had seemed like a pie-in-the-sky research effort could actually be used to ship production sytems.

--
* 2021: Critical adoption, sustainability ✅

???

The next milestone I think we passed this year. We've seen Rust adoption grow to the point where it is used in many critical systems. We're seeing more and more Rust developers being hired to work on the project, which will help us grow faster and be more sustainable.

--
* Next goal: Widespread usage: become an industry standard ⏳

???

So what's next? Where are we headed? I think our next goal is to see Rust in widespread use. I don't expect Rust to be used everywhere, but I think there remain quite a lot of applications where Rust's combination of performance and productivity would be a really good fit. If they could just learn it.

---

# How do we get there?

???

So, how do we get there?

--

.center[
.p60[
![Evangelism](https://raw.githubusercontent.com/rochacbruno/rust_memes/master/img/strikeforce.jpg)
]
]

.citation[
  Seriously though, having people show up uninvited and tell you what language you should use for your own project is kind of annoying. Tell them what you like about their project instead!
]

???

Rust evangelism strike force! Well, maybe not. Just hectoring people  into using Rust is probably not going to do the trick.

---

# How do we get there?

### Today: Productive in Rust in 6 months (or more)

???

What about this. What if instead of people taking 6 months to feel productive in Rust...

--

### Goal: Productive in Rust in 6 weeks (or less)

???

What if it took six weeks?

--

.center[.font300[.font300[😲]]]

---
name: how-do-we-get-there-1

# Upping our game

* We need to be **focused**

* We need to be **creative**

???

So, how are we going to get there? It won't be easy. If we really want to get the "time to productivity" to be measured in weeks, that is something we have to approach deliberately.

---

# Being focused and creative

Always be asking: How do we want Rust to feel?

* Reliable: <q>if it compiles, it works</q>
* Performant: <q>ran well right out of the box!</q>
* Empowering: <q>complex stuff feels easy</q>

???

We always have to be asking ourselves: what is the experience we are trying to create and have we achieved it?

Rust is trying to achieve a delicate balance of exposing complexity in a really simple way. It's not easy.

---
template: how-do-we-get-there-1

???

So, we have to be focused and creative. What else?

--
name: how-do-we-get-there-2

* We need to **think broadly**

???

We need to think broadly, by which I mean we have to look at the experience of using Rust holistically. We need to look at what users are trying to do and figure out how to ensure that all the pieces are there, even the things that aren't under our direct control.

---

# Thinking broadly

### <q>Building a microservice with Rust</q>

> We decided to run an experiment and create a simple microservice written in Rust to see for ourselves if it’s worth it. The thinking was: if we failed, we would learn something useful anyway, if we succeeded, we would add a new awesome device to our team’s toolbox.

.citation[
  [<q>Building a microservice with Rust</q>](https://medium.com/tenable-techblog/building-a-microservice-with-rust-23a4de6e5e14) -- Mikhail Medvedev, Tenable Techblog
]

???

Remember that blog post by the folks at Tenable? The one where they radically reduced their resource usage? If you look at their blog, you'll find that before that post came another post, one where they were evaluating Rust. It's a nice read.

---

# Thinking broadly

> Pieces of the puzzle
>
> A typical microservice is made of:
> * HTTP API
> * Code to work with the database
> * Code to read messages from a queue, such as Kafka.
> * A Dockerfile
>
> ...

???

Something I found interesting about it was that they spelled out their thought process. They talked about all the pieces they need to assemble to make Rust work for their problem. They were able to pull it off, but in some cases they had to hack a few things together. 

---

# Thinking broadly

Productivity is not just about the language or stdlib.

Requires learning materials, tooling, and a rich, stable ecosystem.

<q>Whole product thinking</q> has always been a <q>Rust thing</q>, but it's going to be more important than ever.

???

For us to push productivity down to a few weeks, we need to make sure that all the pieces people need are in place. This includes the "glue code" to connect systems, but also things like documentation, IDE integration, or debugger support. Learning ownership and borrowing is always going to take some time, but the rest, we can solve.

---
template: how-do-we-get-there-2

???

OK, so think broadly, what else?

--
name: how-do-we-get-there-3

* We need to **be bold**

???

We've got to be willing to take risks.

---

# Being bold

The <q>third rails</q> of Rust: 😱

* Recommending specific crates from the ecosystem

* Allocation without an explicit keyword

* Removing the `mut` keyword on `let` <sup>1</sup>

Is it time to revisit some of those questions? Other questions?

.footnote[
   <sup>1</sup> aka [mutpocalypse](https://smallcultfollowing.com/babysteps/blog/2014/05/13/focusing-on-ownership/)
]

???

If we want new results, we've got to be willing to do new things. Here is a list of things that we have never done, with good reasons!

I cannot tell you if revisiting any of these questions would make a difference in terms of reaching "productivity in 6 weeks".

But I CAN tell you that if we want to achieve that goal, if we want to make Rust a mainstream language, we are going to have to be willing re-examine some of our basic assumptions.

---

# Rust 2021 Edition

**Editions let us make otherwise impossible changes.**

As always, we don't split the ecosystem:

* Rust 2021 fully interoperates with Rust 2018 and Rust 2015.
* Tooling handles the migration for you.

???

On that note, of being bold, it's a good time to talk about editions. This year, we are releasing Rust 2021. The idea of an edition is that every crate declares the edition of Rust they want to use -- Rust 2015, Rust 2018, or (soon) Rust 2021. No matter which edition you use, your crate interoperates with other crates. Even better, if you have an existing crate, we have tooling that will automatically convert it from one edition to the next.

So how are we using this tool? The idea is to make targeted improvements that make Rust easier to use. They're often things you might not even realize have changed -- it's just that you suddenly have fewer problems than you had before.
---

# Rust 2021 Edition: Highlights

## Changing closure captures

```rust
let tuple = (String::new(), String::new());
let print_0 = move || println!("{}", tuple.0);
let print_1 = move || println!("{}", tuple.1);
```

In Rust 2018: error. 😢

In Rust 2021: works! 🎉

Shoutout to the [RFC 2229 project group](https://www.rust-lang.org/governance/teams/compiler#wg-rfc-2229) for their hard work on this over the last year: Aman Arora, Archer Zhang, Chris Pardy, Dhruv Jauhar, Jennifer Willis, Logan Mosier, Roxane Fruytier. Y'all rock!

???

As one example, we're changing how closures work. In Rust 2018, closures always capture an entire variable, but this can make code like this stop working -- because both closures move `tuple`. In 2021, this code will compile, just like you would expect.

---

# Rust 2021 Edition: Highlights

## Enabling better format strings

```rust
let mut x = 22;
println!("{x}");
// instead of `println!("{}", x)`
```

Shoutout to Mara Bos (next speaker!) for driving that process!

???

We also use editions to make more obvious features. For example, we recently decided to add better format strings where you can name variables in the string itself. In some edge cases, though, this broke backwards compatibility, so we used an edition to tweak those edge cases in Rust 2021.

---

# More shoutouts

| Feature | Hero(es) |
| --- | --- |
| New prelude | Dirkjan Ochtman, jam1garner |
| Cargo feature resolver | Eric Huss |
| IntoIterator for arrays | cuviper |
| Or patterns | mark-i-m, hi-rustin |
| Reserved syntax | bstrie, lrh2000 |
| Overall leadership | Mara Bos and myself |
| General assistance | Ryan Levick, Manish Goregaokar, |
| | Mark Rousskov  |

Y'all rock too.

.citation[
  I couldn't fit all the people who worked on these features on this slide, so I tried to select the folks who did the most work specifically related to the Edition. Hopefully I didn't forget anyone! 💜
]

???

There's a lot more in the edition I don't have time to talk about, but I did want to say a big Thank You to all the people who've been working on it.

---

# How to visioneer

.center[
.p75[
![shiny future](content/images/shiny-future.jpg)
]
]

???

So, we're ready to be focused, creative, and bold. How do we decide what to do? It happens that this very question was facing us earlier this year, as we thought about how to approach async rust.

You may recall that, 2 years back, we shipped the async-await MVP in Rust. This was a huge achievement. In the meantime, we've had time to gain a lot of experience in Rust, and we wanted to decide what we ought to be doing next to improve the async Rust experience. The problem is that there is such a huge range of possibilities, with so many variations to explore. How do we get everybody on the same page?

---

# The status quo

.center[
.p75[
![shiny future](content/images/shiny-future.jpg)
]
]

.daphnesqarrow[![Arrow](content/images/Arrow.png)]

???

I was discussing this with Shane Miller, the manager of the AWS Rust Platform team, and she shared with me some of the approaches that she had used to do similar product drives within Amazon and elsewhere in the past. The idea was to start with an in-depth examination of the *status quo* -- what is it like to use Async Rust today? This gives you a good view both of what problems people want to solve, but also the myriad challenges that they face in doing so.

Importantly, these challenges are often not in the areas you think. As a simple example, when  discussing Async Rust with working programmers, often the first thing *they* talked about was the question of which IDE to use, and how well the debugger worked (or didn't, as the case may be). This of course is not specific to async Rust, but it can be a blocker to adoption nonetheless.

---

# The shiny future

.center[
.p75[
![shiny future](content/images/shiny-future.jpg)
]
]

.daphnesfarrow[![Arrow](content/images/Arrow.png)]

???

Once you have a good handle on the status quo, the next step is to draft the *shiny future*. The idea is to replay same "status quo" stories, but think about what it would feel and be like if it went right. At this stage, you don't have to worry about exactly how you will achieve that. You just have to think about what you would like to achieve, trust in your own ability to find a path that gives that feeling.

---

# Async vision doc

![2021-07-17](content/images/2021-07-17-Blog.png)

Right, so that was the template we wanted to apply, but the problem that Tyler awe wanted to adapt it from a setting like AWS into something appropriate for an open source project like Rust. What we did was to create a repo where people could open PRs with their open stories. To help encourage people to draft, we help public writing sessions, where Rustaceans from all over would show up and help us document their experiences. We also met privately with people to get a more detailed look. 

Next we collated these with how we thought Rust should feel and tried to find places where we were falling short, and what we could do to fix them.

---

# How async Rust should feel

> Consistent: <q>just add async/await</q>
>
> Async Rust should be a small delta atop Sync Rust.

???

Here is one example: Using Async I/O in Rust should, ultimately, be familiar. We should keep a small gap between async Rust and sync Rust, so that it's easy to move from one to the other.

---

# Not always true today

Synchronous iterator trait:

```rust
trait Iterator {
  type Item;

  fn next(&mut self) -> Option<Self::Item>;
}
```

???

In practice, though, the gap between async Rust and sync Rust can be surprisingly large. Here's a simple example. This is the *synchronous* Iterator trait. If you know Rust, you're probably familiar with it: it has one method, `next`, that you call to get the next item from the iterator.

---

# Today's `Stream` trait

Asynchronous iterator trait, today:

```rust
trait Stream {
  type Item;

  fn poll_next(
    self: Pin<&mut self>
  ) -> Poll<Option<Self::Item>>;
}
```

???

Here is the *asynchronous* iterator trait, `Stream`, that is currently in Nightly. It's actually quite close to the iterator trait, but that's not entirely obvious. The `next` method has become a poll method, for example.

---

# Where we are headed

Asynchronous iterator trait, tomorrow:

```rust
trait AsyncIterator {
  type Item;

  async fn next(&mut self) -> Option<Self::Item>;
}
```

???

This is the definition we expect to get to. You can see that this is much closer to the synchronous trait: it's basically the same, but with the async keyword on the `fn` definition.

---

# Transparency

> Transparent and tunable: <q>it's easy to diagnose deadlocks and performance bottlenecks</q>

[Eliza Weisman] is building the Tremendously Nifty [tokio-console]:

![Tokio Console Screenshot](content/images/tokio-console-1.png)

[tokio-console]: https://github.com/tokio-rs/console
[Eliza Weisman]: https://github.com/hawkw

???

Earlier I mentioned that improving Rust means looking beyond the traditional boundaries of the language and libraries. One thing that we found in talking to people using Rust is that there is a real gap in tooling when you shifted to async Rust. Trying to use a traditional debugger, or top, or other such tools just can't tell you what's going on in an async Rust application, since so many of the concepts are defined in user space.

Fortunately, people in th ecosystem are trying to address this need. In the tokio project, for example, Eliza Weisman has been building a really cool monitoring program called the tokio console. It uses the tracing logging library to track what is happening in your async Rust application and give you a view of all the active tasks and what they're up to. The idea is to extend it with other kinds of monitoring, such as detecting and warning about common pitfalls.

Looking forward, the vision doc outlines a number of improvements we can do to tooling, ranging from better debugger integration, to live profiling for running services, to things like profiler-guided optimization specific to async Rust. I would like to see us take cool projects like tokio console and incorporate them together into a standard suite of Rust profiling and debugging tools.

---

# More things in the vision doc...

* APIs for portability across runtimes
* Ability to spawn tasks that can access borrowed data.
* Structured concurrency and a revised cancellation model.
* Sync and async generators for writing iterators
* Revised async book that covers both getting started and key design patterns

[Read the whole thing.](https://rust-lang.github.io/wg-async-foundations)

???

There's a lot more in the async vision doc, so give it a read.

---

# Not zero sum

* Tools meant for one group tend to benefit everyone:
  * Console can help you learn, too

???

One thing I want to emphasize. Throughout this talk, I've been focusing on reducing learning curve. I sometimes get the pushback that we should be working instead fo enable more powerful features, or to better serve power users. There's definitely tension there, but I think much less than is commonly believed. Usually a tool that helps one group winds up helping the other as well -- and in both directions.

The console project is an interesting example. It was developed in response to the needs of existing developers, people who are running services and want to debug them. But one bit of feedback we've gotten is that it can serve as a really useful teaching tool as well, since it helps people to understand what's going on under the hood.

--
* Work on async benefits everyone:
  * `async fn` in traits requires improvements to trait system

???

Similarly, focusing on async doesn't just benefit async. Building the future that I've sketched here is going to require a lot of fundamental improvements to Rust that will benefit sync and async programs alike.

---

# So...what's next?

---

# Not just changing *who* does system programming...

![new generation](content/images/gogaruco.png)

Yehuda Katz at Golden Gate Ruby Conference 2014

???

We've talked before about how Rust's safety guarantees makes systems programming accessible to a much broader pool of people.

---

# ...but changing what systems programming *is*

Rust is the <q>go to</q> language for critical systems

???

But I think that whereas today people are using Rust just for the *hardest problems*, the *critical systems*...

---

# ...but changing what systems programming *is*

Rust is the <q>go to</q> language for ~~critical systems~~

--

Rust is the <q>go to</q> language for anything running in the cloud.

Rust is the <q>go to</q> language for anything running on embedded devices.

Rust is the <q>go to</q> language for all kinds of things, but especially those where reliability counts.

???

...we should aim for people to be using Rust for all kinds of things. Anything that runs on scale, or anything where reliability counts.

---

# What would that be like?

???

So, if we managed that, what would it be like?

--

Pretty dang great, that's what! 😁

???

I think it'd be fantastic.

--

More people → More good ideas

???

The more people using Rust, the more good ideas those people are going to have for how to improve it, or what libraries to build. 

--

More good ideas → More people

???

That in turn leads to more people using Rust.

--

More people → More good ideas

More good ideas → More people

More people → More good ideas

More good ideas → More people

???

And so on.

---

# Future so bright, you gotta wear 😎

* 2015: Prove it can work ✅
* 2021: Critical adoption, sustainability ✅
* Next goal: Widespread usage: become an industry standard ⏳

???

That brings me to the end of my talk. I'm really excited about what's coming up for Rust over the next few years, and I hope that I've gotten you excited as well. Thanks very much for listening, and I hope that you enjoy the rest of RustConf!