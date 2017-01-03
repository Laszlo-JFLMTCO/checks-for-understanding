## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?  
Cookie is a file stored on our computer that web applications rely on storing details about the user's interaction with the web application that can be used later on to further enhance end user experience. Details such as pages visited, etc.
* What’s the difference between a session and a cookie?  
The lifecycle of a cookie is generally longer than a session. Session's lifecycle is limited for the duration while the browswer window is open. Cookies can be available even after days/weeks, beyond browser sessions, even after computer restarts.
* What’s a flash and when do you want to use flashes?  
Flash is Ruby's built-in hash to easy transfer status details between the various part of a Rails application. We generally use it to let the end users know of the output of an end user action and/or controller operation.
* Why do people say “HTTP is stateless”?  
We say "HTTP is stateless" as HTTP itself does not maintain any tracking of the requested operation. It is more a command=-control type of protocol, where once the command sent and response provided any new request is treated as brand new and not in the context of any previously received one.
* What’s authentication? Explain.  
Authentication is the process to confirm who the user is and that the user can have access to the web application.
* What’s the difference between authentication and authorization?  
Authorization is different from authentication in a way that while authentication confirms who the user is, authorization determines what features of the web application the user is allowed to use.
* What’s a before filter?
* How do we keep track of a user once they’ve logged in?
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
* At a high level, what tools can you use to implement authorization? How would you use them?
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
* What are some strategies you can use to keep your views DRY?
