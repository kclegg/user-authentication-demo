# user-authentication-demo

NOTE: This demo serves as a tutorial for how user authentication plays a key role in 
many software security applications. This code is NOT intended to serve as any measure 
of software security. This demo is inspired by challenges found from the security 
shepherd project.

In this particular demo, we look at a simple login screen that contains security 
vulnerabilities. A user is able to input a username or email address followed by 
an associated account password. The first design flaw starts by indicating to the 
user whether or not that username/email address exists within this system. With 
this major weakness, we can that perform a range of attacks to identify an existing 
username/email. One method that could be applied would be dictonary attacks (brute force) 
to compile a list of existing email addresses. This is type of attack is made much 
easier by applying the attack ONLY on the local-part of an email address and then, 
using only a handfull of domains from common online mail services (gmail, yahoo, 
hotmail, aol, etc...).

local-part@domain	(email address)

The ability to reset an account password is a very common feature offered by many 
modern-day software applications. This can also be an area where security vulnerabilities 
exist with damaging consequences for a large system, particularly those that have a 
high volume of active users. Now looking at the "forgot my password" option, we are now able 
to exploit this feature. Taking the information from our intial attack, we can perform 
different types of attacks by either manipualting POST request the form submits, SQL Injection, 
or some form of brute form on the input field. In this demo we will look at sql injection to
answering a security question for logging in.

SELECT securityAnswer FROM 'login' WHERE securityAnswer=' fluffy' OR '1=1 ';

Key Takeaways:

* Reveal as little info to the user as possible.
* Limit number of attempts to enter security field questions.
* Have secure code to prevent HTTP request manipulation, SQL Injection,
or spamming of HTTP requests (brute form).