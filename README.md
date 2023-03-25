<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <style>
            @import url("https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@300&display=swap");
    
                *{
                    margin:0;
                    padding:0;
                    box-sizing:border-box;
                    font-family: "Be Vietnam Pro", sans-serif;
                    scroll-behavior: smooth;
                }
                #wrapper{
                    height: 100vh;
                    overflow-y: auto;
                    overflow-x: hidden;
                }
                .container{
                    width: 1200px;
                    margin: 0px auto;
                }   
                .nav{
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    padding-top: 1rem;
                }
                .logo-container{
                    display: flex;
                    align-items: center ;
                }
                .logo{
                    width: 80px;
                }
                .logo-text{
                    margin-left: -1.2rem;
                    font-size: 28px;
                }
                .nav-items{
                    display: flex;
                    gap: 1.5rem;
                    padding: 4rem;
                }
                .nav-items div{
                    font-size: 20px;
                    font-weight: 500;
                    cursor: pointer;
                }
                .nav-items div a{
                    color: black;
                }
                a{
                    text-decoration: none;
                }
                .nav-items div:hover{
                    font-weight: bold;
                    transition: 0.8s;
                }
                .hero{
                    display: flex;
                    position: relative;
                    justify-content: center;
                    align-items: center;

                    gap: 5rem;
                    margin: 4rem auto;
                    padding: 0 1rem;
                    padding-bottom: 8rem;
                }
                .faded-text{
                    position: absolute;
                    user-select: none;
                    font-size: 5rem;
                    color: rgb(231, 231, 231);

                    bottom: -14.5%;
                    left: -5%;
                    font-weight: bold;
                    transition: all 3sec;
                }
                .hero-left{
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    gap: 2rem;
                }
                .hero-left-heading{
                    font-size: 35px;
                    color: #343d68;
                    font-weight: 500;
                }
                .role{
                    color: rgb(17, 0, 149);
                    font-weight: 800;
                }
                .hero-left-subheading{
                    font-size: 45px;
                    line-height: 45px;
                }
                .hero-left-desc{
                    margin-top: 1rem;
                    width: 70%;
                    font-weight: 500;
                }
                .pink-button {
                    background-color: rgb(172, 23, 0);
                    width: fit-content;
                    color: white;
                    padding: 0.8rem 2.3rem;
                    box-shadow: 5px 5px 7px 0px #0000003f;
                    font-size: 18px;
                    cursor: pointer;
                    transition: all 0.5s;
                    font-weight: 500;
                    border: solid 3px transparent;
                    position: relative;
                    z-index: 1;
                }
                .pink-button::before {
                    content: "";
                    position: absolute;
                    background-color: #fff;
                    top: 0px;
                    left: 0;
                    right: 0;
                    bottom: 0px;
                    z-index: -1;
                    transform: scaleX(0);
                    transform-origin: left;
                    transition: all 0.8s;
                }
                .pink-button:hover::before {
                    transform: scaleX(1);
                }
                .pink-button:hover {
                    border: solid 3px rgb(172, 23, 0);
                    color: black;
                    scale: 1.1;
                    transition: 1.25s;
                }
                .hero-right{
                    position: relative;
                }
                .absolute{
                    position: absolute;
                }
                .user-image{
                    padding: 2.5rem;
                    filter: grayscale(1);
                    transition: all 1s;
                    animation: scaleImage 5s linear infinite;
                }
                .user-image img{
                    z-index: -1;
                }
                @keyframes scaleImage {
                    0%{
                        filter: grayscale(0);
                        transform: scale(1);
                    }
                    50%{
                        transform: scale(1.1);
                        filter: grayscale(1);
                        box-shadow: 3px 3px 10px 0px black;
                    }
                    100%{
                        transform: scale(1);
                        filter: grayscale(0);
                    }
                }

                .icon-dots{
                    z-index: 1;
                    position: absolute;
                    bottom: -1rem;
                    right: 0rem;
                    animation: updown 5s linear infinite;
                }
                @keyframes updown {   
                    50%{
                        transform: translateY(-15px);
                    } 
                }
                .icon-cube{
                    z-index: 1;
                    position: absolute;
                    right: 0rem;
                    animation: rotate 3s linear infinite;
                }
                @keyframes rotate {
                    0%{
                        transform: translateY(0px) rotateY(0deg);
                    }
                    33%{
                        transform: translateY(15px) rotateY(120deg);
                    }
                    66%{
                        transform: translateY(0px) rotateY(240deg);
                    }
                    100%{
                        transform: rotateY(360deg);;
                    }
                }
                .icon-circle{
                    z-index: 1;
                    position: absolute;
                    bottom: -1rem;
                    animation: side 5s linear infinite;
                }
                @keyframes side {
                    50%{
                        left :5%;
                        bottom:10%;
                    }
                }
                .icon-plus{
                    z-index: 1;
                    position: absolute;
                    top: -0.8rem;
                    left: 50%;
                    animation: plusfor 5s linear infinite;
                }
                @keyframes plusfor {
                    50%{
                        top: 3%;
                        left: 45%x;
                    }
                }
                .icon-zigzag{
                    z-index: 1;
                    top: 1.5em;
                    left: -0.3em;
                    animation: shake 5s linear infinite;
                }
                @keyframes shake {
                    50%{
                        left: 5%;
                        top: 2%;
                    }
                }

                /* Project section */

                .projects-section{
                    background-color: rgb(231, 231, 231);
                    margin-top: 4rem;
                }

                .page-header{
                    color: orangered;
                    text-align: center;
                    font-size: 90px;
                    padding-top: 30px;
                }

                .project-container{
                    max-width: 1200px;
                    margin: 0 auto;
                    padding: 3rem 0;

                    display: flex;
                    flex-direction: column;
                    gap: 5rem;
                }

                .project-card{
                    width: 90%;
                    height: 550px;
                    background-size: cover;
                    position: relative;
                    box-shadow: 0px 0px 40px #765151;
                }

                #project1{
                    background-image: url(./project_portfolio.JPG);
                }

                #project2{
                    background-image: url(./my_gallery.JPG);
                    margin-left: 10%;
                }

                #project3{
                    background-image: url(./project_portfolio.JPG);
                }

                #project4{
                    background-image: url(./project_portfolio.JPG);
                    margin-left: 10%;
                }
                .project-card::after{ /*They are known as pseudo selectors*/
                    content: "";
                    position: absolute;
                    top: 0; 
                    left: 0;
                    right: 0;
                    bottom: 0;
                    background-color: #1f1f1f9a;
                    transform: scaleX(1);
                    z-index: 0;
                }
                .project-card::before{
                    content: "";
                    position: absolute;
                    top: 0;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    background: linear-gradient(45deg, #343d68, #343d68be, #343d687c);
                    transform: scaleX(0);
                    transform-origin: left;
                    transition: all 0.4s;
                    z-index: 1;
                }
                .project-card:hover::before{
                    transform: scaleX(1);
                }
                .project-card:hover .project-number{
                    transition: 1.25s;
                    display: block;
                }   
                .project-number{
                    position: absolute;
                    font-size: 200px;
                    font-weight: 600;
                    color: rgb(251, 251, 251);
                    z-index: 5;
                    display: none;
                }
                .odd{
                    right: -70px;
                    top: -70px;
                }
                .even{
                    left: -70px;
                    top: -70px;
                }
                .project-content{
                    width: 70%;
                    text-align: left;
                    position: absolute;
                    display: flex;
                    flex-direction: column;
                    color: white;
                    padding: 2rem;
                    bottom: 20%;
                    z-index: 5;
                    gap: 1rem;
                    transition: all 0.4s;
                }
                .project-card:hover .project-content{
                    transform: scale(1.1);
                }
                .odd-left{
                    left: 10%;
                }
                .even-right{
                    right: 10%;
                }
                .project-skills-container{
                    width: 60%;
                    display: flex;
                    gap: 10px;
                    flex-wrap: wrap;
                }
                .project-skill{
                    width: 40px;
                }
                .project-heading{
                    font-size: 50px;
                    font-weight: bold;
                    line-height: 3rem;
                }
                .project-subheading{
                    width: 70%;
                    font-style: italic;
                }

                .btn-grp{
                    display: flex;
                    gap: 10px;
                    align-items: center;
                }
                .btn-project{
                    border: none;
                }
                .btn-project:hover{
                    border: none;
                    scale: 1;
                }
                .icon{
                    height: 40px;
                    cursor: pointer;
                    color: white;
                    font-size: 35px;
                }
                .icon:hover{
                    color: orangered;
                    transition: 1.25s;
                }

                /* Skills Section */
                .skills-container{
                    position: relative;
                    display: flex;

                    padding: 5rem;
                    margin: 10rem auto;
                    gap: 30px;
                }
                .skill-container-left{
                    display: flex;
                    flex-direction: column;
                    width: 50%;
                }
                .skill-heading{
                    font-size: 50px;
                    font-style: bold;
                    color: orangered;
                    line-height: 50px;
                }
                .caps{
                    font-size: 90px;
                }
                .skill-subheading{
                    margin-top: 1rem;
                    width: 85%;
                    text-align: justify;
                }
                .skill-subheading p{
                    margin: 15px 0;
                }
                .skill-container-right{
                    display: flex;
                    width: 50%;
                    position: relative;
                    gap: 10px;
                    flex-wrap: wrap;
                }
                .skill-fade-text{
                    position: absolute;
                    user-select: none;
                    font-size: 15rem;
                    color: rgb(231,231,231);
                    bottom: -34.5%;
                    right: -30%;
                }
                .blob-style{
                    position: absolute;
                    z-index: -1;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    animation: blobAnimate 5s linear infinite;
                }
                @keyframes blobAnimate {
                    50%{
                        top: 54%;
                        left: 56%;
                    }
                }
                .skills-logo{
                    width: 90px;
                    border-radius: 20px;
                    transition: all 1s;
                }

                .skills-logo:hover{
                    transform: scale(1.2);
                    box-shadow: 0px 0px 40px #765151;
                }

                /* Contact Us Form */

                .contactus-from-container{
                    width: 100%;
                    background-color: rgb(231, 231, 231);
                }
                .contact-us-heading{
                    font-size: 5rem;
                    color: orangered;
                    padding: 2rem 0;
                }
                .contact-us-sub-heading{
                    font-size: 3rem;
                    color: #343d68aa;
                    text-transform: capitalize;
                }
                .contact-us-form-container{
                    display: flex;
                    flex-direction: column;
                    margin-top: 25px;
                    align-items: center;
                    justify-content: center;
                }
                .form{
                    display: flex;
                    flex-direction: column;
                    margin: 2rem 5rem;
                    width: 70%;
                }
                .formfield-container{
                    width: 100%;
                }
                .formfield{
                    border-radius: 4px;
                    width: 100%;
                    height: 38px;
                    padding: 0 2rem;
                    font-size: 18px;
                    box-shadow: 2px 2px 10px #1f1f1f;
                    border: none;
                    font-weight: 500;
                    margin: 1rem;
                }
                .formfield-textarea{
                    height: 200px;
                    padding-top: 1rem;
                }
                .btn-container{
                    width: 70%;
                    padding: 0 0 2rem 1rem;
                }
                #submit-btn{
                    border: none;
                }
                #submit-btn:hover {
                    border: none;
                    color: black;
                    scale: 0.85;
                    transition: 1.25s;
                }

                /* Footer Section */
                footer{
                    position: relative;
                    margin-top: -1px;
                    background-color: #343d68;
                    padding: 5rem;
                }
                .footer-wrapper{
                    display: flex;
                    gap: 1rem;
                    padding: 1.2rem;
                    justify-content: space-between;
                    align-items: center;
                }
                .link-wrapper{
                    display: flex;
                    gap: 1.2rem;
                    font-size: 20px;
                }
                .link-wrapper div a{
                    text-decoration: none;
                    color: #fff;
                }
                .link-wrapper div a:hover{
                    font-weight: bold;
                    transition: 1.5s;
                    color: orangered;
                }
                .icon-wrapper{
                    display: flex;
                    gap: 1.2rem;
                    font-size: 40px;
                }
                .img-link:hover{
                    transition: 1.25s;
                    transform: scale(1.5);
                }
                .footer-faded-text{
                    position: absolute;
                    left: 0;
                    bottom: 0;
                    color: #535c87;
                    user-select: none;
                    font-size: 5em;
                }

        </style>
    </head>
    <body>
        <div id="wrapper">
            <div class="container">
                <div class="nav">
                    <div class="logo-container">
                        <img src="s_logo.png" class="logo">
                        <div class="logo-text">ubham Sharma</div>
                    </div>
                    <div class="nav-items">
                        <div><a href="#projects">Projects</a></div>
                        <div><a href="#skills">Skills</a></div>
                        <div><a href="#certificates">Certificates</a></div>
                        <div><a href="#contact">Contact Me</a></div>
                    </div>
                </div>
                <div class="hero">
                    <div class="faded-text">Subham Sharma</div>
                    <div class="hero-left">
                        <div class="hero-left-heading">Hii! Subham Sharma</div>
                        <div class="hero-left-heading hero-left-subheading">
                            I am a <span class="role"></span>
                        </div>
                        <div class="hero-left-desc">
                            I'm a student of B.Tech with specialization in computer science 
                            and engineering. On my portfolio you will learn about my journey 
                            for becoming a software devloper.
                        </div>
                        <div class="pink-button" id="btn-pink">Hire Me</div>
                    </div>
                    <div class="hero-right">
                        <div class="absolute icons icon-dots">
                            <img src="dots.png" alt="dots" width="50px">
                        </div>
                        <div class="absolute icons icon-cube">
                            <img src="cube.png" alt="dots"/>
                        </div>
                        <div class="absolute icons icon-circle">
                            <img src="circle.png" alt="dots"/>
                        </div>
                        <div class="absolute icons icon-zigzag">
                            <img src="zigzags.png" alt="dots"/>
                        </div>
                        <div class="absolute icons icon-plus">
                            <img src="plus.png" alt="dots"/>
                        </div>
                        <div class="user-image">
                            <img src="my_image.jpg" alt="dots" width="380px"/>
                        </div>
                    </div>
                </div>
            </div>
            <div id="projects" class="projects-section">
                <h2 class="page-header">Projects</h2>
                <div class="project-container">
                    <div class="project-card" id="project1">
                        <div class="project-number odd">01</div>
                        <div class="project-content odd-left">
                            <div class="project-skills-container">
                                <img class="project-skill" src="HTML.png" alt="" />
                                <img class="project-skill" src="CSS.png" alt="" />
                                <img class="project-skill" src="Javascript.svg" alt="" />
                                <img class="project-skill" src="Express.png" alt="" />
                                <img class="project-skill" src="NextJsCircle.png" alt="" />
                                <img class="project-skill" src="Tailwind.png" alt="" />
                                <img class="project-skill" src="NodeJs.svg" alt="" />
                                <img class="project-skill" src="MongoDB.svg" alt="" />
                                <img class="project-skill" src="Redux.svg" alt="" />
                                <img class="project-skill" src="Vercel.svg" alt="" />
                            </div>
                            <h2 class="project-heading">My Portfolio</h2>
                            <p class="project-subheading">
                                This is my portfolio, tells you about myself, my skills and about my project with some extra information
                            </p>   
                            <div class="btn-grp">
                                <div class="pink-button btn-project">Read More</div>
                                <img class="fa-bands fa-github icon" src="gitLogo.png">
                                <a href="">
                                    <i title="Live Link" class="fa-solid fa-link icon"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="project-card" id="project2">
                        <div class="project-number even">02</div>
                        <div class="project-content even-right">
                            <div class="project-skills-container">
                                <img class="project-skill" src="HTML.png" alt="" />
                                <img class="project-skill" src="CSS.png" alt="" />
                                <img class="project-skill" src="Javascript.svg" alt="" />
                                <img class="project-skill" src="Tailwind.png" alt="" />
                                <img class="project-skill" src="MongoDB.svg" alt="" />
                            </div>
                            <h2 class="project-heading">My Gallery</h2>
                            <p class="project-subheading">
                                This is my galley project helps you to see relavent pictures of a particular field, and 
                                also if you have any account then you can probably add or download any picture.
                                Read more about this project on github below.
                            </p>  
                            <div class="btn-grp">
                                <div class="pink-button btn-project">Read More</div>
                                <img class="fa-bands fa-github icon" src="gitLogo.png">
                                <a href="">
                                    <i title="Live Link" class="fa-solid fa-link icon"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="project-card" id="project3">
                        <div class="project-number odd">03</div>
                        <div class="project-content odd-left">
                            <div class="project-skills-container">
                                <img class="project-skill" src="HTML.png" alt="" />
                                <img class="project-skill" src="CSS.png" alt="" />
                                <img class="project-skill" src="Javascript.svg" alt="" />
                                <img class="project-skill" src="Express.png" alt="" />
                                <img class="project-skill" src="NextJsCircle.png" alt="" />
                                <img class="project-skill" src="Tailwind.png" alt="" />
                                <img class="project-skill" src="NodeJs.svg" alt="" />
                                <img class="project-skill" src="MongoDB.svg" alt="" />
                                <img class="project-skill" src="Redux.svg" alt="" />
                                <img class="project-skill" src="Vercel.svg" alt="" />
                            </div>
                            <h2 class="project-heading">My Portfolio</h2>
                            <p class="project-subheading">
                                This is my portfolio, tells you about myself, my skills and about my project with some extra information
                            </p>   
                            <div class="btn-grp">
                                <div class="pink-button btn-project">Read More</div>
                                <img class="fa-bands fa-github icon" src="gitLogo.png">
                                <a href="">
                                    <i title="Live Link" class="fa-solid fa-link icon"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="project-card" id="project4">
                        <div class="project-number even">04</div>
                        <div class="project-content even-right">
                            <div class="project-skills-container">
                                <img class="project-skill" src="HTML.png" alt="" />
                                <img class="project-skill" src="CSS.png" alt="" />
                                <img class="project-skill" src="Javascript.svg" alt="" />
                                <img class="project-skill" src="Express.png" alt="" />
                                <img class="project-skill" src="NextJsCircle.png" alt="" />
                                <img class="project-skill" src="Tailwind.png" alt="" />
                                <img class="project-skill" src="NodeJs.svg" alt="" />
                                <img class="project-skill" src="MongoDB.svg" alt="" />
                                <img class="project-skill" src="Redux.svg" alt="" />
                                <img class="project-skill" src="Vercel.svg" alt="" />
                            </div>
                            <h2 class="project-heading">My Portfolio</h2>
                            <p class="project-subheading">
                                This is my portfolio, tells you about myself, my skills and about my project with some extra 
                                information.
                            </p>   
                            <div class="btn-grp">
                                <div class="pink-button btn-project">Read More</div>
                                <img class="fa-bands fa-github icon" src="gitLogo.png">
                                <a href="">
                                    <i title="Live Link" class="fa-solid fa-link icon"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div id="skills" class="skills-container container">
                <div class="skill-fade-text">Skills</div>
                <div class="skill-container-left">
                    <h2 class="skill-heading">
                        <span class="caps">M</span>e and
                        <br>
                        MyTech Stack
                    </h2>
                    <div class="skill-subheading">
                        <p>
                            Hi! everyone My name is Subham Sharma I am a full stack web devloper and also a android devloper.
                            I have been working on myself from last 3 year to develop my skills in both these areas.
                            Currently, I am looking for an internship in which I can work on myself and gain some hands on experience in the real world entities.
                        </p>
                        <p>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio voluptatum et eaque unde 
                            sapiente ipsam non laboriosam aliquid facilis veritatis delectus aut, sunt expedita maiores ab 
                            laudantium eligendi ex suscipit? Vero obcaecati mollitia assumenda repellat temporibus voluptatibus. 
                            Voluptatum exercitationem hic enim ad. Ad sapiente debitis in perspiciatis, magni nobis fuga reiciendis 
                            dignissimos sequi eveniet at possimus consequatur nostrum molestiae fugit excepturi.
                        </p>
                    </div>
                </div>
                <div class="skill-container-right">
                    <img class="blob-style" src="./blob vector.png">

                    <img class="skills-logo" src="./Express.png">
                    <img class="skills-logo" src="./HTML.png">
                    <img class="skills-logo" src="./Javascript.svg">
                    <img class="skills-logo" src="./Vercel.svg">
                    <img class="skills-logo" src="./Tailwind.png">
                    <img class="skills-logo" src="./Redux.svg">
                    <img class="skills-logo" src="./NodeJs.svg">
                    <img class="skills-logo" src="./NextJsCircle.png">
                    <img class="skills-logo" src="./MongoDB.svg">
                    <img class="skills-logo" src="./java.jpg">
                    <img class="skills-logo" src="./Cpp.png">
                    <img class="skills-logo" src="./Bash.svg">
                    <img class="skills-logo" src="./Bootstrap.svg">
                    <img class="skills-logo" src="./ChartJs.svg">
                    <img class="skills-logo" src="./CSS.png">
                    <img class="skills-logo" src="./Docker.svg">
                    <img class="skills-logo" src="./Git.svg">
                    <img class="skills-logo" src="./Github.svg">
                    <img class="skills-logo" src="./Graphql.svg">
                    <img class="skills-logo" src="./K8s.svg">

                </div>
            </div>
            <div id="contact" class="contactus-from-container">
                <div class="container">
                    <h1 class="contact-us-heading">Contact Me</h1>
                    <h2 class="contact-us-sub-heading">
                        Questions, Thoughts, Or Just Want To Say Hello...
                    </h2>

                    <div class="contact-us-form-container">
                        <form class="form" action="">
                            <div class="formfield-container">
                                <input class="formfield" 
                                type="text" 
                                name="name" 
                                id="" 
                                placeholder="Enter Your Name" />
                                
                                <input class="formfield" 
                                type="email" 
                                name="email" 
                                id="" 
                                placeholder="Enter Your Email Address" />
                                
                                <input class="formfield" 
                                type="text" 
                                name="subject" 
                                id="" 
                                placeholder="Enter Your Subject" />
                                
                                <textarea name="message"
                                id="" cols="30" rows="10" 
                                class="formfield formfield-textarea"
                                placeholder="Enter Your Message"></textarea>
                            </div>
                        </form>
                        <div class="btn-container">
                            <button type="submit" class="pink-button" id="submit-btn">
                                Send Message<i class="submit-icon fa-solid fa-paper-plane"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            <footer>
                <div class="container">
                    <div class="footer-wrapper">
                        <div class="footer-faded-text">Subham Sharma</div>
                        <div class="link-wrapper">
                            <div>
                                <a href="#projects">Projects</a>
                            </div>
                            <div>
                                <a href="#skills">Skills</a>
                            </div>
                            <div>
                                <a href="#contact">Contact Me</a>
                            </div>
                        </div>
                        <div class="icon-wrapper">
                            <i class="img-link fa-solid fa-envelope" style="color: #ffffff;"></i>
                            <i class="img-link fa-brands fa-square-twitter" style="color: #ffffff;"></i>
                            <i class="img-link fa-brands fa-linkedin" style="color: #ffffff;"></i>
                            <i class="img-link fa-brands fa-github" style="color: #ffffff;"></i>
                            <i class="img-link fa-brands fa-instagram" style="color: #ffffff;"></i>
                        </div>
                    </div>
                </div>
            </footer>
        </div>
        <script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
        <script src="https://kit.fontawesome.com/58a810656e.js" crossorigin="anonymous"></script>
        <script>
            var typeData = new Typed(".role", {
            strings: [
                "Problem Solver",
                "UI/UX Designer",
                "Web Developer",
                "Coder",
            ],
            loop: true,
            typeSpeed: 120,
            backSpeed: 100,
            backDelay: 1000,
            });
        </script>
    </body>
</html>
