## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  A piece of data that is temporarily stored in a browser.

2. What’s the difference between a session and a cookie?
  A session is just a longer lasting cookie. It lasts until the user closes their browser.

3. What’s a flash and when do you want to use flashes?
  A message that notifies a user that something did or did not happen. Use when they do stuff like logout, delete stuff, etc.

4. Why do people say “HTTP is stateless”?
  Because nothing in the protocal explicitely remembers the state of a user's request history.

5. What’s authentication? Explain.
  Verifying that people are who they say they are. Asking for a drivers licence, username/password, etc are examples.

6. What’s the difference between authentication and authorization?
  Authorization is just a fancy word for permission.

7. What’s a before filter?
  A method that runs before other methods to determine how/if those other methods get ran.

8. How do we keep track of a user once they’ve logged in?
  Cookies and Sessions.

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  Namespacing is good for organization and you don't have a specific model or object that is tied to it, like admin/blah. Nesting resources is good when you have a resource dependant on another resource.

10. At a high level, what tools can you use to implement authorization? How would you use them?
  bcrypt? Before actions? 

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  It's a lightweight way to determine a user's permissions or other user attributes that could be associated with an integer (department, office). They are defined in the model.

  enum column: %w[val1 val2]

12. What are some strategies you can use to keep your views DRY?
  Partials, presenters

### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
  Assuming that you meant to have 3 separate holiday hashes:
  
  given.map{ |g| g[:holiday][:name] }.sort

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 
   text.split('.').delete('$').to_i

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week