## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
GET, POST, PUT, DELETE, PATCH
2. What is Sinatra?
It is a Ruby gem that provides webserver solution
4. What is MVC?
Model-View-Controller concept for web application development.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
So that our code is easier to understand/read by others and easier to maintain by a team of people in the future.
6. What types of variables are accessible in our view templates without explicitly passing them?
Instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
`@number_one = 1`

  ```ruby
  get '/horses' do
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed`?
  ```ruby
  get '/horses' do
    name = "Mr. Ed"
    erb :index, locals => {:name => name}
  end
  ```
9. What's the purpose of ERB?
Provide flexible templating solution to render HTML pages with dynamic content
10. Why do I need a development AND test database?
So the we can better control the test case evaluations.
11. What's responsive design?
When a webpage renders in a user friendly and somewhat consistent way independent from the device/display size that it is being viewed on
12. What is CRUD and why is it important?
Create-Read-Update-Delete main functions, important to manipulate database content through HTML browser interface
13. What does HTTP stand for?
HyperText Transfer Protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
`<%= %>` would output a value into the template. `<%%>` would run Ruby code within the template but would not print its output into the template
15. What's an ORM?
Object Relational Mapping
16. What's the most commonly used ORM?
ActiveRecord
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
18. What's a migration? 
Creating the database table structure
19. When you create a migration, does it automatically modify your database?
No, it creates the template of the planned database update/modification
20. How does a model relate to a database?
It is a how we reference an object that represents a row of a table within our web application
21. What's the difference between agile workflow and waterfall method?
Agile is used for rapid development vs the waterfall method
22. What is the difference between `#new` and `#create`?
`new` creates an object instance without saving it into the database, while `create` also saves it
