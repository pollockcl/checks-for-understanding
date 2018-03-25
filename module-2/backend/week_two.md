## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  It's an ORM that let's you abstract away SQL.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  Team.all
  Team.select
  Team.where
  Team.joins
  Team.distinct
  Team.pluck
  Team.find
  etc

  It is in the class because of inheritance.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  Team.find(4)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  class Teacher < AR
    has_many :students
  end

  class Students < AR
    belongs_to :teacher
  end

6. Define foreign key, primary key, and schema.
   Foreign key - unique key that relates to another table's primary key
   Primary Key - unique key that searches a table
   schema - the layout/map of a db

7. Describe the relationship between a foreign key on one table and a primary key on another table.
  the foreign key on table a should be the same as the primary key on table b

8. What are the parts of an HTTP response?
  Header, Body, Footer

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
  .group/.count makes a nice hash of how many times a table has a value
  .pluck grabs just one attribute. Supposedly very lightweight
  .distinct kind of like the uniq method in ruby arrays. very handy
  .where returns multiple instances based off of criteria
  .order organizes data

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
  db:drop drops the database
  db:migrate imports db settings
  db:create make the db

3. What two columns does `t.timestamps null: false` create in our database?
  created_at, updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  class School < AR
    has_many :teachers dependent: destroy
  end  

  class Teacher < AR
    belongs_to :school
  end

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
  rails g migration AddTeachersToSchools school:references

6. Give an example of when you might want to store information besides ids on a join table.
  I can't think of a good reason to do that. I'm sure there is one, but nothing comes to mind.

7. Describe and diagram the relationship between patients and doctors.
  class Doctor
    has_many :patient_doctors
    has_many :patients, through :patient_doctors
  end

  class Patient
    has_many :patient_doctors
    has_many :doctors, through :patient_doctors
  end

8. Describe and diagram the relationship between museums and original_paintings.
  class Museum 
    has_many :original_paintings
  end

  class OriginalPainting
    belongs_to :museum
  end

9. What could you see in your code that would make you think you might want to create a partial?
  repitition.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week
