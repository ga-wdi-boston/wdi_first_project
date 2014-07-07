Entities are the "things" in you application. One can look for entities in user stories or requirements.

__note__: The _italicized comments are how to combine entities_

* GuestUser - _(No entity needed for a user not registered)_  
* User - email, password, address, ...
* Critic - email, password. _(Combined this with User. User has a flag to indicate it's a critic)_
* Site Admin - email, password. _(Combined this with User. User has a flag to indicate it's a site admin)_
* User Profile - full name, address, phone. _(Made these properties part of a User entity)_
* Address - street, city, state, zip . _(Make this Polymorhpic)_
* Movie - title, release year, short desc, full desc, rating, duration,
image, trailer.  
* Cast - _(Made this a property of Movie. List of name in Cast)_
* Director -  _(Made this a property of Movie. Director's name)_
* User Review - comment, rating (1-4)  
* Critic Review - comment, rating (1-4), similar movies, review categories(?)  
* Avg Review. _made this a property of a Movie_  
* Genre -  
* Search - category/genre, title, rating, released year  
* Netflix Queue - API Url, token/keys, position
