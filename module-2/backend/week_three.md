## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  rails new

2. What do Models generally inherit from in rails?
  ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
  ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  get 'horses/:horse_id', to: 'horse#show'
  or
  resources :horses, only: [:index, :show] 
  The index page can probably be taken out too.

5. What rake task is useful when looking at routes, and what information does it give you?
  rails routes
  prefix, path, verb

6. What is an example of a route helper? When would you use them?
  Route helpers are generated automatically by the routes.rb file, ie: new_session_path.
  They aren't mandatory to use but they can be used pretty much anywhere. 

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  _url is an absolute path
  _path is relative based on the resources
  

8. What are strong params and why are they necessary?
  Rails complains without them for the most part. They are a convenient way to secure parameters and pass them through model modifications.

9. What role does `form_for` play in helping us create our forms?
  Ties a model and a method into a form. Gives the form direction.

10. How does `form_for` know where to submit the user's input?
   You can specify with the arguments you feed it. The variant used depends on what you're doing and have available.
     form_for(:model, url: some_path, method: :put) do
     form_for model do

11. Create a form using a `form_for` helper to create a new `Horse`. 
    
    form_for(:horse, url: new_horse_path) do |f|
      f.label :something
      f.text_field :something
      f.submit
    end


12. Why do we want to validate our models?
    Sometimes a model has a dependency on its attributes and we need them to be present. Not always though. 

13. What are the steps of the DNS lookup?
    You can use dig or nslookup I guess?
    computer -> router -> DNS -> router -> destination -> router -> computer?
    DNS checks it's a & aaaa records for matches?


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  def move
    prance
  end

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
  furniture[:table][:height]
  furniture[:purchased]

16. What is inheritance?
  Passing down methods and traits from a superclass to a normal class.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources


Choose One:
* I feel confident about the content presented this week

