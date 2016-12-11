## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR. 

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
ActiveRecord is a Ruby gem that helps to simplify interactions with the database. It allows us to use keywords instead of building our own SQL query strings. Also helps us to set up and manage database table associations through short keywords.
2. What kind of methods are `belongs_to`, and `has_many`? (i.e. class or instance) Give an example.
They are class methods that help us to set up one-to-many and many-to-many associations between database tables. Bike-share project related example:
one station could be associated with more than one trip => so within our `Station` model we had a `has_many: trips` association, which could be called as `station.trips` on any instance of of `station`.
3. What do they allow you to do?
See answer for #2 above and in addition these methods offer easy access to data from tables linked together through specific columns.
4. What's the difference between agile workflow and waterfall method?
Agile approach allows more rapid development with shorter development cycles.
5. What is the difference between `#new` and `#create`?
`new` creates an instance of the model, but does NOT save it in the database, `create` has the same functionality as `new` AND in addition it saves the instance into the database.
6. At a basic level, what does cURL allow you to do?
Allows us to evaluate HTTP calls through the command line.
7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
See screenshot added in the comment section.
8. Define foreign key, primary key, and schema.
__Foreign key:__ the column of the table that is used to associate it with the `Primary key` in the other table
__Primary key:__ the column of the table that is used to associate it with the `Foreign key` in the other table. `Primary key` must be a unique identified of row within that table.
__Schema:__ overview of our database table definitions (list of columns with their names and data types)
9. Describe the relationship between a foreign key on one table and a primary key on another table.
In a one-to-many database association, `Primary key` is the name of the column within the table on the `one` side of the association. `Foreign key` is the is the name of the column within the table on the `many` side of the association.
10. What are the parts of an HTTP response?
Two main parts are `header` and `body`. The `header` contains details such as the HTTP status code, the verb (GET, POST), HTTP version, the path information, etc. The body in addition can be populated with data, such as form submission details.
11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.
__Views:__ Utilize `layout` file to move all repeated ERB details into a single file, so when we render various page content, our web application can still maintain uniform appearance.
__Controllers:__ Towards the `views` collect all information into a helper class that needs to be rendered. Towards the `models` implement helper methods to combine repeated tasks into single methods.
__Models:__ Use methods with single responsibility, add new modules and classes to simplify code.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
4. What can you expect from a group as you begin working together? As you continue working together?
At the beginning I expect to spend some time to establish way of working and spend some time to ensure everybody has the same understanding of what needs to be accomplished, the timeline and the individual tasks. Depending on the set up of the team that can take widely warying amount of effort/time. As we continue working together these communication/correction cycles are expected to become shorter and the overall efficiency of the team working together is expected to increase.
5. What two columns does `t.timestamps null: false` create in our database?
It adds `created_at` and `updated_at` columns into our table within the database.
6. What cURL flag can you use to send a `POST` request?
7. What case does JSON (and JavaScript) use for multi-word variables?
8. What case does Ruby use for multi-word variables?
Ruby syntax is using `_` (underline) character.
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
Although there can be situations when a teacher teaches at multiple schools, it is more like to be a school having multiple teachers and a teacher would belong to a single school. Based on this assumption it would be a `one-to-many`relationship between schools and teachers.
Within the `School` model there would be a `has_many: teachers` association and within the `Teacher` model there would be a `belongs_to: school` association.
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
15. What types of output do we want to test when we test our controllers?
16. What could you see in your code that would make you think you might want to create a partial?
17. Why might you use a helper method?
