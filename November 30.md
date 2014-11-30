# Design notebook for week ending November 30, 2014

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

This week I wasn't able to spend nearly as much time on my project as last week due to having family visit and taking up almost all my time. However, I was able to work on my evaluation which allowed me to reflect on some of the design decision for the DSL. Outside of that, I spent some time working on organizing the code to make it cleaner and better structured for changes that I will need to make later. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**<span style = "text-decoration: underline;">The most pressing issue that i have right now are</span>** 
<ol> 
<li> Getting the time structure working as it should be working</li> 
<li> Ensuring the binding of nested object with outer objects</li>
<li> Adding more effects for the users </li> 
<li> Doing sound analysis to connect sound with visualizer </li> 
</ol>

I described some of the challenges in implementation more in detail in the evaluation document, but as of now this is the ranked list of things that I'd like to have implemented by the end of the semester if possible. The first two items in the list are fairly simple and just require organizing the code well. Adding more effects will require creativity on my part which is combined with what the user could potentially need to create interesting visualizers. The sound analysis is incredibly important to any music visualizers, but as this project is supposed to emphasize the language design and not my ability to learn some of the more complicated details of sound analysis, I want to focus on things important to the language before getting into analysis. I foresee that part being the last piece I attempt before the project is due. 


**What questions do you have for your critique partners? How can they best help
you?**

* One of the criticisms that I received was that my language isn't very intuitive as is now. The [recommendation seen here](https://github.com/mmauricio11235/FrequencyVisualizerDSL/blob/master/critiques/November%2025.md) shows what Chloe believes would be more intuitive, but it is difficult to do in Java. One possibility is to use camel case, but then it's just very long names. Do you have any other ideas? 
* Do you have any resources on Fourier Fast Transforms (FFT's) such as example projects or simple libraries that I might be able to work with. 
* Do you think that there needs to be a strict binding of amplitude to frequency? Do you think that a strict structure makes the language simpler to work with? 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

Total about 4 hours

* 1 hour on Critique
* 1 hour on Evaluation
* 2 hours working with the code, mainly cleaning up and adding basic structure. 


## Post-critique summary

Chloe's critique was very eye opening to me. As the person who is creating the DSL, the language obviously is going to seem intuitive to me, so I was surprised to hear that it wasn't quite as simple to pick up as I had thought. The recommended syntax doe the language was very helpful because it gave me an outside perspective on what could be simpler and easier to understand. 

It was also very nice to have a second opinion on how I should prioritize the language design and implementation over sound analysis. I was very nervous and stressed about getting it working, but can go about working on the language with a clearer head for now. 

## Post-critique reflection

The biggest thing I got was that I need to make sure to get the language design to work the way I want that is intuitive to the user. It should be very easy and simple to create a visualizer in this language, and I hope to use Chloe's criticism to do that. 