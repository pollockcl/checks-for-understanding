## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  GET, POST, DELETE, PATCH/PUT/ CREATE

2. What is Sinatra?
  A DSL that can't compete with Rails.

4. What is MVC?
  Model, View, Controller. Spits responsibility between routing, views and database access

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  To make things easy to manage

6. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables, global variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  Why use an instance variable if it should only be accessed by the :index view?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
    locals: { name: 'Mr. Ed' }

9. What's the purpose of ERB?
    Handles the HTML/CSS integration for websites built using Ruby.

10. Why do I need a development AND test database?
    Test db should get whiped each time you run your tests, development should be used to actually develope your db.

11. What is CRUD and why is it important?
    It mediates/moderates db intractions for users and that is why it important.

12. What does HTTP stand for? 
    Hyper Text Transfer Protocol

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
    <% blah %>       :: When you don't need the return value
    <%= blah.blah %> :: When you need a return value
14. What's an ORM?
    Object Relational Moddel

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
    ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
    GET::POST
    GET
    GET::POST::PATCH/PUT
    POST::DELETE

17. What's a migration? 
    A fancy word for creating/modifying a db table

18. When you create a migration, does it automatically modify your database?
    Nope

19. How does a model relate to a database?
    It interacts with a single table.

20. What is the difference between `#new` and `#create`?
    Create runs an implicit #save to the database.

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
    You'd use a seed file.

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking?
    activities[:supplies] << 'granola bar' 

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
    Encapsulation: Put stuff in classes
    Abstraction:   Hiding stuff to make it more simple
    Inheritance:   Reusing code via modules or parants.
    Polymorphism:  Overriding methods had by an objects parents.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

