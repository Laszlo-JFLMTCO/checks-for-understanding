## Week One - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What is `json` and why is it important?  
Standardize format to pass information between server and client. Balanced solution between machine frieldnly and human readible.
2. What's the difference between `joins` and `includes` in ActiveRecord?  
`joins` will load only the tables that are needed to serve the quiery, `include` loads all relevant tables, reducing the number database queries in the process.
3. What's an API?  
Interface to utilize set of features made available on the server/web application side.
4. How do we test an internal API (in general)?  
Calling the defined endpoints with verious input and confirm that the returned data is what is expected based on the given input.
5. What are two different ways to customize your `json`?  
Use `serializer` or `jbuilder` to alter/control the output that is rendered into a JSON response.
