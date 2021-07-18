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

???

I remember when I started to work on Rust, in 2011, I figured it was a doomed effort.

I told myself that the first time I heard about some really cool thing and *only later* discovered it was written in Rust, that would be success. "Somebody using Rust that I don't know personally"

Well, clearly we crossed *that* threshold, so I guess it's time to set a new goal.

--

.center[.p50[
![Back in time](https://media.giphy.com/media/ZSSoLmkYURcWqKFdVA/source.gif)
]]

---

# 2015

???

But let's step back a minute, to 2015...what happened that year...


---

# 2015

???

what happened in 2015...nope, not that...

--

.center[
![The dress](content/images/the-dress.jpg)
]

---

# 2015

.center[.p50[
![Left shark](content/images/left-shark.png)
]
]

???

...nope, keep going, something else happened that year...

---

# 2015

.center[
  ![Rust 1.0 announcement](content/images/2015-05-15-Blog.png)
]

???

Ah yes, that's it!

---

.center[
Rust started with the quixotic dream of delivering the

## GREAT POWER OF C++

<br/>
*without the*

## GREAT RESPONSIBILITY 

<br/>
that comes with it
]

---

# 2015

- Plan:
  - Control and performance predictability of C++
  - Feel of a high-level language like JavaScript 

---

# Rust journey

1. Show it can work (2015)

--
2. Sustainability, adoption, production (2021)

--
3. ???

--
4. Profit (2024)

---

# "Profit?"

*Graph:* 

```
    │
    │ C++             Rust
    │
    │               xx
    │              xx
    │             xx
    │            xx
    │           xx
    │          xx
    │        xx
    │        x
    │       x
    │     xx         JS, Ruby, Python
    │    xx
    │
    └─────────────────────────────────
```

???

What happens if we truly achieve our dream?

---

# What does that look like?

Yes, traditional "systems programming" targets:

* Browsers
* Foundational infrastructure
* Kernel hacking

--

But also other domains, when used at scale:

* Websites, day-to-day business logic
* Machine learning

---

# Business logic, really?

???

Isn't that the prototypical case for agility?

Isn't programmer time worth more than computer time?

--

Yes.

---

# Why?

.font500[🖥️]

???

Well, it's true if you're running a program on one computer, programmer time is worth a lot.

---

# Why?

.font500[🖥️🖥️🖥️🖥️🖥️🖥️] <br/>
.font500[🖥️🖥️🖥️🖥️🖥️🖥️] <br/>
.font500[🖥️🖥️🖥️🖥️🖥️🖥️] <br/>

???

But what about when you're running it on a LOT of computers?

---

# At scale, even small savings add up...

.center[.font500[💸]] <br/>

???

When you're running things at scale, even small improvements can save a LOT of money.

Not just money: power. carbon.

--
.center[.font500[🌱]] <br/>

---

# ...and more so big savings

### Optimizing 700 CPUs Away With Rust<sup>1</sup>

> The Rust-based filter is much more efficient than the original implementation. With the ability to fully manage the heap allocations, Rust’s memory allocation for handling each datagram is kept to a minimum. This means that the Rust-based filter only needs a few MB of memory to operate. **As a result, we saw a 75% reduction in CPU usage and a 95% reduction in memory usage in production.**

.citation[
<sup>1</sup> [Medium article from Tenable tech blog, by Alan Ning](https://medium.com/tenable-techblog/optimizing-700-cpus-away-with-rust-dc7a000dbdb2) (emphasis mine)
]

---

# It was even pretty easy to do

Article continues:

> With this small change, we were able to optimize away over 700 CPU and 300GB of memory. **This was all implemented, tested and deployed in a single sprint (two weeks).** Once the new filter was deployed, we were able to confirm the resource reduction in Datadog metrics.

---

# We've changed *who* does system programming

![new generation](content/images/gogaruco.png)

Yehuda Katz at Golden Gate Ruby Conference 2014

---

# Let's change what systems programming *is*

Rust is the "go to" language for systems programming

???

Today, people reach for Rust to tackle the hardest problems. 

Things like the rendering engine of a browser, or the core services that underlie the internet.

---

# Let's change what systems programming *is*

Rust is the "go to" language for ~~systems programming~~

???

But I think we could do more than that.

--

Rust is the "go to" language for systems that **run at scale**.

Rust is the "go to" language for systems where **reliability counts**.

???

What if people were using Rust for anything that was going to run at scale, or for anything where reliability was really important?

I mean...why not. I don't know about you, but I at least have found Rust displacing other languages I used to use, like Python. It's nothing against those languages, which are fantastic. It's just that Rust has a lot to offer: you get cargo and easy access to great libraries like serde. Moreover, when you wield Rust well, the code can be remarkably concise and clean. The borrow checker isn't much of a bother, because you can clone or box or do other things. And when you're done, your code runs fast. Even better, you can come back after six months and still do a successful refactoring.

--

.p40[![Galaxy brain](content/images/galaxy-brain.png)]

---

# What would that be like?

--

Pretty dang great, that's what!

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

# The equation

.font150[.center[
*Cost to adopt Rust*

.font150[<]

*Savings from infra, maintenance*
]]

???

OK, so let's get down to brass tacks. If we want to see Rust used in more places, for more things, what do we have to do?

Ultimately, it comes down to a simple equation.

Of course, when you dig in, things get a bit more complicated.

As we've seen, the savings from using Rust can be substantial.

It's not just resources: also maintenance.

So, why doesn't everybody do this?

---

# What is the cost to adopt Rust?

.center[
![Time to perceived user productivity](./content/images/8-How-Long-To-Be-Productive.svg)

(Rust 2019 Survey Results)
]

???

In a word, learning curve. For the tenable folks, Rust worked well. But we know that Rust is not working for a lot of people.

Here is some data from the 2019 Survey. We didn't generate charts for this from the 2020 Survey, but I don't believe it has changed.

In this question, we asked people how long until they felt productive. You can see that for many folks, it's less than a month, but there's a big chunk that say they don't feel productive yet. Well, they're probably all beginners, right?

--

.notproductive[![Arrow](content/images/Arrow.png)]

---

# What is the cost to adopt Rust?

.center[
![How long to be productive](./content/images/22-unproductive-expertise.svg)

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

# What we should strive for

## Productive in Rust in 3 weeks

???

I think we should be aiming for a learning curve where people are productive in Rust after just a few weeks.

--

.center[.font500[.font300[😲]]]

???

It's ambitious. We all know that Rust is 

---

# How do we get there?

--

1. Understand the problems

--

2. Think about how we want Rust to feel

--

3. Take a step in that direction

--

4. Re-evaluate and proceed

---

# Async vision doc

![Building a shared vision for Async Rust](content/images/2021-07-17-Blog.png)

???

If you've been following Rust lately, you'll have noticed this effort around the async vision doc

This is a kind of first attempt to apply the process I'm talking about, within a limited domain

I expect that over the next few years we'll be repeating this experiment and this approach, trying to push ever further.

---

# Understand the problems

???

Going in, I thought I knew the problems around async.

I knew there were composition problems between runtimes, for example, and I knew that we needed to do a fair bit of polish around the compiler's error messages.

--

???

But there was a lot I didn't know. Things that arose out of 


---

# Does this mean that

---