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
- Rust teams at many major companies!! 😲

???

* Banner year for Rust
* Launched Foundation, so Rust has a stable home as it grows and moves toward sustainbility
* Speaking of sustainability, multiple teams of multiple devs!
* oh, and one other thing: linux kernel!
* representative of Rust's growing usage in the foundational pieces of the computing world
* so naturally I have a question for you all

--
- Rust in the linux kernel 🤯

---

# Is...this it?

--

Like, did we... make it?

--

.p50[
![Ferris thinking](content/images/ferris_thinking.jpg)
]

.citation[
  From [rochacbruno/rust_memes](https://github.com/rochacbruno/rust_memes)
]

???

So like...have we done it? Are we done?

---

# Rust's charter

Deliver the

### Great power of C or C++

with the

### Great feel of JavaScript, Ruby, or Python

???

Well, let's go back. What was the "ur-goal" of Rust? What did we set out to do?
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

# Reliable

> .font150[<q>If it compiles, it works</q>]

---

# Performant

> .font150[<q>It ran well right out of the box!</q>]

--

> .font150[<q>Then I remembered `cargo run --release`, and it ran *really* well!</q>]

---

# Above all: Empowering

> .font150[<q>Complex stuff feels easy</q>]

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

---

# Learning Rust takes time

.center[
![Time to perceived user productivity](./content/images/8-How-Long-To-Be-Productive.svg)

(Rust 2019 Survey Results)
]

???

In a word, learning curve. For the Tenable folks, Rust worked well. But we know that Rust is not working for a lot of people.

Here is some data from the 2019 Survey. We didn't generate charts for this from the 2020 Survey, but I don't believe it has changed.

In this question, we asked people how long until they felt productive. You can see that for many folks, it's less than a month, but there's a big chunk that say they don't feel productive yet. Well, they're probably all beginners, right?

--

.notproductive[![Arrow](content/images/Arrow.png)]

---

# Some folks never do

.center[
![How long have "not productive yet" folks been learning Rust?](./content/images/22-unproductive-expertise.svg)

(Rust 2019 Survey Results)
]

???

We thought the same thing, so we looked at how long people who said they didn't feel productive had been using Rust. Turns out-- quite a long time!

--

.fewmonths[![Arrow](content/images/Arrow.png)]

???

Many people use Rust for month a few months.

--

.neverproductive[![Arrow](content/images/Arrow.png)]

???

Even as long as three years! This is not great.

If we want to get to the point where Rust is used for everything at scale. We have to do better. A lot better.

---

# Rust rocks 🎸...

--

## ...once you learn it 😬

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

I recently heard the best phrase ever to describe this. It is very true. Today, getting used to Rust still takes time. Once you do, though, it's really rewarding.

The metaphor works the other way too: with a lot of languages, everything feels great at first, but the hangover comes when you try to manage the maintenance or the bugs.

---

# Don't know if you heard...<sup>1</sup>

We're the, um, most loved language on Stack Overflow for like 100 years running now.

Just sayin'.

.citation[
  <sup>1</sup> Actually, I'm pretty sure you did. That's the joke. Get it? See???
]

???

The "most loved" question is "people using Rust want to keep using Rust". I know I do.

I hear a lot of people saying "At first I used Rust to write some powerful thing. But then I had some old script I had written and I rewrote it in Rust. It turned out to be about the same length, but it runs faster, and it's easier for me to refactor it now." 

The fact is, once you've got your groove in Rust, it's really great! You can grab packages from cargo! You can write high-level code like iterators, for loops, etc, and things run super fast!

---

# Goals of Rust

* Prove it can work ✅

--
* Widespread adoption, sustainability ✅

--
* Become an industry standard ⏳

---

# How do we get there?

--

.center[
.p60[
![Evangelism](https://raw.githubusercontent.com/rochacbruno/rust_memes/master/img/strikeforce.jpg)
]
]

.citation[
  Seriously though, the whole Rust Evangelism Strike Force thing kind of annoys people. Don't do that.
]

---

# How do we get there?

### Today: Productive in Rust in 3 months

### Goal: Productive in Rust in 3 weeks

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

Rust's second edition.

Editions let us make otherwise impossible changes.

As always, we don't split the ecosystem:

* Rust 2021 fully interoperate with Rust 2018 and Rust 2015.
* Tooling handles the migration for you.

---

# Rust 2021 Edition

## Enabling better format strings

```rust
let mut x = 22;
println!("{x}");
```

---

# Rust 2021 Edition

## Changing closure captures

```rust
let tuple = (String::new(), String::new());
let print_0 = move || println!("{}", tuple.0);
let print_1 = move || println!("{}", tuple.1);
```

---

# What does Rust in 2024 feel like?

--

Uh, I don't know yet.

--

But we're gonna figure it out!

---

# Async vision doc

![2021-07-17](content/images/2021-07-17-Blog.png)

???

Earlier this year we undertook a new kind of exercise.

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

# Not good enough?

Considering generator syntax:

```rust
async fn* add_one(
  input: impl AsyncIterator<Item = u32>
) yield u32 {
  while let Some(i) = input.next().await {
    yield i + 1;
  }
}
```

---

# Benefits all users alike

The <q>shiny future</q> rests on a lot of pieces:

* Type alias impl trait: `type Foo = impl Bar`.
* Impl trait in traits: `fn foo() -> impl Trait`.
* Generic associated types: `type Foo<'a>`.
* Const generics `SmallBox<22, T>`.
* Improvements to `dyn` trait.

???

---

# In closing...

* Future so bright, you gotta wear 😎
* Rust is seeing more use, and more investment, than ever before.
* Rust is going to get both easier to learn and more powerful.
