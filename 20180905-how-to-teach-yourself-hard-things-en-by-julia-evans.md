---
title: How to teach yourself hard things
author: Julia Evans
date: 20180905

---

# How to teach yourself hard things
This blog is mostly about learning computer programming / systems. Probably 70% of these posts are in one way or another about things I've learned and why they're exciting.

But how do you teach yourself hard things? I've talked before about having a [growth mindset](https://www.mindsetworks.com/science/), which is about replacing the belief "I'm bad at X" with "I haven't learned about X yet".

Having a positive attitude is really important, but IMO by itself it's not enough to learn hard things. Learning is a skill which takes a lot of work to get better at. So this blog post is about specific learning skills that I've worked on over time. They are:

- Identify what you don't understand (maybe the most important one)
- Have confidence in your knowledge
- Ask questions
- Do research

## What does learning how to learn look like?
Before we start, I want to talk a bit about what learning how to learn can look like. I'm not a teacher or anything, but here are a few things that I think helped me:

- when I was a kid, I spent 7 years doing a math program called [Kumon](https://www.kumon.com/about-kumon/kumon-method/self-learning) which is really focused on learning math independently. I learned all of elementary/high school math that way. (from multiplication to algebra to calculus). I think this was pretty important and I owe a lot to my mom (who has now been helping kids learn independently for > 20 years!!) for making sure I got good at learning when I was a kid.

- did a pure math degree, where having a clear sense of what I understand and don't understand was super important

- went to the [recurse center](https://www.recurse.com/) which is a community of self-directed learners

- I work as a programmer, where as we know teaching yourself new things is an essential skill :)

I think other ways people frequently get better at teaching themselves are:

- do a PhD (where it's also necessary)
- be homeschooled / go to a school where learning is more self-led

It seems a bit weird to put "learn some math independently when you're 8" alongside "do a PhD" but to me figuring out fractions on your own feels like the same kind of mental discipline that's useful as an adult researcher exploring new ideas.

I'm going to avoid talking about math for the rest of this post because today I spend most of my time learning programming ideas, not math ideas. So let's talk about some learning skills!

## Learning skill: Identify what you don't understand
I think this is the most important learning skill. This is the skill of translating "I'm confused, I don't get it" to "I have a specific question about X".

For example, when I was learning Rust last winter, I felt really confused about references & borrowing. It took me a while to figure out why, but eventually I realized that I didn't know the answers to the following questions: (answered in [What's a reference in Rust?](https://jvns.ca/blog/2017/11/27/rust-ref/))

- What does the & symbol in Rust actually mean?
- How can I tell if a variable in Rust is allocated on the stack vs the heap? Is it always possible to tell?
- How can I avoid putting lifetimes on my Rust structs?

Once I understood the answers to these, I had a MUCH stronger understanding of how to use references and borrowing and was permanently less confused about how to write Rust code.

## identifying what you don't understand is important (but hard)
Being good at this is a HUGE DEAL! If I weren't good at figuring out what I'm confused about, then I'd either need to:

- get someone to identify those things for me, which is pretty unlikely to happen.
- find a course / blog post / book where someone's already broken up the confusing things into the right pieces for me
- just decide not to learn hard/confusing things (which would be a disaster!!)

Even though I think I'm pretty good at it now, I still find breaking down "I'm confused about X" into specific questions about X takes work. For example, I only came up with those questions about Rust references 3 years after I'd first used Rust. The reason it took so long is that I had to decide to actually sit down, notice what I found confusing, and focus on figuring out what I was confused about. That takes time!

But I do think that this is something that you can get better at over time. I'm **much** better at breaking down what's confusing to me about a programming thing than I was and much more able to unstick myself.

## Learning skill: Have confidence in your knowledge
Identifying what you **do** understand is IMO just as important as identifying what you don't understand. For example, I don't know everything about networking. One thing I do 100% know is that there are 65535 TCP ports. That is definitely true. The src/dest port fields in the TCP header are 16 bits (2^16=65536), so there is no room for more ports.

Having pieces of knowledge that I'm really confident about is really important when trying to figure out a tricky problem. For example, imagine a program printed out "port 1823832" in a log. That is not because there are secretly port numbers can be bigger than 65535 and I've just misunderstood! That's because there's a bug in the program, there's no port 1823832. That's kind of a silly example, but I need to debug complicated issues all the time and it would be a huge waste of time to second guess things that I do actually know.

Taking a bit of extra time to take a piece of knowledge that you're pretty sure of ("there are 65535 ports, Wikipedia said so") and make it totally ironclad ("that's because the port field in the TCP header is only 16 bits") is super useful because there is a big difference between "I'm 97% sure this is true" and "I am 100% sure about this and I never need to question it again". Things I know are 100% true are way easier to rely on.

## Learning skill: Ask questions
The next skill is "ask questions". This is about taking the things you've identified that you're confused about ("what's the difference between TLS 1.3 and 1.2?") and turning them into questions to ask a person.

Here I'm just going to link to a post I previously wrote called [How to ask good questions](https://jvns.ca/blog/good-questions/).

The hardest part of asking questions for me is actually figuring out what I do and don't know. I think there are also some interesting skills here about:

- finding Slack groups / IRC channels / email lists who can help you
- mailing list etiquette
- asking questions on Stack Overflow (which I've never done successfully)

## Learning skill: Do research!
This is about:

- being good at Googling
- knowing where the best documentation is in your area
- reading mailing list archives
- having / finding books that have the information you need. Not all information is on Stack Overflow! If I'm confused about a Linux concept I'll often reach for [the linux programming interface](http://man7.org/tlpi/) instead of Googling.
- reading the source code when Google/books/the docs can't answer your questions

I'm not aware of any good guides to doing tech research, though I think that could be a really interesting thing to write up – information about different areas is available in dramatically different places (man pages? books? mailing lists?) and some documentation is MUCH better than other than other documentation. How do you figure out the landscape of where information is in your area?

## Learning skill: Recognize that being confused means you're about to learn something
One last thing that has been important for me is to recognize when I'm confused about something and, instead of feeling bad ("oh no! I don't know this thing! disaster!"), recognize that it's a normal feeling and that it just means I'm about to learn something!

I like learning! It's fun! So if I'm confused, that's usually a good thing because it means I'm not stagnating. Here's how I approach it:

- recognize that I'm confused
- figure out what the topic I'm confused about is
- turn that confusion into concrete questions
- ask someone or research to get the answers
- I've learned something new!! Hooray!

Of course, I don't do that every time I'm confused about something –sometimes I just note "ah, I'm confused about X, maybe I will figure that out someday but not today". That's okay too! Learning is a lifetime project :)

## Working on learning skills makes a huge difference
I don't really think I could have a career as a programmer if I didn't invest in learning new things. Almost everything I do in my job day-to-day is something I learned on my own, and most of it is stuff that I learned recently (in the last 2-3 years). So it makes sense for me to continue working on getting better at learning. Some learning skills I'd like to be better at are:

- figuring out when it's appropriate to use a mailing list to ask a question and asking the right questions there
- taking a large / complex piece of open source documentation and determining what information is in it and what isn't
- using open source Slack/IRC groups effectively
- finding great reference books that I can lean on
