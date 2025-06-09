# How I Plan My Coding Projects - 9 Steps

Checklist to use when planning a project:

- [ ] Start from your goal
- [ ] Write user stories
- [ ] Define your data models
- [ ] Nail an MVP
- [ ] Draw a simple prototype
- [ ] Understand future scope
- [ ] Drill into components
- [ ] Pick the stack
- [ ] Plan the development process

> NOTE: Each step builds upon the previous one, so revisit earlier
> decisions as needed.

---

# Step 1 - Start from your goal

Three main questions:
1. Why am I making this project?
2. Who is this project for?
3. What will make it valuable?

The answers to these three questions will set the directions and technical decision-making.

Projects can be for hobby, portfolio, or customers. The needs and decisions will be different according to the goals of the project.

> These questions help keep your project aligned with its purpose.

---

# Step 2 - Write user stories.

Write simple user stories, considering user-centered design.
This is **NOT technical yet**!

Examples:
* User should be able to upload a file
* User should be able to create an account
* User should be able to view a dashboard

Write 10 to 20 user stories. It will have MUSTs, SHOULDs, and NICE-TO-HAVEs

> This list clarifies what is essential versus optional.

---

# Step 3 - Define your data models

Think about the data that will be used. 

No stack (MongoDB, PostgreSQL, etc.) needed yet.

Main questions to answer here:
* What information do I need to store?
* How does it relate to the other data?
* What do those relationships look like?

> Sketching your models early helps visualize how everything fits together.

Simple blog example:
![Blog models](images\Blog_models.png)

---

# Step 4 - Nail an MVP

Code a minimum viable product.

Reduce half or even fewer of the user stories and code them. Go with the crucial features.

> This keeps the project manageable while delivering value quickly.

---

# Step 5 - Draw an extremely simple prototype or wireframe

Sketch a simple wireframe on paper or online.

No need for Figma or advanced wireframe tools here.

Think about the screens needed: navigation, buttons, forms.

It doesn't need fonts, colors, or to look good.

Examples:
* How does the user log in?
* What happens after uploading a file?
* How to navigate between the tabs?

**Paper is cheap; code is expensive.**

> Low-fidelity sketches let you iterate without heavy investment.

---

# Step 6 - Understand what the future of the project is going to look like

Now you have a good idea of the user stories, the data needed, and the wireframe.

But before thinking of frameworks or stacks, consider what the future of the project is.

The goal is to avoid over-engineering small projects but also avoid under-engineering huge projects.

Questions:
* How flexible does the code need to be?
* Is it going to accept hundreds, thousands, maybe tens of thousands of users at the same time?

> Understanding these constraints prevents wasted effort later on.

---

# Step 7 - Drill into the components

The goal here is to help define the architecture of the project.

What are the high-level components?

Examples:
* Is it a simple script?
* Will it have an interface?
* Does it need a backend, a frontend?
* Will it be a browser extension, mobile app, web service?

> Listing components early helps visualize system boundaries.

---

# Step 8 - Picking the stack

We start with the project first, then choose the stack/framework.

Pick the tool that best fits the project.

Follow this:
1. Pick the simplest stack
 2. That fits within the relevant skill set
3. That can accomplish the goals

Must decide on:
* Frontend
* Backend
* Database
* Other features

Example for a simple webapp:
* Frontend: React
* Backend: Node.js
* Database: MongoDB
* AI Agent: LangChain

Key question:
* Can I deploy the project with these stacks?

> You can always swap components later if the project grows.

---

# Step 9 - Overall development process

Make the core functionalities work before adding extras.

It's like building a good foundation to avoid errors due to stack issues.

* Create a project skeleton
  * basic folder structure
  * development environments
  * version control
* Setting up the database and creating data models
* Build the backend routes
  * API endpoints
* Frontend interface
  * connect to backend
* Project iteration (sprints to complete user stories.)
* Automated deployments and testing (if needed)

> Automated pipelines save headaches down the road.
