# Design notebook for week ending November 2, 2014

## Description


This week, I tried to explore currently existing DSL’s to come up with a potential project idea. Once I decided on a topic I thought might be interesting in, I searched around to see what kinds of tools currently exist. My initial project idea is to create a DSL for the creation of music visualizers. My hopes is that I will provide the necessary general animations so the user doesn’t need to worry about the code that creates the animation, but also provide enough tools in the language that the user can define how the animation reacts to the music and give users enough flexibility to make what they want. 

###Here are a couple currently existing software projects 

#### VSXu:
[Video of VSXu](http://youtu.be/iJaQxibbaR0)

[VSXu Website](http://www.vsxu.com/for-programmers)

####Music visualizers using a Photoshop After Effects:

[Example Visualizer](http://youtu.be/yNdhfrIz6Ug)

[Tutorial for After Effects](http://layersmagazine.com/audio-visualization-in-after-effects.html)

####Another 3D tool: VST Plugin (Not Free)
[Website](http://createdigitalmotion.com/2012/12/3d-music-visualization-powerful-editing-rendering-now-as-a-vst-plug-in/)


Following researching the other available tools, I tried to identify some areas where I feel they could improve or become more accessible. Here are a few things that I have thought of thus far: 

* Price. Several of the tools available are not free
* Simplicity: Tools like VSXu are not very well documented and seem fairly difficult to navigate
* No actual language to code in: These all seem to be tools that allow drag and drop to create visualizers, but none seem to allow users to code in a more traditional sense.  

###Trying to image what the language will actually look like: 

Given the observations described above, I am looking for motivation from [ContextFree](http://www.contextfreeart.org/) and trying to see if there is a way to create a DSL similar to ContextFree that would allow users to start with simple definitions and create larger projects from simpler elements. The question that I have for myself now is what are the actual tools available? Here are some areas that I feel need to be taken into account when creating the music visualizer. 

* Animation: Effect, magnitude of music effect on animation, transitions, shape, number of objects in animation. 
* Object: Individual effects including change of color, distance from other objects in animation, and change in size. Also relationship in proportion between objects
* Allow users to define their own unique shapes somehow? 
* Could I allow the user to define the shape of the bar instead of only allowing flat bars [like the example visualizer I provided earlier?](http://youtu.be/TS7Yq7OQRqA)   


### What tools are available for use
Implementation is a big concern for me, as I will be depending heavily on tools that are already available for manipulating and analyzing sound, which will effect animation, and also tools available for displaying graphics and creating animations. Here are a few that I have found so far

* [An explanation on using Java and JavaFX to create visualizers](http://www.oracle.com/technetwork/server-storage/ts-4842-1-159016.pdf)
* [Cool java project on visualizers in java](https://github.com/michaelbrooks/music-visualization)
* [Tutorial for ScalaFX](https://github.com/scalafx/ScalaFX-Tutorials)
* [mp3 to wav format in Java](https://code.google.com/p/mp3transform/source/browse/trunk/mp3/src/mp3/wav/WavConverter.java?r=6)
* [Parser Combinators](http://bitwalker.org/blog/2013/08/10/learn-by-example-scala-parser-combinators/)

###Language Design


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

The most pressing issue right now is that I don't have a very clear vision on what an actual completed program will look like. The design decisions I need to make right now are very dependent on being able to fully list everything that the user needs to create the visualizer, then figure out the syntax that most clearly and simply allows the user write in the DSL and have it do everything they need. 

Once I have an example code snippet and a formal specification, I can further plan what is necessary for me to be able to implement the DSL. 


**What questions do you have for your critique partners? How can they best help
you?**

* Do you know of any other way that I can think about the animations? Right now I've been thinking about using hiding and showing of objects to represent the bounce on the sound bar, but haven't given much thought to how I might allow the user to define animations, or if that's something that's something that can be created by the end of the semester. 
* What are some things that I've missed so far that I should be implementing? Are there parts to music visualizers that I haven't discussed in my description? 
* Do you know of any tools or project currently available that might give me some insight on how to implement this DSL? I've found a couple projects for people who have written music visualizers, but haven't seen any that allow for user defined changes. 
* Are there any aspects to the project that seem overly ambitious? Or not ambitious enough? 
* Any further ideas or criticisms on how I'm thinking the user will write in the DSL. 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

* 8 hours

## Post-critique summary

## Post-critique reflection
