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
- Rust in the linux kernel <sup>1</sup> 🤯

.citation[
<sup>1</sup> Caveat: OK, maybe not quite. But perhaps soon!
]

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
           Productivity -->
```

???

So if we view this as a graph, we kind of have C++
way up there, really fast, but kind of hard to use
correctly.

Then we have JavaScript, Ruby, etc, way over there,
productive, but not all that fast.

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
           Productivity -->
```

.bam-rust[
  ![Rust logo](content/images/rust-logo-512x512.png)
]

???

And then we have *bam* Rust. Best of both.

---

# Let me tell you a story

### <q>Optimizing 700 CPUs Away With Rust</q>

> The Rust-based filter is much more efficient than the original implementation. With the ability to fully manage the heap allocations, Rust’s memory allocation for handling each datagram is kept to a minimum. This means that the Rust-based filter only needs a few MB of memory to operate. **As a result, we saw a 75% reduction in CPU usage and a 95% reduction in memory usage in production.**

.citation[
  [<q>Optimizing 700 CPUs Away With Rust</q>](https://medium.com/tenable-techblog/optimizing-700-cpus-away-with-rust-dc7a000dbdb2) -- Alan Ning, Tenable Techblog
]

---

# It was even pretty easy to do

Article continues:

> With this small change, we were able to optimize away over 700 CPU and 300GB of memory. **This was all implemented, tested and deployed in a single sprint (two weeks).** Once the new filter was deployed, we were able to confirm the resource reduction in Datadog metrics.

.citation[
  [<q>Optimizing 700 CPUs Away With Rust</q>](https://medium.com/tenable-techblog/optimizing-700-cpus-away-with-rust-dc7a000dbdb2) -- Alan Ning, Tenable Techblog
]

---

# This is how should feel

---

# Performant

> .font150[<q>It ran well right out of the box!</q>]

--

> .font150[<q>Then I remembered `cargo run --release`, and it ran *really* well!</q>]

---

# Reliable

> .font150[<q>If it compiles, it works</q>]

---

# Above all: Empowering

> .font150[<q>Complex stuff feels easy</q>]

???

When Rust is really working right, it makes what used to be complicated stuff just feel simple.

You want to parallelize that loop? Do it!

You want to use nifty new kernel APIs like io-uring? Do it!

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
           Productivity -->
```

---
template: lets-get-real

.bam-rust[
  ![Rust logo](content/images/rust-logo-512x512.png)
]

???

* If this is what we're shooting for... the performance of C++ with the productivity of JavaScript, I don't think we're quite there.

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

* We're more like here. We've got the great performance. 
* The productivity can be really high, especially for complex tasks. 
* But on the whole, you just can't claim that Rust is as easy to use as JavaScript or Python. Or even close.

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

# Some folks just never learn

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

The first big step was 1.0, in 2015, where we showed that the basic approach of Rust -- ownership and borrowing -- worked.

--
* 2021: Critical adoption, sustainability ✅

???

The next milestone I think we passed this year. We've seen Rust adoption grow to the point where it is used in many critical systems. We're seeing more and more Rust developers being hired to work on the project, which will help us grow faster and be more sustainable.

--
* 202X: Widespread usage: become an industry standard ⏳

???

So what's next? Where are we headed? I think our next goal is to see Rust in widespread use. I don't expect Rust to be used everywhere, but I think there remain quite a lot of applications where Rust's combation of performance and productivity would be a really good fit. If they could just learn it.

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
  Seriously though, the whole Rust Evangelism Strike Force thing kind of annoys people. Don't do that.
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

# What would that do?

---

# Not just changing *who* does system programming...

![new generation](content/images/gogaruco.png)

Yehuda Katz at Golden Gate Ruby Conference 2014

---

# ...but changing what systems programming *is*

Rust is the <q>go to</q> language for systems programming

???

Today, people reach for Rust to tackle the hardest problems. 

Things like the rendering engine of a browser, or the core services that underlie the internet.

---

# ...but changing what systems programming *is*

Rust is the <q>go to</q> language for ~~systems programming~~

???

But I think we could do more than that.

--

Rust is the <q>go to</q> language for systems that **run at scale**.

Rust is the <q>go to</q> language for systems where **reliability counts**.

???

What if people were using Rust for anything that was going to run at scale, or for anything where reliability was really important?

I mean...why not. I don't know about you, but I at least have found Rust displacing other languages I used to use, like Python. It's nothing against those languages, which are fantastic. It's just that Rust has a lot to offer: you get cargo and easy access to great libraries like serde. Moreover, when you wield Rust well, the code can be remarkably concise and clean. The borrow checker isn't much of a bother, because you can clone or box or do other things. And when you're done, your code runs fast. Even better, you can come back after six months and still do a successful refactoring.

--

.p40[![Galaxy brain](content/images/galaxy-brain.png)]

---

# What would that be like?

--

Pretty dang great, that's what! 😁

--

More people → More good ideas

More good ideas → More people

More people → More good ideas

More good ideas → More people

More people → More good ideas

More good ideas → More people

???

So, if we managed that, what would it be like?

I think it'd be fantastic. Rust has always been premised on the idea that great ideas are everywhere.

The more people we can get working on Rust, the more great libraries we can have, and the more great ideas, the more we will all benefit.

What's more, having more people using Rust leads to more adoption -- it's easier to hire.

And, of course, we're also saving a lot of energy. Something I suspect many of us care about.

---
name: how-do-we-get-there-1

# Upping our game

* We need to be **focused**

* We need to be **creative**

???

So, how are we going to get there? It won't be easy. We have to up our game.

---

# Being focused and creative

Always be asking: How do we want Rust to feel?

* Reliable: <q>if it compiles, it works</q>
* Performant: <q>ran well right out of the box!</q>
* Empowering: <q>complex stuff feels easy</q>

???

We always have to be asking ourselves: what is the experience we are trying to create? Have we achieved it?

Rust is trying to square a circle. It's hard, really hard.

We have to work backwards from the experience we want, and forwards from what we know how to do at once.

---

# Rust design principles

---
template: how-do-we-get-there-1
name: how-do-we-get-there-2

* We need to **think broadly**

---

# Thinking broadly

### <q>Building a microservice with Rust</q>

> We decided to run an experiment and create a simple microservice written in Rust to see for ourselves if it’s worth it. The thinking was: if we failed, we would learn something useful anyway, if we succeeded, we would add a new awesome device to our team’s toolbox.

.citation[
  [<q>Building a microservice with Rust</q>](https://medium.com/tenable-techblog/building-a-microservice-with-rust-23a4de6e5e14) -- Mikhail Medvedev, Tenable Techblog
]

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

---

# Thinking broadly

Productivity is not just about the language or stdlib.

Requires learning materials, tooling, and ecosystem.

<q>Whole product thinking</q> has always been a <q>Rust thing</q>, but it's going to be more important than ever.

???

If we want to make it possible to be productive in 3 weeks, we have to look at the things that people are trying to do and what is blocking them. Those are the problems to attack. They may not be where we expect. In fact, they probably aren't -- if they were, we might have attacked them already.

---
template: how-do-we-get-there-2
name: how-do-we-get-there-3

* We need to **be bold**

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

If we want new results, have to do new things.

Here is a list of things that we have never done, and with good reason.

I cannot tell you if revisiting any of these questions would make a difference in terms of "productivity in 3 weeks".

But I CAN tell you that if we want to achieve that goal, if we want to make Rust a mainstream language, we are going to have to be willing re-examine some of our basic assumptions.

---

# Rust 2021 Edition

**Editions let us make otherwise impossible changes.**

As always, we don't split the ecosystem:

* Rust 2021 fully interoperates with Rust 2018 and Rust 2015.
* Tooling handles the migration for you.

---

# Rust 2021 Edition: Highlights

## Enabling better format strings

```rust
let mut x = 22;
println!("{x}");
```

Shoutout to Mara Bos (next speaker!) for driving that process!

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

Shoutout to the [RFC 2229 project group](https://www.rust-lang.org/governance/teams/compiler#wg-rfc-2229)<sup>1</sup> for their hard work on this over the last year!

.citation[
  <sup>1</sup> Aman Arora, Archer Zhang, Chris Pardy, Dhruv Jauhar, Jennifer Willis, logmosier, Roxane. Y'all rock!
]

---

# More shoutouts

| Feature | Hero(es) |
| --- | --- |
| New prelude | Dirkjan Ochtman, jam1garner |
| Cargo feature resolver | Eric Huss |
| IntoIterator for arrays | cuviper |
| Or patterns | mark-i-m, hi-rustin |
| Reserved syntax | bstrie, lrh2000 |
| General assistance | Ryan Levick, Manish Goregaokar, |
| | Mark Rousskov  |

Y'all rock too.

.citation[
  I couldn't fit all the people who worked on these features on this slide,
  so I tried to select the folks who did the most work specifically related to the Edition.
  Hopefully I didn't forget anyone! 💜
]

---

# Async vision doc

![2021-07-17](content/images/2021-07-17-Blog.png)

???

Earlier this year, Tyler and I undertook a new kind of exercise.

We drafted a vision doc for Async Rust. This process began by talking to lots of Async Rust users about their experiences, both good and bad. We then brainstormed out possible ways to address the gaps we saw and came up with a roadmap for the work we expect to do over the next year or two.

---

# How async Rust should feel

> Consistent: <q>just add async/await</q>
>
> Async Rust should be a small delta atop Sync Rust.

---

# Not always true today

Synchronous iterator trait:

```rust
trait Iterator {
  type Item;

  fn next(&mut self) -> Option<Self::Item>;
}
```

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

---

# Where we are headed

Asynchronous iterator trait, tomorrow:

```rust
trait AsyncIterator {
  type Item;

  async fn next(&mut self) -> Option<Self::Item>;
}
```

---

# How async Rust should feel

> Reliable: <q>if it compiles it works</q>

Challenges:

* *Portability*
* *Subtle details of the poll model*
* *Cancellation*

---

# How async Rust should feel

> Reliable: <q>if it compiles it works</q>

Solutions:

* APIs for portable libraries that support multiple runtimes.
* Parallel async iterator APIs like Rayon.
* Structured concurrency primitives for managing cancellation, task scheduling.

---

# Transparency

> Transparent and tunable: <q>it's easy to diagnose deadlocks and performance bottlenecks</q>

[Eliza Weisman] is building the Tremendously Nifty [tokio-console]:

![Tokio Console Screenshot](content/images/tokio-console-1.png)

[tokio-console]: https://github.com/tokio-rs/console
[Eliza Weisman]: https://github.com/hawkw

---

# Documentation and learning

> Empowering: <q>complex stuff feels easy</q>

Planning a revised async book that is oriented at both getting you "up and going" quickly and thoroughly covering key concepts:

* Getting started
* Fundamental concepts
* Writing async code
* ...
* Design patterns

---

# Not zero sum

* Tools meant for one group tend to benefit everyone:
  * Console can help you learn, too

--
* Work on async benefits everyone:
  * `async fn` in traits requires improvements to trait system

---

# In closing...

* Future so bright, you gotta wear 😎
* Rust is seeing more use, and more investment, than ever before.
* Rust is going to get both easier to learn and more powerful.
