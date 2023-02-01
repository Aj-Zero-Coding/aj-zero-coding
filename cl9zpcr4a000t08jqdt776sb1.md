# How to build an advanced website with the help of HTML, CSS, and JavaScript?


We are building our responsive portfolio website in this article using HTML5,  CSS3, and JavaScript.

A  portfolio website is a webpage where everyone can see your website. It has other options like the home section, About section, Services section, Portfolio section, and Contact section. In this project, we are going to make a website that will use HTML, CSS, and JavaScript. We will use HTML to give a basic layout; with CSS, we will beautify the design of our website. We will use basic JavaScript features ( like-, a function for a scroll ).

Approach:

- We will create the basic layout i.e. using HTML.
- With the help of CSS, we will beautify our overall structure by giving images, padding, margin, styles, etc.
- We will use basic JavaScript functions to get the current status of the scroll and make changes accordingly.
- When we click on any section, the section will show on the display, and click on the icon then go to the other link and when the user presses the scroll button image or icon will be going to the top. This is done using simple scripting.


This portfolio might contain some very important information of yours like:
- Home section
- About section
- Services section
- Portfolio section
- Contact section

Now first, you need a code editor (like- vs code)

Following, the steps to build a responsive website requires some steps:

**Step 1:** Create some files and folders ( for Example ).


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667394614682/czcPjCbaH.png align="left")

- index.html
- assets
   1. css
      - styles.css
   2. js
      - app.js

**Step: -2** write this code in the ```index.html``` file.

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!--CSS Styles -->
    <link rel="stylesheet" href="./assets/css/styles.css" />

    <!-- Favicons -->
    <link rel="apple-touch-icon" sizes="180x180" href="assets/icons/apple-touch-icon.png" />
    <link rel="icon" type="image/png" sizes="32x32" href="assets/icons/favicon-32x32.png" />

    <!-- Animate CSS CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />
    <title>My Portfolio Website</title>
</head>

<body>
    <!-- =====   Navbar ===== -->
    <nav>
        <h2 style="color: green;">Portfolio</h2>

        <ul class="navigation">
            <li><a href="#about" class="nav-link">About</a></li>
            <li><a href="#skills" class="nav-link">Skills</a></li>
            <li><a href="#projects" class="nav-link">Projects</a></li>
            <li><a href="#contact" class="nav-link">Contact</a></li>
        </ul>
        <button class="burger-menu" id="burger-menu">
          <ion-icon class="bars" name="menu-outline"></ion-icon>
        </button>
    </nav>

    <!-- ===== Hero Section ====== -->
    <section class="hero" id="about">

        <img src="https://raw.githubusercontent.com/Ajay-Dhangar/images/main/web-img/web-1.png" width="660" height="400">

        <div class="bio animate__animated animate__shakeX">
            <h2 class="bio-title" style=" color: #0c0753; text-align: center;">About Me</h2>
            <hr><br>
            <img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/images/Ajay-Dhangar.jpg" alt="ajay-dhangar" style="width: 30%; height: 25%; border-radius: 200px;">
            <p class="bio-text">
                <spam style="font-size: 20px; font-weight: bold;">Hello, my name is
                    <spam style="color: rgb(235, 141, 33);font-style: italic;">Ajay Dhangar</spam>.
                </spam><br>
                <spam style="font-weight: 500;"> I am always open to chatting about programming & coding and would love for you to connect with me on LinkedIn, Twitter, YouTube, GitHub, Medium, and Facebook. Please feel free to join me here on LinkedIn or by email at ajaydhangar49@gmail.com.<br>I'm
                    a web developer with extensive experience for over 3 years. My expertise is to create a website design, graphic design, and many more...<br></spam>
            </p>
        </div>
    </section>

    <!-- ====== More about ====== -->

    <section class="more-about" style=" color: #0c0753;">
        <h2>More About Me</h2>
        <hr class="line">
        <p class="details">I am a web developer and solving some problems in the web developing fild. And I am creating some apps with the help of android studio.<br> I am working of some programing languages for example like us JAVA, C, Python, C++, etc. <br>If you have
            any problem then connect with me and send me your feedback and problem in Contact form I will try to help you.
        </p>
        <hr class="line">
    </section>

    <!-- ====== Skills section ====== -->

    <section class="skills" id="skills">
        <h2 class="skill-header">My Top Skills</h2>

        <div class="skills-wrapper">
            <div class="first-set animate__animated animate__pulse">
                <img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/html-5.png" alt="" loading="lazy" class="icon icon-card" />
                <img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/css3.png" alt="" loading="lazy" class="icon icon-card" />
                <img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/javascript.png" alt="" loading="lazy" class="icon icon-card" />
            </div>

            <div class="second-set animate__animated animate__pulse">
                <img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/bootstrap.png" alt="" loading="lazy" class="icon icon-card" />
                <img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/react-native.png" alt="" loading="lazy" class="icon icon-card" />
                <img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/git.png" alt="" loading="lazy" class="icon icon-card" />
            </div>
        </div>
    </section>

    <!-- ====== Projects section ======= -->

    <section class="projects" id="projects">
        <h2 class="projects-title">Some of my Recent Projects</h2>
        <div class="projects-container">
            <div class="project-container project-card">
                <img src="https://raw.githubusercontent.com/Ajay-Dhangar/images/main/Projects-img/Portfolio.png" alt="expense-tracker" loading="lazy" class="project-pic" />
                <h3 class="project-title">Portfolio Website</h3>
                <p class="project-details">Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa nihil sunt provident iure numquam, laborum voluptate.</p>
                <a href="https://ajay-dhangar.github.io/Responsive-portfolio-website.github.io/" target="_blank" class="project-link">Check it Out</a>
            </div>
            <div class="project-container project-card">
                <img src="https://raw.githubusercontent.com/Ajay-Dhangar/images/main/Projects-img/CriptoCurrency.png" alt="netflic-clone" loading="lazy" class="project-pic" />
                <h3 class="project-title">CriptoCurrency Web</h3>
                <p class="project-details">Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa nihil sunt provident iure numquam, laborum voluptate.</p>
                <a href="https://9wygqd-3000.preview.csb.app/" target="_blank" class="project-link">Check it Out</a>
            </div>
            <div class="project-container project-card">
                <img src="https://raw.githubusercontent.com/Ajay-Dhangar/images/main/Projects-img/game.png" alt="greeny-earth" loading="lazy" class="project-pic" />
                <h3 class="project-title">Gamming Website</h3>
                <p class="project-details">Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa nihil sunt provident iure numquam, laborum voluptate. </p>
                <a href="https://ajay-dhangar.github.io/Aj-Zero-Gaming.github.io/" target="_blank" class="project-link">Check it Out</a>
            </div>
        </div>
    </section>

    <!-- ======= Contact section ======= -->

    <section class="contact" id="contact">
        <h2>Get In Touch With Me</h2>
        <div class="contact-form-container">
            <div class="contact-form">
                <form action="#" method="POST">
                    <div class="form-control">
                        <label for="name">Name</label>
                        <input type="text" id="name" name="sender-name" placeholder="Enter Your Name" class="input-field" required />
                    </div>
                    <div class="form-control">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="sender-email" placeholder="Enter Your Email" class="input-field" required />
                    </div>
                    <div class="form-control">
                        <label for="message">Message</label>
                        <textarea id="message" cols="60" rows="10" placeholder="Enter Your Message" name="message" class="input-field" required></textarea>
                    </div>
                    <input type="submit" value="Submit" id="submit-btn" class="submit-btn" />
                </form>
            </div>
        </div>
    </section>

    <!-- ====== Social accounts - Fixed to the right ====== -->
    z
    <div class="socials">
        <a href="#" target="_blank"><img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/twitter-logo.gif" alt="Twitter" loading="lazy" class="socicon" /></a>
        <a href="#" target="_blank"><img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/LinkedIn-logo.gif" alt="Linkedin" loading="lazy" class="socicon" /></a>
        <a href="#" target="_blank"><img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/github.gif" alt="Github" class="socicon" /></a>

        <a href="#" target="_blank"><img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/facebook.gif" alt="Facebook" loading="lazy" class="socicon" /></a>
        <a href="#" target="_blank"><img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/Medium.webp" alt="Blogger" loading="lazy" class="socicon" /></a>
        <a href="#" target="_blank"><img src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/youtube.png" alt="YouTube" loading="lazy" class="socicon" /></a>

    </div>
    <!-- ======= Scroll to top ======= -->

    <i class="scroll-up" id="scroll-up"><img
        src="https://ajay-dhangar.github.io/Portfollio.github.io/assets/icons/images.jpg"
        class="socicon up-arrow"
        alt="scroll-up"/></i>

    <!-- ======= Footer section ======= -->
    <footer>
        <p class="copy">&copy; Copyright 2022</p>
        <p class="copy">
            Built with &#x2661; by
            <a href="https://www.linkedin.com/in/ajay-dhangar-bb89b4227/" target="_blank">Ajay Dangar</a>
        </p>
    </footer>

    <!-- Website scripts -->
    <script src="./assets/js/app.js"></script>

    <!-- Ion icons scripts -->
    <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
    <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>


</body>

</html>
``` 

**Step: -3** write this code in the ```styles.css``` file.

```
:root {
    --variable-name: value;
}

@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,900;1,700&display=swap");

/* Variables */

:root {
    --font-family: "Roboto", sans-serf;
    --normal-font: 400;
    --bold-font: 700;
    --bolder-font: 900;
    --bg-color: #fcfcfc;
    --primary-color: #4756df;
    --secondary-color: #ff7235;
    --primary-shadow: #8b8eaf;
    --secondary-shadow: #a17a69;
    --bottom-margin: 0.5rem;
    --bottom-margin-2: 1rem;
    --line-height: 1.7rem;
    --transition: 0.3s;
}


/* Variables end */

html {
    scroll-behavior: smooth;
}


/* CSS Resets */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

ul {
    list-style-type: none;
}

a {
    text-decoration: none;
    color: var(--primary-color);
}

a:hover {
    color: var(--secondary-color);
}

body {
    font-family: var(--font-family);
}

nav {
    position: sticky;
    top: 0;
    left: 0;
    z-index: 1;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.5rem 3.5rem;
    background-color: var(--bg-color);
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.1);
}

nav h1 {
    color: #170da5;
}

nav a {
    color: var(--primary-color);
    transition: var(--transition);
}

nav a:hover {
    color: var(--secondary-color);
    border-bottom: 2px solid var(--secondary-color);
}

nav ul {
    display: flex;
    gap: 1.9rem;
}

nav ul li {
    font-weight: var(--bold-font);
}

.burger-menu {
    color: var(--primary-color);
    font-size: 2rem;
    border: 0;
    background-color: transparent;
    cursor: pointer;
    display: none;
}


/*  Hero */

.hero {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 2.5rem;
    max-width: 68.75rem;
    margin: auto;
}

.hero img {
    height: 35.5rem;
    width: 35.5rem;
}

.bio {
    width: 25rem;
    padding: 0.625rem;
    border-radius: 6px;
    box-shadow: 0px 2px 15px 2px var(--primary-shadow);
}

.bio h1 {
    margin-bottom: var(--bottom-margin);
}

.bio p {
    line-height: var(--line-height);
    padding: 0.3rem 0;
}


/*-==== More-About ====-*/

.more-about {
    background-color: var(--bg-color);
    padding: 1rem 6rem;
}

.more-about h2 {
    margin-bottom: var(--bottom-margin);
    text-align: center;
}

.more-about p {
    line-height: var(--line-height);
    padding: 0.4rem;
}

.details {
    font-size: 15px;
    color: #010105;
    text-shadow: #fff;
}


/*==== Skill section's css ====*/

.skills {
    max-width: 68.75rem;
    margin: auto;
    text-align: center;
    margin-top: 2.5rem;
}

.skill-header {
    margin-bottom: 1rem;
}

.skills-wrapper img {
    padding: 1.25rem;
}

.icon {
    width: 11.875rem;
    height: 11.25rem;
}

.icon-card {
    background-color: #fff;
    border-radius: 11px;
    box-shadow: 0 3px 10px var(--secondary-shadow);
    padding: 20px;
    margin: 10px;
}


/* === Project section css ===*/

.projects {
    background-color: var(--bg-color);
    padding: 32px 0;
    margin-top: 2rem;
}

.project-pic {
    width: 65%;
    height: 60%;
}

.projects-container {
    display: flex;
    align-items: center;
    justify-content: center;
}

.projects-title {
    text-align: center;
    margin-bottom: 1rem;
}

.project-container {
    text-align: center;
    width: 21.875rem;
    padding: 1rem;
}

.project-container p {
    padding: 0.4rem;
}

.project-title {
    margin-bottom: var(--bottom-margin);
}

.project-details {
    margin-bottom: var(--bottom-margin);
}

.project-card {
    background-color: #fff;
    border-radius: 11px;
    box-shadow: 0 3px 10px var(--primary-shadow);
    padding: 20px;
    margin: 10px;
}


/* Contact section css */

.contact {
    margin-top: 2rem;
}

.contact h2 {
    text-align: center;
    margin-bottom: var(--bottom-margin-2);
}

.contact-form-container {
    max-width: 40.75rem;
    margin: 0 auto;
    padding: 0.938rem;
    border-radius: 5px;
    box-shadow: 0 3px 10px var(--secondary-shadow);
}

.contact-form-container label {
    line-height: 2.7em;
    font-weight: var(--bold-font);
    color: var(--primary-color);
}

.contact-form-container textarea {
    min-height: 6.25rem;
    font-size: 14px;
}

.contact-form-container .input-field {
    width: 100%;
    padding-top: 10px;
    padding-bottom: 10px;
    border-radius: 5px;
    border: none;
    border: 2px outset var(--primary-color);
    font-size: 0.875rem;
    outline: none;
}

.input-field::placeholder {
    padding: 0.5rem;
    color: var(--primary-color);
}

.submit-btn {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    background-color: #fff;
    border: 2px solid var(--primary-color);
    border-radius: 5px;
    font-size: 1rem;
    font-weight: var(--bold-font);
    transition: var(--transition);
}

.submit-btn:hover {
    background-color: var(--primary-color);
    border: 2px solid var(--primary-color);
    cursor: pointer;
}

.socials {
    display: flex;
    flex-direction: column;
    position: fixed;
    right: 1%;
    bottom: 30%;
}

.socicon {
    width: 2rem;
    height: 2rem;
}

footer {
    background-color: var(--bg-color);
    padding: 1.25rem;
    text-align: center;
    margin: 2rem 0 0;
}

.scroll-up {
    position: fixed;
    right: 0.5%;
    bottom: 3%;
    cursor: pointer;
}

.up-arrow {
    width: 3rem;
    height: 3rem;
}

@media screen and (max-width: 720px) {
    /*changes reflects on screen with a width of 720px and below*/
    nav {
        padding: 1.5rem 1rem;
    }
    nav ul {
        position: fixed;
        background-color: var(--bg-color);
        flex-direction: column;
        top: 86px;
        left: 10%;
        width: 80%;
        text-align: center;
        transform: translateX(120%);
        transition: transform 0.5s ease-in;
    }
    nav ul li {
        margin: 8px;
    }
    .burger-menu {
        display: block;
    }
    nav ul.show {
        transform: translateX(0);
    }
    .hero {
        margin-top: -4rem;
        flex-direction: column;
        gap: 0;
    }
    .hero img {
        height: 32.5rem;
        width: 30rem;
    }
    hr.line {
        border: 1px solid green;
        border-radius: 3px;
    }
    .bio {
        margin-top: 0;
        width: 20.5rem;
    }
    .more-about {
        margin-top: 2rem;
        padding: 1rem 3.5rem;
    }
    .more-about h2 {
        text-align: center;
    }
    .more-about p {
        text-align: justify;
    }
    .details {
        font-size: 15px;
        color: #010105;
        text-shadow: #fff;
    }
    .icon {
        width: 5.875rem;
        height: 5.25rem;
    }
    .projects-container {
        flex-direction: column;
    }
    .project-container {
        width: 20.875rem;
    }
    .contact-form-container {
        max-width: 23.75rem;
    }
}

@media screen and (max-width: 420px) {
    .hero img {
        height: 37.5rem;
        width: 23rem;
    }
    .bio {
        width: 18.3rem;
    }
    .project-container {
        width: 17.875rem;
    }
    .contact-form-container {
        max-width: 17.75rem;
    }
}
``` 


**Step: -4** write this code in the ```app.js``` file.

```
// scroll to top functionality
const scrollUp = document.querySelector("#scroll-up");

scrollUp.addEventListener("click", () => {
    window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth",
    });
});
// Nav hamburgerburger selections

const burger = document.querySelector("#burger-menu");
const ul = document.querySelector("nav ul");
const nav = document.querySelector("nav");

burger.addEventListener("click", () => {
    ul.classList.toggle("show");
});
// Close hamburger menu when a link is clicked

// Select nav links
const navLink = document.querySelectorAll(".nav-link");

navLink.forEach((link) =>
    link.addEventListener("click", () => {
        ul.classList.remove("show");
    })
);
``` 


**Output:**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667397012586/d1tltmrKh.png align="left")

**Supported Browser:**

- Google Chrome
- Microsoft
- EdgeFirefox

**Supported Device:**

- Desktop
- Laptop
- Tablet
- Smartphone

Now your best portfolio website is completed. If you have any query then send me message in comment.

Have a Good day, and try to do better work.