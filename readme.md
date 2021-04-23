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
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

##

<!-- About Me -->
## About Me 

I'm Bernardo Rodrigues and I'm currently a Penetration Tester trainee at <a href="https://cipher.com">Cipher</a>. 



<!-- ABOUT THE PROJECT -->
## About The Project

<p>Getting directly into the Cybersecurity without a working background in the area may not be the easiest situation in the world and perhaps the opportunities will not appear so quickly, but nothing is impossible and I hope you will be able to learn a few things from this project. <p>
Penetration testing is a specific area of cybersecurity and requires knowledge of existing vulnerabilities and how to exploit them. Later on, links will be added to other projects and articles that may be important in learning and that helped me get into the field.

`The Journey`, `Cybersecurity`, `Pentest`, `Hacking`, `RedTeam`

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

"Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know." - OWASP

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
## Not Sanitized Inputs 🧨

An extremely common vulnerability is the lack of sanitization of inputs. When this happens, it is normal to be able to explore XSS or SQL Injection for example.

```
1. First try to not activate some type of existent WAF with payloads. 
Try what characters are allowed and processed by the Web Application like: / < > ` " '

2. First payload I like to try: "><script>alert("XSS")</script>

3. Whenever I find XSS vulnerability, I try SQL Injection on same parameter.

4. Sometimes special characters are blocked by HTML, so on forms for example, intercept the request and change for your payload.
When we intercept the request, we already bypass the HTML security. 
```

<br>

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