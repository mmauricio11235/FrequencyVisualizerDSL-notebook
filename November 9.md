# Design notebook for week ending November 9, 2014

## Description


This week, i focused entirely on familiarizing myself with the [Java Sound API](https://docs.oracle.com/javase/tutorial/sound/sampled-overview.html) and [ScalaFX](http://www.scalafx.org/) library, specifically using [this tutorial](http://codingonthestaircase.wordpress.com/2013/05/17/getting-started-with-scalafx-compile-and-run-2/). So far, I have read through the manual for the Java Sound API and have actually started to build a simple application to familiarize myself with the tools. The Java Sound API took much more time to get use to than I originally anticipate because I really wanted to familiarize myself with the resources that are available, and several measure and tools were things that I wasn't familiar with. Overall, I was able to find the base information I needed for my project. These include things like how to start, pause and stop audio file playback, how to get level/amplitude of audio, and other general resources. 

I also started [reading threads on what makes up music frequency bars](http://sound.stackexchange.com/questions/23739/can-someone-please-explain-to-me-what-each-bar-of-the-equalizer-means) to give myself a better context of how they're generally made. 

Fortunately, the Java Sound API is powerful and has plenty of resources online for nearly any question I could have, which means using it for my DSL should work well. ScalaFX has been nice to work with so far, but I still need quite a bit more exploration. 

A relatively major question that I am trying to figure out is what format of music file I will allow users to use, since Java Sound only allows for a couple of [music files](https://docs.oracle.com/javase/7/docs/webnotes/tsg/TSG-Desktop/html/sound.html). I feel like most people would want to use .mp3 files since they are generally the most common available. 

My current goal is to continue working with the Java Sound and ScalaFX and attempt to build a music frequency bar, since that is ultimately the minimal form of visualization I would like the DSL to be able to produce. By Next week, I also hope to have a formal specification of the syntax in EBNF. 

I am one of the organizers of the 5CHackathon and plan on not competing and will be spending the entire night working on this project!  



## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Because I spent a majority of my work time this week learning about and familiarizing myself with Java Sound and ScalaFX, I still haven't designed what my language will look like, so that is definitely the most pressing issue I have right now. 

Fortunately, getting to work with these tools is helping gain a better understanding of what is possible to do with the DSL. My hope is that attempting to build the music frequency bar using the tools as they come will give me more insight on what would make it easier to make, and can then be introduced as tools in the DSL.

The way that I'm hoping to evaluate my design is based on whether creating a unique and interesting music frequency bar is significantly easier using my DSL, and also whether the DSL has the potential to be generalized to music visualization as a whole.  

**What questions do you have for your critique partners? How can they best help
you?**

So far I've been focusing on only using ScalaFX and Java Sound. Are there any other tools that might be helpful ? 



**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

8 Hours, spent mainly reading documentation on Java Sound and ScalaFX, as well as building small sample applications in each. Also read up on general things I needed to know about music to be able to create a visualizer. 

## Post-critique summary

The main area of concern for my critique partner this last week was that I may not have a full grasp on my domain yet, and that it would make the language design difficult. Overall, she felt that I needed more research and a clearer definition on what my DSL would actually allow the users to do. 

## Post-critique reflection

I completely agree with the criticism that my main focus right now needs to be on the language design! It's been something I've been thinking about a lot and have struggled with. I realized that I didn't have the greatest understanding of the domain and needed to study more on the area of music visualization in general. I'm hoping that by the end of this week, I'll have a better grasp on the domain and be able to more eloquently define my design and implementation ideas. 

