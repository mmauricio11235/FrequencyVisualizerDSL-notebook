# Design notebook for week ending November 23, 2014

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

This week was a bit rough overall, but ultimately I ended up making a lot more progress than I expected. After spending over half of my work hours struggling to get libraries to work with scala, and attempting to learn how to handle several different aspects of third party libraries, I decided that I needed to focus more on the actual implementation of the language, and to do so I should try to work with libraries and languages I'm familiar with. I am writing the language entirely in Java, and using the Williams College objectdraw library for simple graphics and Java Sound API for sounds. Once I made this decision, the actual development and outline of the language came together fairly well. I kept the same general design of the language from last week, but decided to go with Paul's advice and made it an internal language. Here is an example program and it's output: 

<p style = "text-align:center;">
<img src="/Prototype-code1.jpg" style="width:800px;height:600px;"/>
</p>

<p style = "text-align:center;">
<img src="/Prototype-Image.jpg" style="width:500px;height:500px;"/>
</p>

Because this is an internal DSL, the user can take advantage of built in java features like for loops to significantly cut down the amount of code they need to write if it's mainly the same thing being made over and over, just for different frequencies. Here's an example: 

<p style = "text-align:center;">
<img src="/Prototype-code2.jpg" style="width:700px;height:500px;"/>
</p>

**Note**: The Thread sleep line is not necessary as it is handled elsewhere in the DSL. 

Currently, the only effect that has been implemented is the "Bounce" effect, which essentially takes the given object (in this case a simple framed rectangle) and stretches it to the desired height based on the amplitude at that moment of the frequency it represents. However, because this is simply a conditional check in the code itself, the DSL can have any number of effects implemented fairly easily by just adding more methods when desired. Ideally I would have liked to find a way for a user to describe an animation themselves and given them full creative ability in the DSL, but that is a goal I hope to attempt at a later time.

The biggest let down of the week for me was not being able to understand Fast Fourier Transforms, which are what every resource I found online say is necessary to do the kind of analysis necessary to get amplitude/frequency information on the sound clips. The libraries I found that could do FFTs efficiently are a bit complicated and would take more time than I had to understand. Even if I could get an FFT library to work, I don't really understand what the return data structure represents nor how to use it. I started reading over several resource such as: 

* [FFT overview](http://hyperphysics.phy-astr.gsu.edu/hbase/math/fft.html)
* [Stack overflow](http://stackoverflow.com/questions/7674877/how-to-get-frequency-from-fft-result)
* [Stack Overflow 2](http://stackoverflow.com/questions/4708613/graphing-the-pitch-frequency-of-a-sound) 
* [Wikipedia](http://en.wikipedia.org/wiki/Discrete_Fourier_transform)
* [Java implementation of fft from Princeton](http://introcs.cs.princeton.edu/java/97data/FFT.java.html)
* [Java library for FFT](https://sites.google.com/site/piotrwendykier/software/jtransforms)
* [More stack overflow](http://stackoverflow.com/questions/6740545/need-help-understanding-fft-output)
* [More FFT library](http://www.fftw.org/download.html) 
* Plus many others i skimmed through....
## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

There are a couple of pressing issues that I am facing right now: 

* While the language should be laid out in the way the examples are shown, there is no real way for the DSL to enforce it to be laid out that way. Currently, it will just assume this is the order that the user is defining elements and attempt to add the described attributes to what would make sense. For example, if you describe an effect before a frequency, the DSL will attempt to match the effect with the last image to have been added to the visualizer. 
 
* For the sake of getting some form of language up and running for the prototype, I decided to create pseudo-frequency amplitude data. This means that I created a method that created what I thought data being brought in from the sound clip should look like. This is why the prototype looks a bit funky. I've looked into how to do the necessary analysis of the sound clips, and it is fairly complicated and requires the use of other 3rd party libraries that will take time to get to work. Even then, I would still need to work with the returned information to put it in the format I need.  
* I haven't implemented the logic for defining different time ranges for the DSL, so no matter what ranges the user defines the DSL to show, it will always add more objects on top of the previous ones instead of only showing them when they should be shown. 
	* This will be a matter of more strictly associating nested elements of time with that time range, which hopefully won't be too large a change in the structure of the DSL code. Will just take some time to implement. 
* I still only have 1 effect available in the DSL (I hope that's ok for a prototype). Adding more effects over the next two weeks will be a priority.
* I worry that giving the users flexibility in what they make is dependent on their ability to add to the DSL backend itself, which isn't ideal. I'd like to find a way to give them more freedom. 
* I'm starting to debate if the amplitude definition is even necessary. I included it in the above example to show the general structure of the DSL, but it isn't absolutely necessary to get the result. I feel that this could be an interesting piece in giving users more flexibility on what happens when certain thresholds occur. So if the highest amplitude of a sound clip occurs, the user could define what happens. 
	* If this is the case, I'd have to rethink the logic behind how the DSL should be constructed. Fortunately this should be a quick fix. 
* I still have the syntax for creating object that the objectdraw library utilizes, which is not ideal. Ideally, the logic of where items should be placed for certain effects should be handled by the DSL and not by the user. This should hopefully be an easy fix.

**What questions do you have for your critique partners? How can they best help
you?**

* Do you have any tips on how to handle frequency/amplitude data from sound clips? All the resources I've collected point to the use of Fourier Transformation and libraries that implement them, but they all will take some time to go through. Any sample code or resources would be nice! But I understand that it's a bit of an odd request. 
* What is your general feeling about how the DSL looks? Are there any things that could be optimized? 
* What are some things the DSL is missing that would be very necessary for a frequency visualizer (or music visualizer in general?) 
* Does the general syntax make sense? 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent about ~16 hours, unfortunately over 6 hours of my work time was struggling to get Scala to work, which I eventually gave up on to try to make actual progress. This doesn't include time taken to critique my partner's work from last week. 

* Struggling with Scala (6 hours) 
	* **Trying to get Minim library to work** 
	* **Trying to get Java Sound to work well with Scala**
	* **Trying out any other Scala library for graphics or sound**
	* **Trying to work with [ScalaFX](https://github.com/scalafx/scalafx)** 
	* **Learning about Java2D (gave up and used objectdraw instead)**

* Trying to understand Fast Fourier Transforms and looking at libraries (2 hours)
* Getting sound clips to play correctly (1 hours) 
* Looking over objectddraw API and old objectdraw projects (1 hour)
* Getting an applet running (1 hour) 
* Laying out the framework for the DSL (1 hours) 
* Adding semantics to the DSL (4) 


## Post-critique summary

Paul's feedback was incredibly helpful! He pointed out almost immediately that I should probably be aiming for an internal DSL, which makes a lot more sense given the general structure of the DSL and how I can use Java utilities to help the user write in the DSL. Apart from that, the structural suggestions and questions for the DSL were very helpful, and I hope to include them more as I progress with the project. 

## Post-critique reflection

The creation of this DSL had challenges that I honestly wasn't expecting, and now that I'm focusing more on the actual language implementation and not so much the more technical details, I'm glad that these questions on actual language design are actually coming out. If I spent a majority of my time trying to figure out how sound analysis works in Java instead of fixing and pointing out weaknesses in the language, the DSL could have gone to waste before it was even started. 

Right now, I'm completely fine (at least personally) with using psuedo-data while I try to make sure my language makes sense and can actually be used to make things. My ultimate goal is to get a language that works well with this pseudo data and can be used. Once that is completed, the challenge of understand sound analysis can be a higher priority. 