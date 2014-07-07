## Home Page
Given I'm a guest user  
When I go to the home page  
Then I should see the last 10 released movies.  

Given I'm a guest user  
When I go to the home page  
Then I should be able to navigate to the older movies in groups of 10.  

Given I'm a guest user  
When I look at a single movie on the home page  
Then I can see the title, release year, short description, rating and duration.  

Given I'm a guest user  
When I look at a single movie on the home page  
Then I can view an image from the movie.  

Given I'm a guest user  
When I view one movie on the home page.  
Then I can see a trailer of the movie.  

Given I'm a guest user  
When I view  on the home page.  
And I click on the movie title  
Then I can see the movie's details.  

## Movie Detail Page
Given I'm a guest user  
When I view a movie's details  
Then I can see the movie title  
And I can see the movie release year, full short description  
And I can see the movie rating and duration.  
And I can see the movie's cast and director.  
And I can see the movie' average review (1 to 4 stars).  
And I can navigate to a view of all the movie's reviews.  


## User Registration  

Given I'm a guest user 
When I visit the registration page. 
Then I can enter my email address, password and password confirmation.
And I can enter my full name.
And I can enter my address.
And I can register a new account.

Given I'm a guest user     
When I fill out the registration info.  
I will be given an option to become a Critic  

Given I'm a newly registered user.  
And I have created a new account  
Then I will receive an account activation email.  

Given I'm a newly registered user.  
When I have received an account activation.  
And I navigate the activation page.  
Then I will have an activated account and be allowed to login.  

## User Login
Given I'm a registered user.
And I go to the login page.
Then I can enter my email and password 


## Logged In User stories.
As a logged in user.  
When I view a movie's details  
Then I can navigate to the add review page.  

Given I'm a logged in user.  
When I review a movie.  
Then I can enter my review comment.  

Given I'm a logged in user.  
When I review a movie.
Then I can select from one to four stars.  

Given I'm a logged in user.  
When I review a movie.  
Then I can post my review.  

Given I'm a logged in user.  
When I review a movie.  
Then I can cancel my review.  

Given I'm a movie reviewer.  
When I post my review.  
The I can view all the movie's reviews.  

## Site Admin stories
Given I'm a site administrator  
When I navigate to the user admin page.  
I can search for users by email, (username)  

Given I'm a site administrator  
When I navigate to the user admin page.  
I can select a user's profile.  

Given I'm a site administrator
When I view a user's profile.
I can make the user a 'critic'.

Given I'm a site administrator  
When I view a user's profile.  
I can delete the user.  

## Critic stories

Given I'm a critic  
When I view a movie's detail.  
I can choose a movie's genre.  

Given I'm a critic.   
When I view a movie's detail.  
I can view one of my reviews.  

Given I'm a critic.  
When I view a movie's detail.  
I can create,update or delete a review  

Given I'm a user
When I choose to send a movie my Netflix queue.
Then the movie will be marked as in my netflix queue until it is
removed

Given I'm a guest user.  
When I'm on the home page.  
And I'm on the movie details page  
Then I can search for a movie.  

Given I'm a guest user   
When I attempt to search   
I can search by category/genre, title, rating and released year.  

## Epics
Allow site admins to manage all resources.

Periodically update movie DB with most recently released movies.

Update movie DB with old movies by demand. 
User may search for a movie that doesn't exist locally which will
cause a remote query. 
If the remote query is successful add movie to DB.

Mark a user's movies that are now or have been in their Netflix queue.

Allow a user to search for movies by location, rating, critic, in-theaters.

Create producer accounts that can build embed code for a movie and
video player..

Given I'm a producer.
Allow me to manage ads into the above movie player.
<Ad network integration>




