# Design notebook for week ending November 16, 2014

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Right now, the most pressing issue is to start actually developing the DSL and getting a  working prototype by the end of the week. This is highly dependent on getting feedback on the current design of the language. I'm hoping to have at least a minimum running version of the code by Sunday, but still need some time to familiarize myself with Minum, the Java sound library that was introduced to me by Matt last week. Implementation issues I'm currently facing is trying to stay organized with the heavily nested data structure format of the DSL, and trying to simplify it to make implementation a bit more reasonable. 

Another implementation 

**What questions do you have for your critique partners? How can they best help
you?**

* What are the most pressing issues with the current design of the language? 
* Do you have any recommendations for how I should approach the implementation of the DSL? 
* Do you have any advice on how to implement the DSL given that it will be changing as the music continuosly plays? What are best practices that you've seen in the past? 
* Any other general advice? 



**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**


* Critique of Matt Cook Project: 1 hour
* Figuring out ScalaFX: 3 hours
	* Trying to find documentation
	* Looking at examples
		* Fixing those examples so they work with the newest versions of scala and java 8

	* Attempting to write my own simple application. 	
* Looking over Java 2D API: 2 hours
	* Much better documentation
	* Simpler to create simple programs
	* Creating a sample app (still in progress) 
* Design and Implementation work: 3 hours
	* Reviewing feedback from Matt.
	* Discussing with friends what would make sense in a DSL for this domain
	* Designing the language in EBNF form
	* Writing up the document. 
* **Total: 9 hours**

## Post-critique summary

A majority of the concern raised my Matt was how the language would look in defining the bars of the frequency spectrum, so I spent a lot of time discussing with friends what that should look like and coming up with a design that makes sense in this context. Matt was also able to collect very very helpful libraries like Minum which I am extremely excited to explore more as they should hopefully be easier to use for the beginning phase of my DSL. Matt found very good examples of what he thought a visualizer could look like based on my description, which helped me see what kind of output I would hope to have. 

## Post-critique reflection

I completely agreed that my ideas were still a bit scattered at the end of last week, and I spent a lot of time trying to come to a formalization of what my DSL would look like in the grammar_ideal.txt file. I think that this design is a bit more intuitive and structured than what I had described earlier, although potentially a bit ambitious. I'm hoping this design makes sense to my critique partner and that they will be able to raise any questions. Now that I spent more time on the design. 