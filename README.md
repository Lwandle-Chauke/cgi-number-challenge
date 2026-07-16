<div align="center">

#  CGI Number Challenge

### A Java-based CGI web application that generates dynamic number challenges using server-side processing and the Common Gateway Interface (CGI).

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![CGI](https://img.shields.io/badge/CGI-Dynamic%20Web%20Content-blue?style=for-the-badge)
![Apache](https://img.shields.io/badge/Apache-Web%20Server-red?style=for-the-badge&logo=apache)
![Networking](https://img.shields.io/badge/Computer-Networks-orange?style=for-the-badge)

**Author:** **Lwandle Chauke**

</div>

---

#  Overview

The **CGI Number Challenge** is a Java-based web application developed to demonstrate how dynamic web content can be generated using the Common Gateway Interface (CGI).

Unlike static web pages that always display the same content, this application generates responses dynamically on the server whenever a user interacts with the system. The project highlights the relationship between web servers, CGI programs, HTTP requests, and browser-based user interaction.

The application processes user requests through a CGI script executed by the web server and generates custom HTML responses based on user input and randomly generated values.

This project provided practical experience with early web technologies and helped strengthen my understanding of server-side processing, HTTP communication, and dynamic content generation.

---

#  Project Highlights

- **Dynamic web content generation**
- **Java CGI application**
- **HTTP request processing**
- **Server-side execution**
- **Browser-based interaction**
- **Random number generation**
- **HTML response creation**
- **Apache web server integration**
- **Client-server communication**
- **Network protocol fundamentals**

---

#  Features

##  Web Interface

- **Browser-accessible application** – Access via any web browser
- **Dynamic HTML page generation** – Content changes on every request
- **Interactive user experience** – Click numbers to test your skill
- **Server-generated responses** – All logic executes on the server
- **HTTP request handling** – Proper GET request parsing

##  Game Functionality

- **Random number generation** – Two random numbers between 1 and 100
- **Dynamic challenge creation** – Each page load gives fresh numbers
- **Larger number selection** – User must identify and click the larger number
- **Immediate feedback** – Instant results via right.htm or wrong.htm
- **Try again mechanism** – Reset the game with a single click

##  Server-Side Processing

- **CGI execution through Apache** – Server runs the Java application
- **Request parsing** – Handles form data and URL parameters
- **Response generation** – Dynamic HTML with proper headers
- **Caching prevention** – Meta tags and headers to prevent stale content
- **No JavaScript** – All processing happens on the server

---

#  Networking Concepts

This project demonstrates several important networking and web development concepts:

##  HTTP Communication

- **HTTP requests** – Understanding the GET method and request structure
- **HTTP responses** – Generating proper HTTP/1.1 response headers
- **Request headers** – Parsing client information
- **Response headers** – Content-Type, Cache-Control, and more
- **Browser-server communication** – Understanding the request-response cycle

##  CGI Architecture

- **Common Gateway Interface (CGI)** – The standard for server-side scripting
- **Web server integration** – Apache's role in executing CGI programs
- **Process execution** – How Apache invokes external programs
- **Environment variables** – QUERY_STRING, HTTP_USER_AGENT, and more
- **Dynamic content generation** – Creating HTML on the fly

##  Client-Server Model

- **Browser as client** – Initiating HTTP requests
- **Apache as web server** – Interfacing between client and CGI
- **Java CGI application** – Processing requests and generating responses
- **Request-response lifecycle** – Understanding the complete flow

---

#  Technologies Used

##  Core Technologies

| Technology | Purpose |
|------------|---------|
| **Java** | Primary programming language |
| **CGI** | Dynamic content generation interface |
| **HTML5** | Content structure and markup |
| **HTTP** | Client-server communication protocol |
| **Apache2** | Web server with CGI support |
| **Ubuntu** | Operating system environment |

##  Concepts Applied

| Concept | Application |
|---------|-------------|
| **Server-side programming** | Java CGI implementation |
| **Dynamic web applications** | Generating content on the fly |
| **Form processing** | Handling user input |
| **Input validation** | Ensuring data integrity |
| **Random number algorithms** | Game logic implementation |

---

#  System Architecture

```text
┌─────────────────────────────────────────────────────────────┐
│                       USER BROWSER                          │
│   http://localhost/cgi-bin/numberchallenge                  │
└─────────────────────────────────────────────────────────────┘
                              │
                              │ HTTP GET Request
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    APACHE WEB SERVER                        │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  HTTP Request Handler                               │   │
│  │  Receives and parses the request                    │   │
│  └─────────────────────────────────────────────────────┘   │
│                              │                              │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  CGI Module                                         │   │
│  │  Identifies CGI request and prepares execution      │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                              │
                              │ Invokes CGI Program
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                   JAVA CGI APPLICATION                     │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  Request Processing                                 │   │
│  │  Parses QUERY_STRING and environment variables      │   │
│  └─────────────────────────────────────────────────────┘   │
│                              │                              │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  Business Logic                                     │   │
│  │  Generates random numbers, compares values          │   │
│  └─────────────────────────────────────────────────────┘   │
│                              │                              │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  Response Generation                                │   │
│  │  Builds HTTP headers and HTML body                 │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                              │
                              │ HTTP Response (HTML)
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                       USER BROWSER                          │
│              Displays dynamic challenge page                │
└─────────────────────────────────────────────────────────────┘
```

---

#  Repository Structure

```text
cgi-number-challenge/
│
├── Numbers.java               # Main Java CGI application source
├── numbers                    # Bash wrapper script for CGI execution
├── Numbers.class              # Compiled Java bytecode
│
├── right.htm                  # Congratulatory page (correct guess)
├── wrong.htm                  # Try again page (incorrect guess)
│
├── numbers.md5                # MD5 digest for submission
│
├── screenshots/               # Screenshots of the application
│   ├── main-page.png
│   ├── correct-answer.png
│   └── wrong-answer.png
│
├── README.md                  # This documentation file
│
└── LICENSE                    # License information
```

---

#  How It Works

##  Request-Response Lifecycle

### Step 1: Page Request

The browser sends an HTTP GET request to the Apache server:

```
GET /cgi-bin/numbers HTTP/1.1
Host: localhost
```

### Step 2: CGI Invocation

Apache identifies the file in the `cgi-bin` directory and executes the wrapper script (`numbers`).

### Step 3: Wrapper Execution

The wrapper script (`numbers`) invokes the Java interpreter:

```bash
#!/bin/bash
cd /usr/lib/cgi-bin
java Numbers
```

### Step 4: Random Generation

The Java program generates two random numbers between 1 and 100:

```java
Random rand = new Random();
int num1 = rand.nextInt(100) + 1;
int num2 = rand.nextInt(100) + 1;
```

### Step 5: HTML Generation

The program determines which number is larger and builds the HTML page:

```html
<!DOCTYPE html>
<html>
<body>
    <p>Click on the larger number:</p>
    <p>
        <a href="/right.htm">47</a>
        <a href="/wrong.htm">23</a>
    </p>
</body>
</html>
```

### Step 6: Response Delivery

The server sends the HTTP response:

```
HTTP/1.1 200 OK
Content-Type: text/html
Cache-Control: no-cache

<!DOCTYPE html>...
```

---

#  How to Play

##  Game Rules

1. A page loads showing **two random numbers** (1–100)
2. You must **click on the larger number**
3. If you click correctly → `right.htm` congratulates you
4. If you click incorrectly → `wrong.htm` lets you try again
5. Both result pages contain a **"Try again"** link to start a new round

## 🧠 Strategy

- The game is purely luck-based
- Each round generates new random numbers
- The page uses anti-caching headers, so you always get fresh numbers
- No client-side code – all logic is server-side

---

#  Running the Project

##  Prerequisites

- **Ubuntu** (or any Linux distribution)
- **Apache2** with CGI module enabled
- **Java** (OpenJDK 8 or later)
- **Web Browser** (Chrome, Firefox, etc.)

##  Setup Instructions

### 1. Install Apache and Enable CGI

```bash
sudo apt update
sudo apt install apache2 -y
sudo a2enmod cgi
sudo systemctl restart apache2
```

### 2. Install Java

```bash
sudo apt install openjdk-11-jdk-headless -y
```

### 3. Compile the Application

```bash
javac Numbers.java
```

### 4. Deploy Files

Copy the static files to the document root:

```bash
sudo cp right.htm wrong.htm /var/www/html/
```

Copy the CGI files to the CGI directory:

```bash
sudo cp numbers Numbers.class /usr/lib/cgi-bin/
```

### 5. Set Permissions

```bash
sudo chmod 755 /usr/lib/cgi-bin/numbers
sudo chmod 644 /usr/lib/cgi-bin/Numbers.class
sudo chmod 644 /var/www/html/right.htm /var/www/html/wrong.htm
```

### 6. Launch the Application

Open a browser and navigate to:

```
http://localhost/cgi-bin/numbers
```

---

#  Design Notes

##  User Interface

The application focuses on functionality over aesthetics:

- **Clean, minimal layout** – Simple and effective
- **Clear call-to-action** – "Click on the larger number"
- **Immediate feedback** – Success or failure pages
- **Easy restart** – "Try again" link on both result pages

##  Anti-Caching

To ensure fresh numbers on every visit:

```html
<meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Expires" content="0">
```

---

#  Learning Outcomes

This project strengthened my understanding of:

| Concept | Application |
|---------|-------------|
| **Web Server Configuration** | Setting up Apache with CGI support |
| **CGI Programming** | Writing server-side applications in Java |
| **HTTP Protocol** | Understanding request/response structure |
| **Server-Side Logic** | Processing user input on the server |
| **Dynamic Content** | Generating HTML responses programmatically |
| **File Permissions** | Securing CGI execution with proper permissions |
| **Packaging & Deployment** | Using tar with absolute paths |
| **Checksums** | Generating and using MD5 digests for verification |

---

# 🔧 Troubleshooting

##  Common Issues

### "500 Internal Server Error"

- Check Apache error logs:
  ```bash
  sudo tail -f /var/log/apache2/error.log
  ```
- Verify wrapper script permissions (`chmod 755`)
- Ensure Java is installed and accessible

### "File Not Found" (404)

- Confirm `right.htm` and `wrong.htm` are in `/var/www/html/`
- Check file permissions (`chmod 644`)

### "Numbers Not Changing"

- Verify anti-caching headers are present
- Test in incognito/private browsing mode

### "Cannot Connect to Server"

- Ensure Apache is running: `sudo systemctl status apache2`
- Verify the `cgi-bin` directory exists and is configured

---

## 📂 Archive Structure

The archive must use absolute paths so that extracting from root places files correctly:

```text
var/
└── www/
    └── html/
        ├── right.htm
        └── wrong.htm

usr/
└── lib/
    └── cgi-bin/
        ├── numbers
        └── Numbers.class
```

---
#  Future Improvements

Potential enhancements include:

| Feature | Description |
|---------|-------------|
| **Difficulty Levels** | Easy (1–10), Medium (1–100), Hard (1–1000) |
| **Score Tracking** | Session-based score tracking |
| **Leaderboard** | Persistent high scores |
| **Timer** | Timed challenges |
| **Visual Enhancements** | Animated transitions and feedback |
| **Mobile Optimization** | Fully responsive design |
| **Multiple Languages** | Internationalization support |

---

#  About Me

I'm **Lwandle Chauke**, a Computer Science student at the University of Pretoria with a strong interest in:

- **Software Engineering** – Building robust, maintainable systems
- **Computer Networks** – Understanding how the internet works
- **Cybersecurity** – Protecting systems and data
- **Backend Development** – Creating scalable APIs and services
- **Distributed Systems** – Building resilient, large-scale applications

I enjoy learning through building, and this project gave me hands-on experience with networking fundamentals that I'll carry into my career.

**GitHub:** https://github.com/Lwandle-Chauke

---

<div align="center">

---

If you found this project helpful, please consider starring the repository! 


</div>
```
