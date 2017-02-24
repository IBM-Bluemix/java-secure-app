# Writing Secure Java Web Applications

## Overview
All web applications must be designed and coded with security in mind to avoid introducing severe security vulnerabilities. This secure starter application helps you write a more secure Liberty Java code right when you start the development. It helps you code to avoid or mitigate most of Cross-Site Scripting (XSS) issues in your application.

## Run the application on Bluemix or locally
Deploy it directly to Bluemix:

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/IBM-Bluemix/java-secure-app)

Or, download this secure starter application, build and deploy it on Bluemix or locally the same way as you do with the [get-started-java sample application](https://github.com/IBM-Bluemix/get-started-java)
```
git clone https://github.com/IBM-Bluemix/java-secure-app
cd java-secure-app
mvn install liberty:run-server
```
View the app at [localhost:9080/GetStartedSecureJava/](http://localhost:9080/GetStartedSecureJava/)

## Background
A security vulnerability can be exploited by various security attacks. An attack may cause stealth of credentials, loss of data and function, disruption of services, and a serious damage to the reputation and revenue of a business. Cross-Site-Scripting is one of the common security vulnerabilities found in most web applications that must be avoided.

Instead of having you to learn first the theory of XSS attacks and remedial techniques before starting to develop a web application, a good secure sample application including the coding examples of key secure coding practices that prevent XSS can help you get started development right away while quickly learn and apply the XSS prevention techniques to protect your application as you write it. This starter application is it.

## How to use it
Use this secure application as a starting point of a new Liberty application development. Learn the XSS countermeasure code in it and apply them to the operations of the application API. The countermeasures will prevent malicious user input to cause damages to your application on the server and the user data on the browser, mitigating the XSS attacks or preventing them altogether.

## Details		 
The [**BadServlet.java**](src/main/java/secure/web/starter/bad/BadServlet.java) is an example insecure code that developers may write if without care. 

The [**GoodServlet.java**](src/main/java/secure/web/starter/good/GoodServlet.java) contains a number of good secure coding practices such as input validation, output encoding, secure Http Header settings, and Content Security Policy. These are key countermeasures against XSS. Applying them can also mitigate other vulnerabilities such as some injection and directory traversal. 

Rrefer to this excellent resource at OWASP on XSS prevention (https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet) to learn more about XSS and its countermeasures. 		

## Code against other security vulnerabilities

In the near future, we intend to incorporate more secure coding examples to mitigate other common security vulnerabilities, such as session hijacking, cross-site request forgery, and SQL/command injection, etc.

## Contribute

We are happy to accept external contributions to this project, be it in the form of suggestions, issues and pull requests. If you find a bug or have a useful secure code to contribute, please report it via the Issues section or fork the project and submit a pull request with your fix or code change! Pull requests will be evaluated on an individual basis based on value add to the sample application.

## Disclaimer

Like other sample applications in github.com/IBM-Bluemix, this is an as-is code serving as an education material with limited support as described in the Contribute section above.
