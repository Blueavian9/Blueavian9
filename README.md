# My GitHub Repository

Welcome to my GitHub repository! Here's a cool penguin animation:

<details>
<summary>Click to see the penguin!</summary>

<div class="penguin">
  <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="./styles.css" />
    <title>Penguin</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  </head>

  <body>
    <div class="left-mountain"></div>
    <div class="back-mountain"></div>
    <div class="sun"></div>
    <div class="penguin">
      <div class="penguin-head">
        <div class="face left"></div>
        <div class="face right"></div>
        <div class="chin"></div>
        <div class="eye left">
          <div class="eye-lid"></div>
        </div>
        <div class="eye right">
          <div class="eye-lid"></div>
        </div>
        <div class="blush left"></div>
        <div class="blush right"></div>
        <div class="beak top"></div>
        <div class="beak bottom"></div>
      </div>
      <div class="shirt">
        <div>💜</div>
        <p>I CSS</p>
      </div> 
      <div class="penguin-body">
        <div class="arm left"></div>
        <div class="arm right"></div>
        <div class="foot left"></div>
        <div class="foot right"></div>
      </div>
    </div>

    <div class="ground"></div>
  </body>
</html>
</div>

<style>
  :root {
  --penguin-face: white;
  --penguin-picorna: orange;
  --penguin-skin: gray;
}

body {
  background: linear-gradient(45deg, rgb(118, 201, 255), rgb(247, 255, 222));
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.left-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(80, 183, 255));
  position: absolute;
  transform: skew(0deg, 44deg);
  z-index: 2;
  margin-top: 100px;
}

.back-mountain {
  width: 300px;
  height: 300px;
  background: linear-gradient(rgb(203, 241, 228), rgb(47, 170, 255));
  position: absolute;
  z-index: 1;
  transform: rotate(45deg);
  left: 110px;
  top: 225px;
}

.sun {
  width: 200px;
  height: 200px;
  background-color: yellow;
  position: absolute;
  border-radius: 50%;
  top: -75px;
  right: -75px;
}

.penguin {
  width: 300px;
  height: 300px;
  margin: auto;
  margin-top: 75px;
  z-index: 4;
  position: relative;
  transition: transform 1s ease-in-out 0ms;
}

.penguin * {
  position: absolute;
}

.penguin:active {
  transform: scale(1.5);
  cursor: not-allowed;
}

.penguin-head {
  width: 50%;
  height: 45%;
  background: linear-gradient(
    45deg,
    var(--penguin-skin),
    rgb(239, 240, 228)
  );
  border-radius: 70% 70% 65% 65%;
  top: 10%;
  left: 25%;
  z-index: 1;
}

.face {
  width: 60%;
  height: 70%;
  background-color: var(--penguin-face);
  border-radius: 70% 70% 60% 60%;
  top: 15%;
}

.face.left {
  left: 5%;
}

.face.right {
  right: 5%;
}

.chin {
  width: 90%;
  height: 70%;
  background-color: var(--penguin-face);
  top: 25%;
  left: 5%;
  border-radius: 70% 70% 100% 100%;
}

.eye {
  width: 15%;
  height: 17%;
  background-color: black;
  top: 45%;
  border-radius: 50%;
}

.eye.left {
  left: 25%;
}

.eye.right {
  right: 25%;
}

.eye-lid {
  width: 150%;
  height: 100%;
  background-color: var(--penguin-face);
  top: 25%;
  left: -23%;
  border-radius: 50%;
}

.blush {
  width: 15%;
  height: 10%;
  background-color: pink;
  top: 65%;
  border-radius: 50%;
}

.blush.left {
  left: 15%;
}

.blush.right {
  right: 15%;
}

.beak {
  height: 10%;
  background-color: var(--penguin-picorna);
  border-radius: 50%;
}

.beak.top {
  width: 20%;
  top: 60%;
  left: 40%;
}

.beak.bottom {
  width: 16%;
  top: 65%;
  left: 42%;
}

.shirt {
  font: bold 25px Helvetica, sans-serif;
  top: 165px;
  left: 127.5px;
  z-index: 1;
  color: #6a6969;
}

.shirt div {
  font-weight:  initial;
  top: 22.5px;
  left: 12px;
}

.penguin-body {
  width: 53%;
  height: 45%;
  background: linear-gradient(
    45deg,
    rgb(134, 133, 133) 0%,
    rgb(234, 231, 231) 25%,
    white 67%
  );
  border-radius: 80% 80% 100% 100%;
  top: 40%;
  left: 23.5%;
}

.penguin-body::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 45%;
  background-color: var(--penguin-skin);
  top: 10%;
  left: 25%;
  border-radius: 0% 0% 100% 100%;
  opacity: 70%;
}

.arm {
  width: 30%;
  height: 60%;
  background: linear-gradient(
    90deg,
    var(--penguin-skin),
    rgb(209, 210, 199)
  );
  border-radius: 30% 30% 30% 120%;
  z-index: -1;
}

.arm.left {
  top: 35%;
  left: 5%;
  transform-origin: top left; 
  transform: rotate(130deg) scaleX(-1);
  animation: 3s linear infinite wave;
}

.arm.right {
  top: 0%;
  right: -5%;
  transform: rotate(-45deg);
}

@keyframes wave {
  10% {
    transform: rotate(110deg) scaleX(-1);
  }
  20% {
    transform: rotate(130deg) scaleX(-1);
  }
  30% {
    transform: rotate(110deg) scaleX(-1);
  }
  40% {
    transform: rotate(130deg) scaleX(-1);
  }
}

.foot {
  width:  15%;
  height: 30%;
  background-color: var(--penguin-picorna);
  top: 85%;
  border-radius: 50%;
  z-index: -1;
}

.foot.left {
  left: 25%;
  transform: rotate(80deg);
}

.foot.right {
  right: 25%;
  transform: rotate(-80deg);
}

.ground {
  width: 100vw;
  height: 400px;
  background: linear-gradient(90deg, rgb(88, 175, 236), rgb(182, 255, 255));
  z-index: 3;
  position: absolute;
  margin-top: -58px;
}
</style>

</details>

## About this repository

This repository contains ...
Hello, My Name is Cesar Aguilar 👋
 
I am a results-driven Front End Engineer with 2+ years of experience building robust web applications at Bloom Institute of Technology. My technical expertise includes:

Developing a secure, user-friendly Full-Stack Asylum Report Generator app using Auth0 and collaborating with cross-functional teams
Building RESTful APIs, performing CRUD operations, and implementing efficient database schemas using Node, Express, and Knex
Creating dynamic web applications with React, leveraging Axios for API interactions, and useState hooks for state management
My background in security and access control management showcases my ability to work effectively in fast-paced environments while maintaining a strong focus on safety and compliance. My passion for web development, coupled with my diverse skill set and dedication to delivering high-quality solutions, makes me an ideal candidate for a software development role in the tech industry.



## 💬 Aks me about: 

| **FRONT END SKILLS AND EXPERIENCE**                                                                |  
|----------------------------------------------------------------------------------------------------|
| **UI/UX Principles**       | **PostgreSQL Administration** | **CSS Accesibility**                  |
| **CSS Variables**          | **Web Applications**          | **Application Testing**               |
| **HTML5 Markup**           | **Desktop Applications**      | **CSS Box Model**                     |
| **CSS3 Markup**            | **CSS Flexbox**               | **CSS Typography**                    |
| **CSS Grid**               | **ES6**                       | **Deployment**                        |
| **Context API**            | **Python3**                   | **VS Code**                           |
| **Express**                | **SaaS**                      | **Bootstrap**                         | 
| **Server Administration**  | **Project Management**        | **Figma Framework**                   | 
| **Java Programming**       | **Flask Micro-Framework**     | **Responsive Web Design Principles**  | 
| **React JS Projects**      | **Tailwind CSS Projects**     | **Linux Administration**              |
| **Gitbash commandline**    | **React Router**              | **Redux**                             |
| **Git CLI**                | **UI Principles**             | **Debugging**                         |
|                                                                                                    |
| **BACK END SKILLS AND EXPERIENCE**                                                                 |
|                                                                                                    |
| **MySQL**                  | **SQLite**                    | **JQuery**                            | 
| **React State Management   | **HTTP/Ajax                   | **TypeScript**                        |
| **DOM.JS**                 | **Unit Testing**              | **Node.JS**                           | 
| **Next.JS**                | **Primality  Testing Algorithms** | **Tables**                        |  
| **Cypress**                | **POSTMAN**                   | **SANITY**                            |
| **Dynamic Programming**    | **Exponential by Squaring**   | **String Matching and Parsing**       |
| **OOP**                    |  **Agile Project Management** | **Architecture**                      |
| **WebAPI'sDataPersistence**|  **Authentication**           | **Auth0 Security**                    |               |

  
- 📫 Reach out to me at: blueavian9@gmail.com | https:// Linkedin.com/in/cesar-aguilar-blueavian9


<h3 align="left">Connect</h3>
<p align="left"><a href="https://www.linkedin.com/in/cesar-aguilar-blueavian9/" target="blank"><img align="center" src="https://rawgithubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="Cesar-Aguilar" height="30" width="40" /></a>
</p>

<h3 align="left">Languages and Tools:</h3>
<p>
 <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/ides/pycharm.svg" width="50px" alt="pycharm" />
 <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/frameworks/boostrap.svg" width="50px" alt="bootstrap" />
 <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/frameworks/django.svg" width="50px" alt="django" />
 <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/frameworks/react.svg" width="50px" alt="react" />
 <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/frameworks/redux.svg" width="50px" alt="redux" />
 <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/frameworks/nodejs.svg" width="50px" alt="nodejs" />
 <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/frameworks/angular.svg" width="50px" alt="angular" />
</p>

<p>
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/cloud/github.svg" width="50px" alt="github" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/cloud/heroku.svg" width="50px" alt="heroku" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/databases/mysql.svg" width="50px" alt="mysql" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/others/npm.svg" width="50px" alt="npm" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/others/git.svg" width="50px" alt="git" />
</p>

<p>
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/others/html.svg" width="50px" alt="html" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/others/css.svg" width="50px" alt="css" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/others/json.svg" width="50px" alt="json" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/programming%20languages/bash.svg" width="50px" alt="bash" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/programming%20languages/java.svg" width="70px" alt="java" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/programming%20languages/javascript.svg" width="50px" alt="javascript" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/programming%20languages/python.svg" width="50px" alt="python" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/programming%20languages/typescript.svg" width="50px" alt="typescript" />
  <img align="center" src="https://raw.githubusercontent.com/yurijserrano/Github-Profile-Readme-Logos/master/text%20editors/vscode.svg" width="50px" alt="vscode" />
</p>



![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Redux](https://img.shields.io/badge/redux-%23593d88.svg?style=for-the-badge&logo=redux&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
<br>
![Styled Components](https://img.shields.io/badge/styled--components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![NodeJS](https://img.shields.io/badge/node.js-%2343853D.svg?style=for-the-badge&logo=node.js&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=red)
<!--
![Jest](https://img.shields.io/badge/-jest-%23C21325?style=for-the-badge&logo=jest&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)


<p><img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=decagondev&theme=dracula&count_private=true&show_icons=true&locale=en&layout=compact" alt="decagondev" /></p>

 <img align="center" src="https://github-readme-stats.vercel.app/api?username=decagondev&show_icons=true&locale=en&theme=dracula&count_private=true&hide=stars" alt="decagondev" />

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=decagondev&theme=dracula" alt="decagondev" /></p>
**decagondev/decagondev** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile. -->



- 😄 I am excited to be part of a team that contributes on projects of great importance and would love to discuss any opportunities for further reconsideration. 

- 🔭 I’m currently working on 3D Portfolio using tailwindcss, React class components, where i display multifple projects i have built during my Coding Bootcamp Journey ...
- 👯 I’m looking to collaborate and help out as much as possible i am dedicated, hard-working and believe that it is better to give than to recieve...
- 🤔 I’m looking for help with masterying my Algorithms and Data Structures to an Expert level based knowledge...
- 💬 Ask me about the projects that i have worked on and what kind of stuff I am building now as a Full-stack Software Engineer Graduate.
- 👨‍💻  With 2+ years of real world hands-on experience at Bloom Institute of Technology and a proven track record of collaborating with teams to build cutting-edge applications, I am poised to make an immediate impact on your development team. 
- I'm currently learning Java

- 🌱 I'm looking for help with getting experience / unpaid internship / non-profit / contribute

- ⚡ Fun facts: I am a dedicated, caring, and hardworking husband  Another fun fact is that ever since I can remember, I have always been fascinated by programming, dating back to the Myspace era.

-  📝 through out my 7+ self-taught years, I have learned to fall in love with knowledge, and appreciate the History of A.I. and Technology in General.
-   
- I graduated with Academic Achievement Awards in Social Studies.
