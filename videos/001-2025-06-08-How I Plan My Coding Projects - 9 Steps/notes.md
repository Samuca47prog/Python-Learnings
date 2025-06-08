# How I Plan My Coding Projects - 9 Steps

Checklist to use when planning a project:


---

# Step 1 - Start from your goal

three maion questions:
1. Why am I making this project?
2. Who is this project for?
3. What is gonna make it valuable?

The answers for this three questions will set the directions and technical decision making.

Projects can be for Hobby, Portifolio, Customers. The needs and decisions will be different according to the goals of the project. 

---

# Step 2 - Write user stories.

Write simple user stories, considering user central design.
This is **NOT technical yet**!

Examples:
* User should be able to upload a file
* User should be able to create an account
* User should be able to view a dashboard

Write 10 to 20 user stories. It will have MUSTs, SHOULDs and NICE TO HAVEs

---

# Step 3 - Define your data models

Think about the data that will be used. 

No Stack (mongo db, postgre, etc) needed yet.

Main questions to answer here:
* What information I need to store?
* How it relates to the other data?
* What those relantionships look like?

Simple blog example:
![Blog models](images\Blog_models.png)

---

# Step 4 - Nail a MVP

Code a minimal viable product.

Reduce half or even less of the users stories and code them. Go with the crucial features.

---

# Step 5 - Draw a stupid simple prototype, or very simple wireframe

Write a simple wireframe on paper or online.

No need for figma or advanced wireframe tools here.

Think on the screens needed, navigation, buttons, forms.

It doesn't need fonts, colors, or looking good.

Examples:
* How the user login?
* What happens after uploading a file?
* How to navigate between the tabs?

**Paper is cheate, code is expensive**

---

# Step 6 - Undestand what the future of the project is going to look like

Now you have a good idea of the user stories, the data needed and the wireframe.

But before thinking of frameworks, stacks, etc, think of what is the future of the project.

The goal is to not overengeneering small projects, but also not underengeneering huge projects.

Questions:
* How flexible the code needs to be?
* Is it going to accept hundreds, thounsands, maybe ten thounsands users at the same time?

---

# Step 7 - Drill into the components

The goal here is to help define the architecture of the project.

What are the high level components?

Examples:
* Is it a simple script?
* Will it have a interface?
* Does it need a backend, frontend?
* Will it be a browser extension, mobile app, web service?

---

# Step 8 - Picking the stack

We come with the project first, than we choose the stack/framework.

Pick the best tool that best fit the project.

Follow this:
1. Pick the simplest stack
2. That fits within the relative skillset
3. That can accomplish the goals

Must decide on:
* Frontend
* Backend
* Database
* Other features

Example for a simple webapp:
* Frontend: React
* Backend: Node.js
* Database: Mongo db
* AI Agent: Lang Chain

Key question:
* Can I deploy the project with this stacks?

---

# Step 9 - Overall development process

Make the core functionalities be ready to work before developing.

It is like making a good foundation to avoid errors due to stack issues.

* Create a project skelleton
  * basic folder structure
  * development environments
  * version control
* Setting up the dabase and creating data models
* Build the backend routes
  * API endpoints
* Frontend interface
  * connect to backend
* Project iteration (sprints to kill user stories.)
* Automated deployments and testing (if needed)
