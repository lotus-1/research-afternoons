### What is MITM attack
A man in the middle (MITM) attack is a general term for when a perpetrator positions himself in a conversation between a user and an application—either.

The goal of an attack is to steal personal information, such as login credentials, account details and credit card numbers. Targets are typically the users of financial applications, SaaS businesses, e-commerce sites and other websites where logging in is required.

![img](https://www.imperva.com/learn/wp-content/uploads/sites/13/2019/01/man-in-the-middle-mitm.jpg)

#### Man in the middle attack prevention
Blocking MITM attacks requires several practical steps on the part of users

For users, this means:

- Avoiding WiFi connections that aren’t
password protected.

- Paying attention to browser notifications reporting a website as being unsecured.

- Immediately logging out of a secure application when it’s not in use.

- Not using public networks (e.g., coffee shops, hotels) when conducting sensitive transactions.

### What is CSRF
Cross site request forgery (CSRF), also known as XSRF, Sea Surf or Session Riding, is an attack vector that tricks a web browser into executing an unwanted action in an application to which a user is logged in.

A successful CSRF attack can be devastating for both the business and user. It can result in damaged client relationships, unauthorized fund transfers, changed passwords and data theft—including stolen session cookies.

![image](https://www.imperva.com/learn/wp-content/uploads/sites/13/2019/01/csrf-cross-site-request-forgery.png)

#### Using custom rules to prevent CSRF attacks
The highly individual nature of CSRF attacks hinders the development of a one-size-fits-all solution. However, custom security policies can be employed to secure against possible CSRF scenarios.

IncapRules, the Imperva cloud proprietary custom rules engine, lets customers create their own security policies. The policies are generated using an intuitive syntax and can be modified on the fly, augmenting our default web application firewall configuration.

Using IncapRules, you can create a policy that filters requests to sensitive pages and functions based on your HTTP referrer header content. Doing so allows requests to be executed from a short list of secure domains.

This method completely counters the social engineering aspect of CSRF attacks. It prevents execution of malicious requests outside of a security perimeter, regardless of content.

Alternatively, you can run the rule in ‘Alert Only’ mode to track possible exploit attempts, or present CAPTCHAs that alert unwary users.

### What is cross site scripting (XSS)
Cross-site Scripting (XSS) is a client-side code injection attack. The attacker aims to execute malicious scripts in a web browser of the victim by including malicious code in a legitimate web page or web application. The actual attack occurs when the victim visits the web page or web application that executes the malicious code. The web page or web application becomes a vehicle to deliver the malicious script to the user’s browser. Vulnerable vehicles that are commonly used for Cross-site Scripting attacks are forums, message boards, and web pages that allow comments.

#### How to Prevent XSS
To keep yourself safe from XSS, you must sanitize your input. Your application code should never output data received as input directly to the browser without checking it for malicious code.

##### 3 Ways to Keep Cross-Site Scripting Out of Your Apps:
###### 1. Escaping:
by escaping user input. Escaping data means taking the data an application has received and ensuring it’s secure before rendering it for the end user. By escaping user input, key characters in the data received by a web page will be prevented from being interpreted in any malicious way.

###### 2. Validating Input:
Validating input is the process of ensuring an application is rendering the correct data and preventing malicious data from doing harm to the site, database, and users. While whitelisting and input validation are more commonly associated with SQL injection, they can also be used as an additional method of prevention for XSS.

###### 3. Sanitizing:
Sanitizing data is a strong defense, but should not be used alone to battle XSS attacks. It’s totally possible you’ll find the need to use all three methods of prevention in working towards a more secure application. Sanitizing user input is especially helpful on sites that allow HTML markup, to ensure data received can do no harm to users as well as your database by scrubbing the data clean of potentially harmful markup, changing unacceptable user input to an acceptable format.

##### The figure below illustrates a step-by-step walkthrough of a simple XSS attack.


![image](https://www.acunetix.com/wp-content/uploads/2012/10/how-xss-works-1024x454.png)
  
