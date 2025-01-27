<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/bernardofsr">
    <img src="images/logo.png" alt="Logo" width="200" height="200">
  </a>

  <h3 align="center">𝒥𝑜𝓊𝓇𝓃𝑒𝓎 𝑜𝓃 𝒫𝑒𝓃𝓉𝑒𝓈𝓉𝒾𝓃𝑔 𝒲𝑜𝓇𝓁𝒹</h3>

  <p align="center">
    This project is mainly dedicated to people who are <br> starting in Cybersecurity, especially in the area of Penetration Testing.
    <br>
    <br>
    <sub>Project start: 23/04/2021</sub>
    <br/>
    </br>
    <a href="https://github.com/bernardofsr"><strong>Explore the docs »</strong></a>
    <br />
    <a href="mailto:bernardofsr@protonmail.com">Report Bug</a>
    ·
    <a href="mailto:bernardofsr@protonmail.com">Request Feature</a>
  </p>
</p>



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
        <li><a href="#my-toolkit-">My Toolkit</a></li>
      </ul>
    </li>
    <li>
      <a href="#web-application-">Web Application</a>
      <ul>
      <li><a href="#http-status-codes-">HTTP Status Codes</a></li>
      <li><a href="#owasp-top-ten-">OWASP - Top Ten</a></li>
      <li><a href="#lets-testing-">Let's Testing</a></li>
      <ul>
        <li><a href="#authentication-tests-">Authentication Tests</a></li>
        <li><a href="#weak-or-non-existent-sanitization-">Not Sanitized Inputs</a></li>
        <li><a href="#information-disclosure---error-messages-">Information Disclosure - Error Messages</a></li>
        <li><a href="#session-management-">Session Management</a></li>
        <li><a href="#business-logic-">Business Logic</a></li>
        <li><a href="#upload-bypass-">Upload Bypass</a></li>
      </ul>
      <li><a href="#exploiting-common-vulnerabilties-">Exploiting Common Vulnerabilties</a>
      </ul>
    </li>
    <li>
        <a href="#internal-infrastructure-">Infrastructure</a>
    </li>
    <ul>
      <li>
      <a href="#lets-testing-infrastructures-">Let's Testing</a>
      </li>
      <ul>
      <li><a href="#os-credential-dumping---mitre-attck-">OS Credential Dumping - MITRE ATT&CK</li>
      <li><a href="#process-injection---mitre-attck-">Process Injection - MITRE ATT&CK</li>
      </ul>
      </ul>
    <li>
    <a href="#learning-material-">Learning Material</a>
      <ul>
        <li><a href="#awesome-resources-">Awesome Resources</a></li>
        <li><a href="#awesome-tools-">Awesome Tools</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact-">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

##

<!-- About Me -->
## About Me 👨‍💻

I'm Bernardo Rodrigues and I'm currently a Penetration Tester trainee at <a href="https://cipher.com">Cipher</a>. 
<p>From a very early age, I was involved with computers until the taste for hacking was born. Nowadays I practice ethical hacking and I am passionate about offensive cybersecurity, offensive physical security and social engineering. Everything that involves Red Team.</br>
This is my first professional experience as a Penetration Tester and in the area of Cybersecurity.

<!-- ABOUT THE PROJECT -->
## About The Project 🧩

<p>Getting directly into the Cybersecurity without a working background in the area may not be the easiest situation in the world and perhaps the opportunities will not appear so quickly, but nothing is impossible and I hope you will be able to learn a few things from this project. <p>
Penetration Testing is a specific area of cybersecurity and requires knowledge of existing vulnerabilities and how to exploit them. Later on, links will be added to other projects and articles that may be important in learning and that helped me get into the field.

`The Journey` `Cybersecurity` `Pentest` `Hacking` `RedTeam`

<br>

<!-- GETTING STARTED -->
## Getting Started

Since this project is directly designed for people who are entering the area of Penetration Testing, the topics will not be extremely deep and serve only as a basis and guide for learning.

### Prerequisites

1. Computer fundamentals :computer:
2. Desire to learn :books:
3. Coffee :coffee:
<br>

### My Toolkit 👨‍🔧

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
##

<br>


<!-- Web Application -->
## Web Applications 🎯

Web applications are increasingly composed of different types of technologies and it is important to understand a little of each and the different types of vulnerabilities that they can present. 
The amount of knowledge in each technology, in my opinion, comes directly from experience, which is why it is so important to experiment and test in training environments.


<br>

### HTTP Status Codes 🎫

```
1XX - Information
2XX - Successful
3XX - Redirection
4XX - Client Errors
5XX - Server Errors
```

<br>


<br>

### OWASP Top Ten 🔟

```
A1: 2017-Injection
A2: 2017-Broken Authentication
A3: 2017-Sensitive Data Exposure
A4: 2017-XML External Entities (XXE)
A5: 2017-Broken Access Control
A6: 2017-Security Misconfiguration
A7: 2017-Cross-Site Scripting (XSS)
A8: 2017-Insecure Deserialization
A9: 2017-Using Components with Known Vulnerabilities
A10: 2017-Insufficient Logging & Monitoring
```

<br>

<!-- Lets Testing -->
## Let's Testing Web Apps 👨‍🔬

In this topic, I will show you multiple ways to try to find vulnerabilities related to each topic. It's important before you start to test, you understand what each topic is and the importance for the Web Application. For tests, you can try multiple vulnerable machines existent on the web.

<br>

<!-- Authentication Tests-->
### Authentication Tests 🔑

"Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know." - <a href="https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html" target="_blank">OWASP</a>

```
1. Credentials or Important Data sent over HTTP

Intercept authentication-related methods like Login, Account Registration, Password Recovery and 
Password Reset.
Check for important data sent through HTTP.
If the information is being sent over HTTPS, change to HTTP and observe if data are sent.


2. Weak or Non-Existent Anti Brute-Force Mechanism

Create an account (some mechanism can block the account).
Intercept login request and sent a request to the Intruder. 
Use multiple random data and check if you are blocked by any protection mechanism.
Tip: If after test brute-force mechanism doesn't block the account, try to disclose admin or possible 
staff email and try the most common passwords. This way you make tests for Weakness Mechanisms 
and Default Passwords in use.


3. Weak Password Policy

When creating your account for tests, try to set weak passwords like 12345 or admin.


4. Weak Password Change or Reset

Try to add header X-Forwarded-Host of your server and see if you receive the request.
Try X-Forwarded-For and check if after clicking the link you receive the request on your server.


5. Use authentication to enumerate

See what errors are displayed when you try the wrong credentials. If the web application shows something like: 
"The password is incorrect" when you use the correct username, but display the "Wrong Username" error when 
you use the wrong username, you can perform enumeration of registered usernames. Same with emails.
```

<br>

<!-- Not Sanitized Inputs-->
### Weak or Non Existent Sanitization 🧨

An extremely common vulnerability is the lack of sanitization of inputs. When this happens, it is normal to be able to explore XSS or SQL Injection for example.

```
1. Understand how application works

First try to not activate some type of existent WAF with payloads. 
Try what characters are allowed and processed by the Web Application like: / < > ` " '


2. Test with payload

First payload I like to try: "><script>alert("XSS")</script>


3. XSS triggered? Maybe we have SQLi

Whenever I find an XSS vulnerability, I try SQL Injection on the same parameter.


4. Bypass HTML security mechanisms

Sometimes special characters are blocked by HTML, so on forms, for example, intercept the request and change 
for your payload.
When we intercept the request, we already bypass the HTML security. 


5. Multiple vulnerabilities

If you find some input that is not sanitized, you can try multiple types of vulnerabilities. Below you find 
a list of the vulnerabilities you should learn to exploit the weakness in inputs sanitization.
```
**Learn about:** `Types of XSS` `SQL Injection` `HTML Injection` `Server Side Template Injection` 
`Local File Inclusion` `Command Injection`

<br>

<!-- Information Errors -->
### Information Disclosure - Error Messages 🔡

Errors can give you good information about the platform, so try to trigger them!

```
1. Stack Trace in Error Messages

Try to put special characters in URLs and inputs, and observe the stack trace.
If you receive SQL errors, you could try SQLi.


2. Customized Error Messages

Try trigger errors on directories in url. 
Error messages should be customized to not show personal information about the plataform. 
Some errors display Internal IP addresses or technology in use like: Apache/2.2.22 (Linux) PHP/7.0.0-1 
ubuntu3.4 at 192.168.1.30 Port 80
```

<br>

<!-- Session Management -->
### Session Management 🔐

A web session is a sequence of network HTTP request and response transactions associated with the same user. In Web Applications, Session Control is extremely important to protect users. 

```
1. Check Tokens sent over URL

If the Tokens are going over requests with the GET method and you can see it on the URL, that may be a 
problem for user's privacy and security.
Use Burp to view all requests and check if Tokens are on the URL. 


2. Session keep up after logout

Login on your account, intercept some action with Burp, and sent it to Repeater.
Logout from the account on Web Application, go to Repeater, and sent the request. If the request is sent with 
no errors, the application has a problem with Session Logout.


3. Password reset link doesn't expire

Request password recovery to your email. Use the link to the recovery password and save the new password.
Go to email and try to use the same link again. If you can reuse the link, the Web Application is not 
expiring Reset Password Tokens.

[topic in production]
```
<br>

<!-- Business Logic -->
### Business Logic 👔

The vulnerabilities of business logic, are all those that go against the normal workflow that a company would have in the process of a certain action.

```
1. Negative numbers

When the Web Application uses transaction or shop carts for example, try to use negative numbers. Using burp, 
intercept and change the integer to a negative number and see the response.  

[topic in production]

```
<br>

<!-- Upload Bypass -->
### Upload Bypass 📤

Is an attempt to bypass the security mechanisms related to the file upload functionality. It can be in the type of file (file extension) or in its maximum size.

```
1. Try upload a large file

If the application allows you to upload a large file in a section where a small file was expected, this can 
lead to a DoS in the application. For example, the application expects a PDF file and allows you to upload a
file that is 1GB in size.


2. Try bypass the allowed files extension

Upload a file with a different extension and try to change it on burp suite.
Imagine that the application only allows you to upload a PNG file. Create a shell in PHP and rename it to 
"shell.php.png" and intercept the upload request in the burp. Change the file name to "shell.php" in the 
request and forward to the request.
For these types of situations, it is important to understand which directory the files are sent to, and 
whether we have access to them.
```

<br>

<!-- Exploiting -->
### Exploiting Common Vulnerabilties 🐞


<br>

<p align="center">
  <a href="https://github.com/bernardofsr">
    <img src="images/uc.jpg" alt="Logo" width="430" height="200">
  </a>

#

<br>

<!-- Infrastructure -->
## Internal Infrastructure 🏢

Internal Infrastructure Pentesting can include the pentesting for internal networks, internal services, associated external devices and employees (social engineering).
Nowadays, probably the most used technology in an internal network is Active Directory, and that will be one of the focuses of this topic.

<br>

### Let's Testing Infrastructures 👨‍🔬

<br>

<p align="center">
  <a href="https://github.com/bernardofsr">
    <img src="images/uc.jpg" alt="Logo" width="430" height="200">
  </a>


<br>
<br>


### OS Credential Dumping - MITRE ATT&CK 🎣


Notes from "MITRE ATT&CK - OS Credential Dumping" by Picus Security.
<br>
<br>

**LSASS** - Local Security Authority Subsystem Service

```
This service is responsible for storing the credentials of users logged into memory.
Stores reversibly encrypted plain text, Kerberos tickets, and LM and NT hashes.
Local Administrador or System is required to interact with "lsass.exe" process.
```
```
Tools used to dump credentials from Lsass:
1. Mimikatz
2. Gsecdump
3. ProcDump
```
<br>

**SAM** - Security Account Manager
```
The SAM file is located at "%systemroot%\system32\config\SAM", and contains usernames and hashed passwords 
for local accounts.
Stores Lan Manager (LM) or NT Lan Manager (NTLM/NTHash) hashes of the users passwords.
Nowadays, NTLM are the types of hashes used in the most recent systems.
```
```
Dumping techniques:
- Registry: reg.exe can be used to copy HKLM/SAM and HKLM/SECURITY file.
- In-memory: injecting DLL into the LASS system process.
- Volume Shadow Copy: Copy of the SAM file from the shadow copy instance.
```

<br>

**NTDS** - NT Directory Services
```
NTDS.dit is the file related to Active Directory, which serves as a database and stores the AD data.
Contains: Information about user objects, groups, and group membership. Also contains the password hashes for 
all user in the domain.
```
<br>

**LSA** - Local Security Auhtority
```
Stores sensitive user and system information, allowing applications to run with proper privileges.
This include services accounts credentials, VPN's, and auto-logins.
```
```
LSA secrets can be dumped using Mimikatz: lsadump::secrets
```
<br>

### Red Team Examples
Some methods for dump credentials using native operating system files.

<br>

#### Copy SAM file from shadows

1. Create shadow copy: 
`wmic shadowcopy call create Volume=C:\`

1. Enumerate shadows and the path of shadows:
`vssadmin List Shadows`

1. Copy SAM file from shadow: 
`copy $PathToShadow\Windows\System32\config\SAM C:\temp`

1. Extract hashes from SAM file:
   `samdump2 system sam`
 
<br>

##### From Registry
1. Extracting SAM from registry:
   `reg.exe save hklm\sam c:\temp\sam.save`
#


### Process Injection - MITRE ATT&CK 💉

Notes from "MITRE ATT&CK - OS Credential Dumping" by Picus Security.
<br>

**Process Injection** consists in inject malicious code into applications or processes that are usually trusted by the user.

```
Running arbitrary code
Enabling access to the target process:
 1. memory
 2. system
 3. network resources
```
<br>

**Most common** injected processes:

Windows native processes: `explorer.exe` `svchost.exe` `dllhost.exe` `services.exe` `rundll32.exe` `csc.exe` `cmd.exe`

Processes common software: `iexplorer.exe` `opera.exe` `chrome.exe` `outlook.exe` `firefox.exe` `ieuser.exe`

<br>


## Learning Material 👨‍🎓
In Cybersecurity, we find a community that likes to share its knowledge and it is easy to find a lot of interesting material, below you can find some topics with learning resources and tools.

<!-- ACKNOWLEDGEMENTS -->
### Awesome Resources 📚

* [Gitbook by Pedro Tavares](https://gitbook.seguranca-informatica.pt/)
* [Cobalt Blog](https://cobalt.io/blog)
* [PortSwigger](https://portswigger.net/blog)
* [PTSwarm](https://swarm.ptsecurity.com/)
* [David Alves Channel](https://www.youtube.com/channel/UCX2ADIIC5GYNERNSxSerKow)
  
<p>  

<!-- ACKNOWLEDGEMENTS -->
### Awesome Tools 🔨

* [Project Discovery](https://github.com/projectdiscovery)
* [FeroxBuster](https://github.com/epi052/feroxbuster)
* [SQLMap](https://github.com/sqlmapproject/sqlmap)
  
<p>  



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.



<!-- CONTACT -->
## Contact 📬

[![Linkedin: bernardo](https://img.shields.io/badge/LinkedIn-Bernardo-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/bernardofsrodrigues/)](https://www.linkedin.com/in/bernardofsrodrigues/)

[![Email: bernardo](https://img.shields.io/badge/Email-Bernardo-blue?style=flat-square&logo=Protonmail&logoColor=white&link=mailto:bernardofsr@protonmail.com)](mailto:bernardofsr@protonmail.com)




<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* []()
* []()
* []()


