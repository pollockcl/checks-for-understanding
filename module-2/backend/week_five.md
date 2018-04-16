### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 5 Questions
1. How do we make flash messages display on a page?
  By storing the flash we want in the flash hash and calling it in the appropriate view as such:

      <% flash.each do |message_type, message| %>
        <%= message %>
      <% end %>



2. Where is cart information/temporary information usually stored?
  Oof. I feel like the answer you're looking for is in the session.

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  We wouldn't use raw queries to store the cart in the database everytime something was added. It would become a traffic chokepoint. We'd probably have to do something like make batches. It is beneficial so that when a user logs out or clears their cookes they don't destroy their cart.

4. What is the purpose of the asset pipeline?
  To optimize and organize the loading/requesting of styling and javascripts

5. Why do we precompile our assets?
  To make it work with heroku. Also to minify them.


6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %> :: loads a stylesheet
<%= javascript_include_tag "application" %> :: imports a javascript
<%= image_tag "rails.png" %> :: loads an image
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project? 
  Readability. Benefits include not scaring away employers.

8. What are the top four accessibility issues that we as developers should be aware of?
  Probably authorization followed closely by authentication followed by some other principles I'm not sure were covered.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  That is a callback method. It would live in a model.

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```
  def self.active_users
    where(active: true)
  end

11. What is the difference between a scope and a class method?
  There isn't really one.

  Also on a side not I've spoken with three other people who agree that you didn't cover material. Come on.


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
    cart['48'] = 4

  12b. How would you increase the quantity of item 29?  
    cart['29'] += 7

  12c. How would you find out how many items your user is thinking about purchasing?   
    cart.values.sum
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
  Writing/overwriting built in methods from inheritance. 
    1. ActiveRecord methods. Most can be treated as array returns
    2. Overwriting the to_param method

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  string.scan(/\d\d\d\d?/).join('.')

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
