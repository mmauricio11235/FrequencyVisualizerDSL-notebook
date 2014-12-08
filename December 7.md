# Design notebook for week ending December 7, 2014

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

This week I focused on making sure that the nested structure of the language was actually binding the inner structures to the outer structures. This turned out to be quite a bit more challenging than I thought. While it was great that I was able to get a simple running version without this binding, it made creating the binding a bit difficult to do later since a lot of the code originally written was done so without the binding. 

Although it took a lot longer than I thought to get this part of the code restructured, I'm really happy that I was able to do so. It allowed me to rethink a lot of the structure of the language and see what was difficult to understand in the backend, which generally meant it didn't make sense in the language itself. I decided that amplitude was a structure in the language that isn't absolutely necessary, and therefore isn't required in the language structure. A user can add amplitude as an extra form of control of what happens, but the language can be used without it. 

Additionally, I was finally able to get the time constraints the user defines to work correctly. While I was really excited that the DSL works the way i was hoping, I'm not sure that the normalization from 0-100 for time constraint (and other structures) is as intuitive as I would have hoped. It made it a bit difficult for me to make things happen at the exact time that I wanted. What would be nice is to have some way for the user to know how much time has gone by (from 0-100) so they know when to have the time constraints. 

My next problem is that I haven't done much error handling yet, but I know where to handle those errors and should be able to do that in a short amount of time (granted I did say that about restructuring the code this last week too) So I hope to spend time on that before the final project is due. 

I was able to add a new effect, but due to trying to fix time constraints and other issues in the project, I wasn't able to get the more flexibly effect interface working. This effect would ideally allow users to create their own effects by defining things that are necessary in an effect. I hope to get this working so I don't have to hard code too many more example effects and can leave it up to the user to do so. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**
 	
* Need to continue adding a few more effects
* Need to do error handling and messages
* Would like to work a bit on Sound Analysis and working with FFT libraries (looking fairly unlikely given the amount of time I have left) 
* Want to find a way to simplify the time constraint 0-100 so it's easier for the user to know when to create this constraints. 


**What questions do you have for your critique partners? How can they best help
you?**

* Do you think that having the time constraint and frequency constraint at 0-100 makes sense?
*  Would adding a time counter while the visualizer plays help users know what time they want to create the intervals for?
*  Do you have any other ideas for how I can make defining the time more intuitive? 
*  What would you say the most critical things I need to implement before the end of the project are? If I had to choose 3 things to spend this week doing, what should they be?  


**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

**8 hours**

* 1 hour critique
* 3 hours restructuring code
* 2 hours working on time constraint functionality
* 1 hours getting new effect to work correctly
* 1 hour journal entry


## Post-critique summary

Matt brought up very good points as to whether or not it makes sense to have very strong requirements for bindings vs. giving users flexibility and was able to bring up very valid concerns as to the ease of use of the DSL. While there are pieces of the DSL that are fairly simple and straight forward, it can require quite a bit of code to get the sections to work the way the user wants when they want it. 

## Post-critique reflection

This project has been very eye opening to the challenges and diversity of approaches there are to language design. While I spent a lot of time in the beginning of the project trying to come up with a language that was perfect for all situations, I now see that there are always going to be pros and cons to any design decision I make. While I hope to keep adding changes to make the language even more simple and intuitive as I go, I now feel the need to always keep a running list of the weaknesses the current language has and look for ways that they can be simplified in creative way, such as good error messages or taking advantage of existing java tools. 

My current concern is to try to keep making the language more intuitive by asking for more feedback before the end of the project. 
