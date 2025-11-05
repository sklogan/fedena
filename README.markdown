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




## 1. Core Ruby (Language Fundamentals)

| Question | Answer |
|---------|--------|
| **What is the difference between a Symbol and a String?** | Symbols are immutable and occupy a single memory reference. Strings are mutable and create new objects when changed. |
| **What is the difference between a Block, `Proc`, and `Lambda`?** | Blocks are not objects unless converted; `Proc` is a callable object without strict argument checks; `Lambda` behaves like a method and enforces argument count. |
| **What does `self` represent in Ruby?** | `self` refers to the *current object* context — changes depending on scope (class, instance, module). |
| **What is the difference between `==`, `eql?`, and `equal?`?** | `==` compares value, `eql?` compares value + type, `equal?` checks object identity in memory. |
| **Difference between `include` and `extend`?** | `include` adds methods as instance methods; `extend` adds methods as class methods. |
| **What is a Module used for?** | Group reusable methods and namespaces without instantiation. |

---

## 2. Rails Architecture / Fundamentals

| Question | Answer |
|---------|--------|
| **Explain MVC in Rails.** | **Model** manages data and business logic, **Controller** handles requests & responses, **View** displays UI. |
| **What is the role of `routes.rb`?** | Maps URLs to controller actions. Defines application routing. |
| **Difference between `render` and `redirect_to`.** | `render` displays a view **without** a new request; `redirect_to` performs a **new request** and updates the URL. |
| **What are Strong Parameters?** | Security mechanism to permit only allowed attributes. Example:<br>`params.require(:user).permit(:name, :email)` |

---

## 3. ActiveRecord / Model Layer

| Question | Answer |
|---------|--------|
| **Difference between `find`, `find_by`, and `where`.** | `find(id)` → Raises error if not found. <br> `find_by` → Returns first match or `nil`. <br> `where` → Returns a lazy `ActiveRecord::Relation`. |
| **What is the N+1 Query Problem? How to fix it?** | Occurs when queries are triggered inside loops. Fix using `includes` / eager loading:<br> `User.includes(:posts)` |
| **Explain `has_many :through`.** | Defines association through a join model. Useful when join has its own logic. |
| **What is a scope?** | Reusable query logic.<br> `scope :active, -> { where(status: 'active') }` |
| **Explain polymorphic association.** | Allows a model to belong to more than one model using `<name>_id` and `<name>_type`. Example: `Comment` can belong to `Post` or `Photo`. |

---

## 4. Controller Layer

| Question | Answer |
|---------|--------|
| **What does `before_action` do?** | Runs code before controller actions (e.g., authentication, loading records). |
| **How to return JSON from a controller?** | `render json: { message: "Success" }` |
| **How to avoid "fat controllers"?** | Move business logic to **models**, **service objects**, or **presenters**. |

---

## 5. View / Layout / Templating

| Question | Answer |
|---------|--------|
| **Difference between `yield` and `content_for`.** | `yield` inserts main view content; `content_for` stores named layout sections. |
| **What are helpers used for?** | To extract repeated or complex logic from views. |
| **How to render a partial?** | `render "users/user", user: @user` |

---

## 6. Front-End Integration

| Question | Answer |
|---------|--------|
| **How do you load CSS/JS in Rails?** | Using the **Asset Pipeline**, Import Maps (Rails 7), or Webpacker depending on project setup. |
| **How is AJAX handled in Rails?** | Via Rails UJS, StimulusJS, or fetch API returning JSON responses. |

---

## 7. Git / Collaboration

| Question | Answer |
|---------|--------|
| **Difference between `git pull` and `git fetch`.** | `fetch` downloads changes, `pull` downloads **and** merges changes into your branch. |
| **How to resolve merge conflicts?** | Manually edit conflict markers, save, stage, commit. |
| **How to create and push a new branch?** | `git checkout -b feature-name` <br> `git push origin feature-name` |

---
