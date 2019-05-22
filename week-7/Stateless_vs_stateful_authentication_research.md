# Stateless vs stateful authentication

HTTP is what enables communication between a client (frontend) and a server (backend). HTTP is stateless so each request made is totally unaware of any action taken previously. For example we just logged into our twitter account and we navigate to our settings page, with the default HTTP behavior, we would be required to log back in again because the server has no idea that we just logged in but with session and token authentication we can tell the server that we are already logged in and we have should be granted access to that page.  

##  :star2: What is session based authentication (stateful)?  
Session based authentication is one in which the user state is stored on the server’s memory. When using a session based auth system, the server creates and stores the session data in the server memory when the user logs in and then stores the session Id in a cookie on the user browser.
The session Id is then sent on subsequent requests to the server and the server compares it with the stored session data and proceeds to process the requested action.  

##  :star2: What is token based authentication (stateless)?  
Token based authentication is one in which the user state is stored on the client. This has grown to be the preferred mode of authentication for RESTful APIs. In the token based authentication, the user data is encrypted into a JWT (JSON Web Token) with a secret and then sent back to the client.
The JWT is then stored on the client side mostly localStorage and sent as a header for every subsequent request. The server receives and validates the JWT before proceeding to send a response to the client.


## Draw flow diagrams to show the steps involved in each process  

### Session based authentication :

![](https://res.cloudinary.com/practicaldev/image/fetch/s--jzM6Wq6e--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/800/0%2AP5OxJMihg0S0jyqk.png)

### Token based authentication :
![](https://res.cloudinary.com/practicaldev/image/fetch/s--xAjXADfz--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/800/0%2A16xpkdbQ1tuFphvs.png)



## What are the advantages :+1: and disadvantages :-1: of each?  

###  Stateful:  
:+1: ** Advantages **  
1. Revoke the session anytime  
2. Easy to implement and manage for one-session-sever scenario  
3. Session data can be changed later  

:-1: ** Disadvantages **  
1. Increasing server overhead: As the number of logged-in users increases, the more server resources are occupied.  
2. Fail to scale: If the sessions are distributed in different servers, we need to implement a tracking algorithm to link a specific user session and the specific session sever.
3. Difficult for 3rd party applications to use your credentials:  When a 3rd party application enables your users to login their website, the 3rd party application is not able to directly verify your users’ session because they are stored on your backend. The verification must be redirected to the credential servers.


### Stateless:  
:+1: ** Advantages **  
1. Lower server overhead: The great number of session data does not store on the server side. We can store more user properties on the client-side session data to reduce the number of database access without worrying the memory overhead on the server.  
2. Easy to scale: Since the session data is stored on the client side, it does not matter which backend server the request is routed to, as long as all backend servers share the same private key, then all servers have the same capability to verify the validity of the session.  
3. Good to integrate with 3rd party application: In the single sign-on protocols, the 3rd party applications and the IdP must be able to communicate with each other via user agents (browser). During the account linking process between 3rd party applications and IdP, IdP sends a signed message to the browser, and the browser redirects this message to the 3rd party applications. Using a pre-configured shared secrete, the 3rd party applications can determine whether the account linking (single sign-on) is valid by itself.  

:-1:** Disadvantages **  
1. Cannot revoke the session anytime: Since the user session is stored at client side, the server does not have any rights to delete the session.
2. Relatively complex to implement for one-session-server scenario: The advantages of stateless authentication is scalability. However, it increases the technical complexity and it is not extremely useful when we only have one-session-server.
3. Session data cannot be changed until its expiration time: Suppose we want to add “Age” property to a session data, probably we can ask the client to update it, but we cannot make sure the client does update it, since its previously session data is not expired yet, then the client still has the chance to make requests with old session data.   

:rose: Thank you for listening :rose:
