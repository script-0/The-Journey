<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/bernardofsr">
    <img src="images/logo.png" alt="Logo" width="150" height="150">
  </a>

  <h3 align="center">𝒥𝑜𝓊𝓇𝓃𝑒𝓎 𝑜𝓃 𝒫𝑒𝓃𝓉𝑒𝓈𝓉𝒾𝓃𝑔 𝒲𝑜𝓇𝓁𝒹</h3>

  <p align="center">
    This project is mainly dedicated to people who are <br>starting in Cybersecurity, especially in the area of Penetration Testing, like me.
    <br />
    </br>
    <a href="https://github.com/bernardofsr"><strong>Explore the docs »</strong></a>
    <br />
    <a href="mailto:bernardofsr@protonmail.com">Report Bug</a>
    ·
    <a href="mailto:bernardofsr@protonmail.com">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li><a href="#about-me">About Me</a></li>
    <li><a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#my-toolkit">My Toolkit</a></li>
      </ul>
    </li>
    <li>
      <a href="#lets-testing">Let's Testing</a>
      <ul>
        <li><a href="#authentication-tests">Authentication Tests</a></li>
        <li><a href="#not-sanitized-inputs">Not Sanitized Inputs</a></li>
        <li><a href="#information-disclosure-on-errors">Information Disclosure on Errors</a></li>
      </ul>
    </li>
    <li>
    <a href="#learning-material">Learning Material</a>
      <ul>
        <li><a href="#awesome-resources">Awesome Resources</a></li>
        <li><a href="#awesome-tools">Awesome Tools</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

##

<!-- About Me -->
## About Me 👨‍💻

I'm Bernardo Rodrigues and I'm currently a Penetration Tester trainee at <a href="https://cipher.com">Cipher</a>. 


<!-- ABOUT THE PROJECT -->
## About The Project 🧩

<p>Getting directly into the Cybersecurity without a working background in the area may not be the easiest situation in the world and perhaps the opportunities will not appear so quickly, but nothing is impossible and I hope you will be able to learn a few things from this project. <p>
Penetration testing is a specific area of cybersecurity and requires knowledge of existing vulnerabilities and how to exploit them. Later on, links will be added to other projects and articles that may be important in learning and that helped me get into the field.

`The Journey` `Cybersecurity` `Pentest` `Hacking` `RedTeam`

<br>

<!-- GETTING STARTED -->
## Getting Started

Since this project is directly designed for people who are entering the area of Penetration Testing, the topics will not be extremely deep and serve only as a basis and guide for learning.

### Prerequisites

1. Computer fundamentals :computer:
2. Desire to learn :books:
3. Coffee :coffee:

### My Toolkit 

Despite the immensity of existing tools at this moment, after some time some tools will be part of your day to day and are essential for your projects.
Some of my favorite tools:
* Intercept and edit requests:
  ```
  Burp Suite 
  ```
* Scan Target:
  ```
  nmap | naabu | rustscan
  ```
* Find Subdomains:
  ```
  FeroxBuster | Subslist3r | Subfinder
  ```
* Probe Domains and Subdomains:
  ```
  httpx
  ```
* Fast information about subdomains:
  ```
  Aquatone 
  ```
* First test for vulnerabilities:
  ```
  Nuclei
  ```

<br>


<!-- Lets Testing -->
## Let's Testing

Since this project was designed for people who are starting out in the field, the themes will not be very deep and the only objective is to help learning.


<!-- Authentication Tests-->
## Authentication Tests 🔑

"Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know." - <a href="https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html" target="_blank">OWASP</a>

```
1. Credentials or Important Data sent over HTTP

Intercept authentication related methods like: Login, Account Registration, Password Recovery, Password Reset.
Check for important data sent through HTTP.
If the information is being sent over HTTPS, change to HTTP and observe if data are sent.


2. Weak or Non-Existent Anti Brute-Force Mechanism

Create an account (some mechanism can block the account).
Intercept login request and sent request to intruder. 
Use multiple random data and check if you are blocked by any protection mechanism.
Tip: If after test brute-force mechanism doesn't block the account, try to disclose admin or possible staff email and try most common passwords. This way you make tests for Weakness Mechanisms and Default Passwords in use.


3. Weak Password Policy

When creating your account for tests, try to set weak passwords like: 12345 or admin.


4. Weak Password Change or Reset

Try to add header X-Forwarded-Host of your own server and see if you receive the request.
Try X-Forwarded-For and check if after click the link you receive the request on your server.


5. Use authentication to enumerate

See what errors are displayed when you try wrong credentials. If the web application show something like: The password is incorrect when you use correct username, but display Wrong Username when you use wrong username, you can performe enumeration of registered usernames. Same with emails.
```

<br>

<!-- Not Sanitized Inputs-->
## Weak or Non Existent Sanitization 🧨

An extremely common vulnerability is the lack of sanitization of inputs. When this happens, it is normal to be able to explore XSS or SQL Injection for example.

```
1. Understand how application works

First try to not activate some type of existent WAF with payloads. 
Try what characters are allowed and processed by the Web Application like: / < > ` " '


2. Test with payload

First payload I like to try: "><script>alert("XSS")</script>


3. XSS triggered? Maybe we have SQLi

Whenever I find XSS vulnerability, I try SQL Injection on same parameter.


4. Bypass HTML security mechanisms

Sometimes special characters are blocked by HTML, so on forms for example, intercept the request and change for your payload.
When we intercept the request, we already bypass the HTML security. 


5. Multiple vulnerabilities

If you find some input that is not sanitized, you can try multiple types of vulnerabilities. Below you find a list of the vulnerabilities 
you should learn in order to exploit weakness in inputs sanitization.
```
**Learn about:** `Types of XSS` `SQL Injection` `HTML Injection` `Server Side Template Injection` 
`Local File Inclusion` `Command Injection`

<br>

<!-- Information Errors -->
## Information Disclosure on Errors 🔡

Errors can give you good information about the plataform, so try to trigger them!
```
1. Stack Trace in Error Message

Try to put special characters in urls and inputs, and observe de strack trace.
If you receive SQL errors, you could try SQLi.

2. Customized Error Messages

Try trigger errors on directories in url. 
Error messages should be customized to not show personal information about the plataform. 
Some errors display Internal IP addresses or technology in use like: Apache/2.2.22 (Linux) PHP/7.0.0-1ubuntu3.4 at 192.168.1.30 Port 80
```

<br>


## Learning Material
In Cybersecurity, we find a community that likes to share its knowledge and it is easy to find a lot of interesting material, below you can find some topics with learning resources and tools.

<!-- ACKNOWLEDGEMENTS -->
## Awesome Resources

* [Gitbook by Pedro Tavares](https://gitbook.seguranca-informatica.pt/)
* [Cobalt Blog](https://cobalt.io/blog)
  
<p>  

<!-- ACKNOWLEDGEMENTS -->
## Awesome Tools

* [Project Discovery](https://github.com/projectdiscovery)
  
<p>  



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.



<!-- CONTACT -->
## Contact

[![Linkedin: bernardo](https://img.shields.io/badge/LinkedIn-Bernardo-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/bernardofsrodrigues/)](https://www.linkedin.com/in/bernardofsrodrigues/)

[![Email: bernardo](https://img.shields.io/badge/Email-Bernardo-blue?style=flat-square&logo=Protonmail&logoColor=white&link=mailto:bernardofsr@protonmail.com)](mailto:bernardofsr@protonmail.com)




<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* []()
* []()
* []()





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/github_username