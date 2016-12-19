## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?  
`rails new <project_name>`  
Typically we would add the following options:  
  * -database=postgresql  
  * -skip-spring
2. What do Models generally inherit from in rails?  
ActiveRecord::Base
3. What do Controllers generally inherit from in a rails project?  
ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?  
`resources :horses, :only => [:show]`
5. What rake task is useful when looking at routes, and what information does it give you?  
`rake routes` This task would provide us a list of all available routes, for each routes listed the following details:  
  * path helper  
  * path  
  * controller#view definition
6. What is an example of a route helper? When would you use them?  
`horses_path` would provide helper for the `/horses` path that would by RESTful convention render the `index` view that would typically show a list of all horses. We would use the route helper to reference the same path throughout our application, both within our `views` and `controllers` where a path is needed.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?  
`_url` would provide absolute path, that would include the domain details along with the path. Example: `http://testsite.com/details`.  
`_path` would provide relative path, that would be relative from the application root. For the above example: `/details`.
8. What are strong params and why are they necessary?  
`strong params` is a collection of params that our application would receive and we would allow to pass through to our `model`. Using `strong params` allows us to control what params can directly go to our model without any additional processing evaluation on the `controller` side.
9. What role does `form_for` play in helping us create our forms?  
`form_for` helps us to set up the `html form` details, such as what `variable` to capture the input fields and what action the form would have upon submission. It also offers options to format the form itself.
10. How does `form_for` know where to submit the user's input?  
`form_for` knows it based on the input variable(s) we assign upon `form_for` defition.
11. Create a form using a `form_for` helper to create a new `Horse`.  
```ruby
<%= form_for @horse for |f| %>
...FORM DETAILS...
<% end %>
```
12. Why do we want to validate our models?  
To ensure that the columns we defined are populated prior to writing into the database table => the database table will contain rows with the key details available for the proper function of our application.
