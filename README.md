# WDI First Project 

For the first project you will use your knowledge of front and back-end web development to produce an awesome web application that can be used by friends, family or any of the other billions of people who use the Internet. The type of web application you create is your choice.

The objective of this project is to:
* To apply knowledge by building a web application from the ground up.
* To demonstrate mastery of topics covered during this course.
* Showcase your abilities to potential employers, friends, family, and community members.


## Rubics

## PLANNING & DELIVERABLES

*  **User Stories or tasks.**
	You will want to create a set of small stories or tasks that you can
	implement. 
	* [User Stories](http://www.mountaingoatsoftware.com/agile/user-stories) 
	* [Using “Given-When-Then” to Discover and Validate Requirements](http://ebgconsulting.com/blog/using-given-when-then-to-discover-and-validate-requirements-2/)  
	* [Writing good user stories](https://www.youtube.com/watch?v=DaqyLWOEObY)
* **Concept** What is your conceptual model? From the above user stories create a object/entity model that can be used to communicate the objects or entities in you application.

	_Show you conceptual model to another developer and explain!_  
	
	* [Crows feet model](http://www.tdan.com/view-articles/7474)
		Probably don't need all the detail shown here.  
	* [Domain Modeling](http://www.agilemodeling.com/essays/initialRequirementsModeling.htm#DomainModel)
	* [Data Modeling 101](http://www.agiledata.org/essays/dataModeling101.html)
	
	Conceptual models are _only_ a tool used to communicate with others and as 
	a high-level model in your head.
	
	They are __NOT__ a model for the DB schema.
	
	They can use different modelling syntax such as Crows Feet, UML, etc. 
	
	Entities in a model can be extracted from user stories.

* **Relationships** What are the relationships between the entities in your object model. Relationships typically have names that explain the relationship.  

* **Scope.** What features will it have? What do you reasonably think you can implement in the time period? Don't overdo it. Keep it simple. Prioritize you user stories or tasks. Complete the "easy" and most essential stories first.
.  
* **APIs**
	* Finding an API [ProgrammbleWeb](http://www.programmableweb.com/)  
	* How often does API contents change? Does the data returned from the API changes once a decade? For example, US Census data.
	
		If it doesn't change that often you may be asking the API for the same data for every request your app processes. This is very inefficient and could make you site unusable.
		
		Alternative is to run a background job, Ruby/Rake script, that will 
		re-populate date in the app DB from the API on a periodic basis.
		
		Or you could "cache" the API data in your DB. Check if the data being asked for already exists in your app DB. If it does get it from the DB. Else get it from the API, store the results in the app DB so that subsequent requests for this data will be retrieved from the DB.
		
	* How often does the structure of the data returned from the API change?
		Perhaps you have docs for an older version of the API?
		If the data from the API changes it's structure you may have to rewrite code that depends on this structure.
	* How good is the API documentation?  
	   Perhaps you'll have to explore the API with a tool such as curl. Or write small Ruby programs to exploer the API?  
	* Is there a Ruby Gem that can be used to access the data?
	* Is there a way to get a data dump that can be used to populate you local DB?  
		If a data dump is available you can populate you app's DB and avoid API
  	    problems.  
  	    
* **Ruby Gems**
	You should search for a Ruby gem that help you build your app. You do not want to re-invent wheels.  
	Your API may have a Ruby Gem that wraps the API and makes it much easier to work with.  
	You should "vet" the Ruby Gem. See [Exploring Rubygems](http://railscasts.com/episodes/384-exploring-rubygems), [Ruby Toolbox](https://www.ruby-toolbox.com/)

Final project deliverables:  
* Link to Heroku hosted project  
* Link to source code on GitHub  


### Example application.

I want to create a Movie Review site. Guess users can see reviews. Registered users can write a review and profession movie critics can write a detailed review and associate other _"like"_ movies. 

[User Stories](user_stories.md)
[Application Entities/Classes/Models](entities.txt)

## Suggested TIMELINE

* Tues July 8 - Draft user stories and object model.
* Tues July 8 - Project plan.
* __required__ Monday July 14 - Final project deliverables due 

## WHAT WE ARE LOOKING FOR
Make sure that your code is:  
* Dynamic  
* Flexible/extensible  
* Well-commented  
* Well-formatted  
* Follows naming conventions  

We’ll also be looking at:  
* Quality of communication around decision-making. Can you defend why you chose a certain technology or why you implemented your solution in a certain way?  
* Your ability to pick up new technologies.  
* Your ability to take full advantage of a language’s features.  
