#Fedena : Open source school management system

Project Fedena is the open source school management system based on Ruby on Rails. It is developed by a team of developers at Foradian Technologies. The project was made open source by Foradian, and is now maintained by the open source community. Fedena is the ideal solution for schools and campuses that want an easy means to manage all campus records.

The Project Fedena website http://www.projectfedena.org/ is the home to the developer community behind Fedena project. There you can find forums and bug tracker for Fedena.

#Demo
A demo website for Fedena has been set up at demo.projectfedena.org. You can log in with following usernames and passwords:

    * As admin -- username - admin, password - admin123
    * As student -- username - 1, password - 1123
    * As employee -- username - E1, password - E1123

#License

Fedena is released under the Apache License 2.0.

#Installation

Visit  http://projectfedena.org/install for detailed installation instruction.

#Community Support:

Visit www.projectfedena.org for community support.


# Ruby on Rails Interview – Initial Screening (Q&A)

This set of questions is suitable for 10–20 minute screening rounds.

---

## 1. Core Ruby (Language Fundamentals)

**Q1: What is the difference between a Symbol and a String?**  
**A:** Symbols are immutable and stored in memory only once. Strings are mutable and create new objects when modified.

**Q2: What is the difference between a Block, `Proc`, and `Lambda`?**  
**A:** Blocks are not objects unless converted. `Proc` is a callable object that does not enforce argument count. `Lambda` behaves like a method and enforces correct arguments.

**Q3: What does `self` refer to in Ruby?**  
**A:** `self` refers to the current object or context — it changes based on where it is used (class, module, instance level).

**Q4: What is the difference between `==`, `eql?`, and `equal?`?**  
**A:** `==` checks value equality. `eql?` checks value and type. `equal?` checks if two variables point to the same object in memory.

**Q5: What is the difference between `include` and `extend`?**  
**A:** `include` adds methods as instance methods. `extend` adds methods as class-level methods.

**Q6: What are modules used for?**  
**A:** For namespacing and sharing reusable methods (mix-ins).

---

## 2. Rails Architecture / Fundamentals

**Q1: Explain MVC in Rails.**  
**A:** Model handles data and business logic, View handles the UI, and Controller manages request/response flow.

**Q2: What does `routes.rb` do?**  
**A:** It defines URL mappings to controller actions.

**Q3: What is the difference between `render` and `redirect_to`?**  
**A:** `render` shows a view template without creating a new request. `redirect_to` triggers a new HTTP request and updates the browser URL.

**Q4: What are Strong Parameters?**  
**A:** A security feature to restrict which parameters can be submitted.  
Example: `params.require(:user).permit(:name, :email)`

---

## 3. ActiveRecord / Model Layer

**Q1: What is the difference between `find`, `find_by`, and `where`?**  
**A:**  
- `find(id)` raises an error if the record is not found.  
- `find_by` returns the first matching record or nil.  
- `where` returns an ActiveRecord relation which can be chained.

**Q2: What is the N+1 query problem and how do you fix it?**  
**A:** It happens when queries run inside loops. Fix using eager loading:  
```ruby
User.includes(:posts)


**Q3: What is has_many :through used for?
A: To set up a relationship through a join model that may contain its own logic.

**Q4: What is a scope?
**A:** Reusable query logic defined in the model.
Example: scope :active, -> { where(status: 'active') }

**Q5: Explain polymorphic association.
**A:** Allows one model to belong to multiple other models.
Example: Comment can belong to a Post or Photo.

## 4. Controller Layer

**Q1: What does before_action do?
**A:** Runs a method before certain controller actions, commonly used for authentication or object lookup.

**Q2: How do you return JSON from a controller?
**A:**

render json: { message: "ok" }


**Q3: How do you avoid fat controllers?
**A:** Move business logic into models, service objects, decorators, or presenters.

5. View / Layout / Templates

**Q1: What is the difference between yield and content_for?
**A:** yield outputs the main content block, while content_for stores specific content blocks that can be rendered later in the layout.

**Q2: What are helpers used for?
**A:** To keep view code clean by extracting repeated or complex logic into methods.

**Q3: How do you render a partial?
**A:**

render "users/user", user: @user

6. Front-End Integration

**Q1: How do you include CSS and JS in Rails?
**A:** Through the Asset Pipeline, Import Maps, or Webpacker depending on Rails version.

**Q2: How do you perform AJAX in Rails?
**A:** Using Rails UJS, StimulusJS, or Fetch API returning JSON responses.

7. Git / Team Collaboration

**Q1: What is the difference between git fetch and git pull?
**A:** fetch only downloads remote changes. pull downloads and merges them into your branch.

**Q2: How do you resolve merge conflicts?
**A:** Open the conflicted files, manually fix issues, stage the files, and commit.

**Q3: How do you create and push a new feature branch?
**A:**

git checkout -b feature-branch
git push origin feature-branch
