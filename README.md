# user-authentication-demo

NOTE: This demo serves as a tutorial for how user authentication plays a key role in 
many software security applications. This code is NOT intended to serve as any measure 
of software security. 

In this particular demo, we look at a simple login screen that contains security 
vulnerabilities. A user is able to input a username or email address followed by 
an associated account password. The first design flaw starts by indicating to the 
user whether or not that username/email address exists within this system. With 
this major weakness, we can that perform a range of attacks to identify an existing 
username/email. In this case, we will look at dictonary attacks (brute force) to 
compile a list of existing email addresses. This is type of attack is made much 
easier by applying the attack ONLY on the local-part of an email address and then, 
using only a handfull of domains from common online mail services (gmail, yahoo, 
hotmail, aol, etc...).

local-part@domain	(email address)

The ability to reset an account password is a very common feature offered by many 
modern-day software applications. This can also be an area where security vulnerabilities 
exist with damaging consequences for a large system that has a high volume of active 
users. Taking the information from our intial attack, we can then perform ....

the first key piece of information (username/email) we are then, able to utilize this information in the 
"forgot my password" feature. All that is 