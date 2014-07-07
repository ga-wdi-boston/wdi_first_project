# WDI First Project 

For the first project you will use your knowledge of front and back-end web development to produce an awesome web application that can be used by friends, family or any of the other billions of people who use the Internet. The type of web application you create is your choice.

The objective of this project is to:
* To apply knowledge by building a web application from the ground up.
* To demonstrate mastery of topics covered during this course.
* Showcase your abilities to potential employers, friends, family, and community members.


## Rubrics
[WDI Project Rubric](WDI_Project_Rubric_WDI_BOS_4.pdf)

## PLANNING & DELIVERABLES

*  **User Stories or tasks.**
	You will want to create a set of small stories or tasks that you can
	implement. 
	* [User Stories](http://www.mountaingoatsoftware.com/agile/user-stories) 
	* [Using “Given-When-Then” to Discover and Validate Requirements](http://ebgconsulting.com/blog/using-given-when-then-to-discover-and-validate-requirements-2/)  
	* [Writing good user stories](https://www.youtube.com/watch?v=DaqyLWOEObY)
* **Concept** What is your conceptual model? From the above user stories create a object/entity model that can be used to communicate the objects or entities in you application.

	_Show your conceptual model to another developer and explain!_  
	
	* [Crows feet model](http://www.tdan.com/view-articles/7474)
		Probably don't need all the detail shown here.  
	* [Domain Modeling](http://www.agilemodeling.com/essays/initialRequirementsModeling.htm#DomainModel)
	* [Data Modeling 101](http://www.agiledata.org/essays/dataModeling101.html)
	
	Conceptual models are _only_ a tool used to communicate with others and as 
	a high-level model in your head.
	
	They are __NOT__ a diagram of the DB schema.
	
	They can use different modelling syntax such as Crows Feet, UML, etc. 
	
	Entities in a model can be extracted from user stories.

* **Relationships** What are the relationships between the entities in your object model. Relationships typically have names that explain the relationship.

	For example. A User may be subscribed to one or more magazines. The Entities are __User__, __Magazine__ and __Subscription__. The __Subscription__ is the relationship between Users and Magazines.
 

* **Scope.** 
	* What features will it have? 
	* What do you reasonably think you can implement in the time period?
	* Don't overdo it. 
	* Keep it simple. 
	* Prioritize you user stories or tasks. 
	* Complete the "easy" and most essential stories first.
.  
* **APIs**
	* Finding an API. 
		* [ProgrammbleWeb](http://www.programmableweb.com/)  
		* [List of Open APIs](http://en.wikipedia.org/wiki/List_of_open_APIs)  
		* [Government APIs](https://www.data.gov/developers/apis)  		* [Non profit APIs](http://projects.propublica.org/nonprofits/)
		* [Sunlight Foundation APIs](http://sunlightfoundation.com/api/)
		* [Yoda Speak API](https://www.mashape.com/ismaelc/yoda-speak#!documentation)
	* How often does the API content change? Does the data returned from the API change once a decade? 
	
		* For example, US Census data changes once every ten years.  
			 It would be error prone, wasteful and inefficient to request data for every HTTP Request handled by Rails.
	

		* Alternative is to run a background job that will re-populate data in the app DB from the API on a periodic basis.  
			This background job could be scheduled or it could be run manually
			by executing a ruby script or rake task in the production environment. 
		
		* One could "cache" the API data in your DB. 
			1. Check if the data being asked for already exists in your app DB.  
			2. Get data from the DB.
			3. Or, get data from the API.
				* Store the results in the app DB.
				* Subsequent requests for this data will be retrieved from the DB.
		
		* Use the publisher/subscriber or queuing pattern to _fire_ off API requests and return to the user immediately. The calling of the remote API is handled _asynchronously_.  [Heroku Background Jobs with Queuing](https://devcenter.heroku.com/articles/background-jobs-queueing)

	* How often does the structure of the data returned from the API change?
	
		If the data from the API changes it's structure you may have to rewrite code that depends on this structure.  __(Probably not a concern in this project)__
		  
	* How good is the API documentation?  
	   
	   Perhaps you'll have to explore the API with a tool such as curl. Or write small Ruby programs to exploer the API?
	     
	* Is there a Ruby Gem that can be used to access the data?  
	* Is there a way to get a data dump that can be used to populate you local DB?  
		If a data dump, CSV file maybe, is available you can populate you app's DB and avoid using an API and it's problems.  
		
		But, you'll have to periodically sync you DB with remote data.
  	    
  	    [Open Government Data](https://www.data.gov/)  
  	    
* **Ruby Gems**
	You should search for a Ruby gem that will help you build your app. You do not want to re-invent wheels. 
	 
	Your API may have a Ruby Gem that wraps the API and makes it much easier to work with.  
	You should "evaluate" the Ruby Gem. 
	* [Exploring Rubygems](http://railscasts.com/episodes/384-exploring-rubygems)
	* [Ruby Toolbox](https://www.ruby-toolbox.com/)

Final project deliverables:  
* Link to Heroku hosted project  
* Link to source code on GitHub  


### Example application.

I want to create a Movie Review site. Guess users can see reviews. Registered users can write a review and professional movie critics can write a detailed review and associate other _"like"_ movies. 

* [Example User Stories](user_stories.md)  
* [Example Application Entities/Classes/Models](entities.md)  
* Example Object/Domain Model (TBD)

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
