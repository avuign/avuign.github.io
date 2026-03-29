---
title: "Projects"
---

## What is spacetime made of ?

I'm trying to understand what are the building block of space and time themselves. As strange as this question might sound, the last 50 years of fundamental physics taught us that instead of being fundamental, spacetime can be an emergent phenomena, much like temperature emerges from the motion of a large number of particles. What are the "particles" building up spacetime ? How exactly do they interact ?

Those are the questions I'm exploring in my research, where I essentially study the simplest models I can think of that exhibit gravity-like properties when we look at a large ensemble of particles. This is the core idea behind the [holographic principle](https://en.wikipedia.org/wiki/Holographic_principle).

Finding such models is quite hard, but we know some examples coming out of string theory. I study what I think are the simplest of those models in terms of complexity, and try to understand why exactly those models are holographic. Understanding what is the crucial mechanism of particles interactions that lead to an emergent geometric description satisfying the laws of general relativity would be a fundamental breathrough in the field.

---

## How do computers work ?

In parallel of my dreams about spacetime, I'm also interested in more down-to-earth things, and in particular computers. In my journey of trying to understand how they work I came accross the [boot.dev](https://boot.dev) platform. There I could strengthen my python skills, learn about memory managment in C,backend developement using Golang and SQL and so much more. You can follow my progression on my [profile](https://www.boot.dev/u/hatom).

---

## How do computers think ?

I've been interested by machine learning and artificial intelligence for a long time, but I finally decided to actually invest into learning it after participating to a workshop on [artificial intelligence for high energy physics](https://indico.global/event/14060/).

There we quickly saw how deep neural netwok work, and how to train a machine to recognize handwritten digits. Since I wanted to understand things from the ground up, I replicated the exercise by coding every function from scratch to be sure I understood the logic. You can see the result on my [github](https://github.com/avuign/MNIST).

Then, wanting to go further and ultimately to learn LLMs, I started by implementing a simple [character-generation model](https://github.com/avuign/char_lm). This model is trained to guess the next letter in a word, and can then be used to generate new words, or names. This was a small increment from the digit recognition, and therefore took the opportunity to also learn how models can learn via distillation, something I implemented in the project.

The next step is to have real text generation, and for that I'm working through Sebastian Raschka's book *Build a Large Language Model (From Scratch)* to learn how to implement a GPT-style model step by step in PyTorch. The goal is to understand transformers at a low level: tokenization, attention, training loops, and text generation. My current progress is [there](https://github.com/avuign/femto_chatbot).
