<div align="center">

# CGI Number Challenge

### A Java-based CGI web application that generates dynamic number challenges using server-side processing and the Common Gateway Interface (CGI).

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge\&logo=openjdk\&logoColor=white)
![CGI](https://img.shields.io/badge/CGI-Dynamic%20Web%20Content-blue?style=for-the-badge)
![Apache](https://img.shields.io/badge/Apache-Web%20Server-red?style=for-the-badge\&logo=apache)
![Networking](https://img.shields.io/badge/Computer-Networks-orange?style=for-the-badge)

**Author:** **Lwandle Chauke**

</div>

---

# Overview

The **CGI Number Challenge** is a Java-based web application developed to demonstrate how dynamic web content can be generated using the Common Gateway Interface (CGI).

Unlike static web pages that always display the same content, this application generates responses dynamically on the server whenever a user interacts with the system. The project highlights the relationship between web servers, CGI programs, HTTP requests, and browser-based user interaction.

The application processes user requests through a CGI script executed by the web server and generates custom HTML responses based on user input and randomly generated values.

This project provided practical experience with early web technologies and helped strengthen my understanding of server-side processing, HTTP communication, and dynamic content generation.

---

# Project Highlights

* Dynamic web content generation
* Java CGI application
* HTTP request processing
* Server-side execution
* Browser-based interaction
* Random number generation
* HTML response creation
* Apache web server integration
* Client-server communication
* Network protocol fundamentals

---

# Features

## Web Interface

* Browser-accessible application
* Dynamic HTML page generation
* Interactive user experience
* Server-generated responses
* HTTP request handling

## Game Functionality

* Random number generation
* User input validation
* Dynamic challenge creation
* Result calculation
* Immediate feedback

## Server-Side Processing

* CGI execution through Apache
* Request parsing
* Response generation
* Form data handling
* Dynamic content rendering

---

# Networking Concepts

This project demonstrates several important networking and web development concepts:

### HTTP Communication

* HTTP requests
* HTTP responses
* Request headers
* Response headers
* Browser-server communication

### CGI Architecture

* Common Gateway Interface (CGI)
* Web server integration
* Process execution
* Environment variables
* Dynamic content generation

### Client-Server Model

* Browser as client
* Apache as web server
* Java CGI application as server-side processor
* Request-response lifecycle

---

# Technologies Used

## Core Technologies

* Java
* CGI
* HTML
* HTTP
* Apache Web Server

## Development Concepts

* Server-side programming
* Dynamic web applications
* Form processing
* Input validation
* Random number algorithms

---

# System Architecture

```text
User Browser
      │
      ▼
HTTP Request
      │
      ▼
Apache Web Server
      │
      ▼
Java CGI Application
      │
      ▼
Business Logic
(Random Number Generation)
      │
      ▼
HTML Response
      │
      ▼
User Browser
```

---

# Repository Structure

```text
cgi-number-challenge/

├── src/
│   ├── NumberChallenge.java
│   ├── RequestHandler.java
│   ├── ResponseGenerator.java
│   └── Utilities.java
│
├── docs/
│   ├── Assignment Specification.pdf
│   ├── Design Notes.pdf
│   └── Screenshots/
│
├── screenshots/
│
├── README.md
│
└── LICENSE
```

---

# How It Works

The application is executed through a web server configured to support CGI programs.

When a user accesses the application:

1. The browser sends an HTTP request.
2. Apache invokes the Java CGI program.
3. The program processes the request.
4. A random challenge is generated.
5. User input is validated.
6. Results are calculated.
7. A dynamic HTML page is returned to the browser.

Every request triggers a fresh execution of the CGI application, demonstrating the traditional CGI processing model.

---

# Example Workflow

### Step 1

User opens the application in a browser.

```text
http://localhost/cgi-bin/numberchallenge
```

### Step 2

The server generates a challenge and displays it.

```text
Guess a number between 1 and 100
```

### Step 3

The user submits a response.

```text
50
```

### Step 4

The CGI application evaluates the input and returns feedback.

```text
Too High
```

or

```text
Too Low
```

or

```text
Correct!
```

---

# Skills Demonstrated

This project demonstrates proficiency in:

* Java programming
* Web server configuration
* CGI application development
* HTTP protocol fundamentals
* Client-server architecture
* Dynamic content generation
* Input validation
* Problem solving
* Software design principles
* Network application development

---

# Running the Project

## Clone the Repository

```bash
git clone https://github.com/Lwandle-Chauke/cgi-number-challenge.git
```

## Compile the Application

```bash
javac NumberChallenge.java
```

## Configure Apache CGI Support

Enable CGI execution within Apache and place the compiled application in the configured CGI directory.

Example:

```text
cgi-bin/
└── NumberChallenge.class
```

## Launch the Application

Open a browser and navigate to:

```text
http://localhost/cgi-bin/NumberChallenge
```

---

# Documentation

Documentation included in this repository may contain:

* Assignment specification
* Design decisions
* Testing results
* Screenshots
* Deployment notes
* Architecture diagrams

---

# Screenshots

Screenshots demonstrating the application can be found inside the:

```text
screenshots/
```

directory.

Example screenshots include:

* Initial challenge screen
* User input form
* Generated responses
* Server interaction workflow

---

# Learning Outcomes

This project strengthened my understanding of:

* How web servers execute CGI programs
* Dynamic web content generation
* HTTP request and response structures
* Browser-server communication
* Java server-side programming
* Input handling and validation
* Request processing workflows
* Early web application architectures

Most importantly, it provided practical insight into the foundations upon which modern server-side web frameworks are built.

---

# Future Improvements

Potential enhancements include:

* Improved user interface
* Session tracking
* Persistent score storage
* User authentication
* Multiplayer support
* Database integration
* Enhanced input validation
* REST API implementation
* Migration to modern web frameworks
* Cloud deployment

---

# About Me

I'm **Lwandle Chauke**, a Computer Science graduate with a strong interest in:

* Software Engineering
* Computer Networks
* Cybersecurity
* Application Security
* Backend Development
* Distributed Systems

I enjoy building systems that combine programming, networking, and security concepts while continuously expanding my technical knowledge.

**GitHub**

https://github.com/Lwandle-Chauke

---

<div align="center">

If you found this project interesting, feel free to star the repository!

</div>
