# T3A2 Full Stack Application

# MemPal - Memory Palace Management System

## Table of Contents
1. [Description](#description)
2. [Dataflow Diagram](#dataflow-diagram)
3. [Application Architecture Diagram](#application-architecture-diagram)
4. [User Stories](#user-stories)
5. [Wireframes](#wireframes)
6. [Project Management](#project-management)

## Description

### Purpose
MemPal is a minimalist, user-friendly web application designed to help memory athletes and enthusiasts store, organize, and practice their memory palaces. The app aims to improve memory training efficiency by providing a structured and intuitive platform for managing memory palaces and loci.

### Memory Palace Technique

#### What is the Memory Palace Technique
The Memory Palace technique, also known as the Method of Loci, is a mnemonic device that involves visualizing a familiar place (a "palace") and associating each location withinit (a "locus") with information you want to remember.

#### How to Use the Memory Palace Technique
1. **Choose Your Palace**: Select a familiar place, such as your home, a route you walk daily, or any well-known location.
2. **Define Your Loci**: Identify specific locations within your palace where you will store information. These could be rooms, furniture, landmarks, etc.
3. **Associate Information**: Visualize the information you want to remember and place it at each locus. Use vivid and memorable images to make the associations stronger.
4. **Practice Recall**: Mentally walk through your palace and recall the information at each locus. Regular practice helps reinforce the associations.

#### Applications of the Memory Palace Technique
- Daily Life: Remembering shopping lists, to-do lists, names, and faces.
- Competitions: Used by **_memory athletes_** to memorize decks of cards, numbers, and other data quickly and accurately.
- Learning: Enhancing study techniques by memorizing facts, dates, vocabulary, and more.
- Work: Improving productivity by remembering tasks, presentations, and key information.

### Functionality / Features
- **Simple Login System:** Easy sign-up and login process using email and password with secure authentication using JWT.
- **Memory Palace Management:** Users can create, edit, and delete memory palaces, and categorize them (e.g., numbers, cards, names, and faces).
- **Loci Management:** Users can add, edit, and organize loci within each palace, attach brief descriptions, and reorder loci using drag-and-drop functionality.
- **Review System:** Built-in system to practice memorizing the memory palaces with customizable settings (e.g., timed review, randomized order) and basic progress tracking.
- **Storage Limits:** Free users can store up to 5 memory palaces, while premium users can store unlimited palaces for $0.99/month.
- **Minimalist Design:** Clean, intuitive interface with everything accessible from the front page, and responsive design for both desktop and mobile devices.

### Target Audience
MemPal targets memory athletes, enthusiasts, and anyone interested in improving their memory skills. The app is designed to cater to both beginners and advanced users by offering a range of features that support different levels of memory training.

### Tech Stack
- **Front End:** React.JS, Javascript, HTML, CSS
- **Back End:** Node.JS, Express.JS
- **Database:** MongoDB, Mongoose
- **Testing:** Jest
- **Package Manager:** npm
- **Design Tools:** draw.io, Figma
- **Deployment:** Heroku, Render
- **Development Environment:** Visual Studio Code
- **Version Control:** GitHub
- **Project Management:** Trello

## Dataflow Diagram
**Dataflow Diagram**

The dataflow diagram illustrates the flow of data within the MemPal application:
- **User Authentication**: Users sign up and log in using email and password, with JWT-based authentication for secure sessions.
- **Memory Palace Management**: Users can create, edit, and delete memory palaces, which are stored in MongoDB.
- **Loci Management**: Users can add, edit, and organize loci within each palace, with data stored in MongoDB.
- **Review System**: Users can practice memorizing the memory palaces, with progress tracking data stored in MongoDB.
- **Subscription Management**: Free and premium users have different storage limits, managed through payment integration (e.g., Stripe).

![Dataflow](/docs/Dataflow.jpg)


## Application Architecture Diagram
**Application Architecture Diagram**

The application architecture diagram provides an overview of the high-level structure of the MemPal app:
- **Front End**: Built with React.JS, the front end handles user interactions and displays data fetched from the back end.
- **Back End**: Built with Node.JS and Express.JS, the back end handles API requests, user authentication, and data processing.
- **Database**: MongoDB is used to store user data, memory palaces, loci, and progress tracking information.
- **Authentication**: JWT is used for secure user authentication and session management.
- **Deployment**: The app is deployed on Render.com, ensuring scalability and reliability.

![Application Architecture Diagram](/docs/AAD.jpg)

### **Explanation of Each Stage**

### *Frontend*
- **React.js Application (A):** The frontend is built using React.js, providing a dynamic and responsive user interface. It handles user interactions and updates the UI based on user actions and data received from the backend.
- **HTML/CSS/JavaScript (B):** Standard web technologies used to structure, style, and add interactivity to the web application.

### *Backend*
- **Node.js Server (C):** The backend server is built using Node.js, which handles incoming API requests from the frontend.
- **Express.js Framework (D):** Express.js is used to create RESTful API endpoints for handling CRUD operations, authentication, and subscription management.
- **JWT Authentication (E):** JSON Web Tokens (JWT) are used for secure user authentication, ensuring that only authorized users can access certain features.
- **Subscription Management (F):** Manages user subscriptions, including free and premium tiers, and integrates with the Stripe payment gateway for processing payments.

### *Database*
- **MongoDB (G):** A NoSQL database used to store user data, memory palaces, loci, and progress tracking information.
- **Mongoose ORM (H):** An Object-Relational Mapping (ORM) library for MongoDB, providing a schema-based solution to model application data and interact with the database.

### *External Services*
- **Stripe Payment Gateway (I):** An external service used to handle payment processing for premium subscriptions.
- **Render.com Hosting (J):** The application is deployed on Render.com, ensuring scalability, reliability, and ease of deployment for both the frontend and backend.

### **Detailed Description**

#### 1. *User Interaction*
Users interact with the React.js application (A) through a web browser. The frontend handles user inputs, displays data, and communicates with the backend via API requests.

#### 2. *API Requests*
The React.js application sends API requests to the Node.js server (C) to perform various operations such as creating, editing, and deleting memory palaces and loci, as well as handling user authentication and subscription management.

#### 3. *Request Handling*
The Node.js server, using the Express.js framework (D), processes incoming API requests. It performs CRUD operations on the MongoDB database (G) through the Mongoose ORM (H).

#### 4. *Authentication*
The backend uses JWT (E) for secure user authentication. When users log in or sign up, the server generates a JWT, which is used to authenticate subsequent requests.

#### 5. *Subscription Management*
The backend manages user subscriptions (F), differentiating between free and premium users. It integrates with the Stripe payment gateway (I) to process payments for premium subscriptions.

#### 6. *Data Storage and Access*
The MongoDB database (G) stores all application data, including user information, memory palaces, loci, and progress tracking. The Mongoose ORM (H) provides a schema-based solution to interact with the database.

#### 7. *Deployment*
The application is deployed on Render.com (J), which hosts both the frontend and backend, ensuring the application is scalable and reliable.

## User Stories
1. As a memory athlete, I want to create a new memory palace so that I can organize my loci for efficient memorization.
   - Acceptance Criteria:
     - User can create a new memory palace with a name and description.
     - The new memory palace is saved in the database.

2. As a memory trainer, I want to add loci to my memory palace so that I can store and organize information within the palace.
   - Acceptance Criteria:
     - User can add loci with descriptions to a memory palace.
     - The loci are saved and associated with the correct memory palace.

3. As a premium user, I want to store unlimited memory palaces so that I can manage a large number of palaces without restrictions.
   - Acceptance Criteria:
     - Premium users can create and store an unlimited number of memory palaces.
     - Subscription status is verified and managed through payment integration.

4. As a user, I want to practice memorizing my memory palaces so that I can improve my memory skills.
   - Acceptance Criteria:
     - User can enter practice mode with customizable settings.
     - Progress is tracked and displayed to the user.

## Wireframes

The wireframes illustrate the layout and design of the MemPal app across different screen sizes:
- **Mobile View**: Optimized for small screens with a focus on ease of navigation and accessibility.
- **Tablet View**: Adjusted layout to take advantage of larger screen real estate while maintaining usability.
- **Desktop View**: Full-featured interface with all functionalities easily accessible from the dashboard.

**Mobile View**
![Mobile Wireframe](link_to_mobile_wireframe_image)

**Tablet View**
![Tablet Wireframe](link_to_tablet_wireframe_image)

**Desktop View**
![Desktop Wireframe](link_to_desktop_wireframe_image)

## Project Management


The project management approach **Principle** for MemPal includes:
- **Task Organization**: Tasks are organized and prioritized using Trello, with clear labels and due dates.
- **Progress Tracking**: The Trello board is updated regularly to reflect the current status of tasks and milestones.
- **Agile Methodology**: The project follows agile principles, with regular sprints and reviews to ensure continuous improvement and adaptability.

### 1. Brainstorming Step:

- Check Requirements, forming ideas.
- Create draft plan for framework, github repositories, Readme.md and documentation, etc.
- Add regular/repeated tasked as reminders for a more eficient process
- Add labels to Trello.

![Brainstorming](/docs/brainstorming.png)

### 2. Framework Step:

- Check sample projects from others.
- Form the ideas of requirement, planning and important key tasks/points:

    1. Problems and Solutions
    2. Planning and Framework
    3. Dataflow Diagram, Application Architecture Diagram, User Stories and Wireframes
    4. Project Management

- Create a more detailed plan with more actionable tasks.

![Framework](/docs/framework.png)
![Plan](/docs/plan1.png)

### Update 1 - R1 

Complete the below steps for documentation:

- Purpose
- Functionality / Features
- Target Audience
- Tech Stack
- Added Explanation and Applications of the Memory Palace Technique

![trello2](/docs/trello2.png)
![trello3](/docs/trello3.png)

### Update 2 - R2

Complete Dataflow diagram

![trello4](/docs/trello4.png)

### Update 3 - R3

Complete Application Architecture Diagram

![trello5](/docs/trello5.png)