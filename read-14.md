# OAuth
![](https://www.royalcyber.com/blog/wp-content/uploads/2017/09/Rest-OAuth-2.0-Client-Specifications-img.jpg)

## 1. What is OAuth?

OAuth is an authorization framework that enables an application or service to obtain limited access to a protected HTTP resource. 

To use REST APIs with OAuth in Oracle Integration, you need to register your Oracle Integration instance as a trusted application in Oracle Identity Cloud Service.

## 2. Give an example of what using OAuth would look like.

The simplest example of OAuth in action is one website saying “hey, do you want to log into our website with other website's login?” In this scenario, 

the only thing the first website – let's refer to that website as the consumer – wants to know is that the user is the same user on both websites and has logged in
## 3. How does OAuth work? What are the steps that it takes to authenticate the user?

* In a command window, change to the project folder that you created in the tutorial Tutorial: Creating an invoke REST API definition.
* In the API Designer, click the APIs tab.
* Click Add > OAuth 2.0 Provider API.
* Complete the fields according to the following table: ...
* Click Create API.
## 4. What is OpenID?
![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/OpenID_logo_2.svg/1200px-OpenID_logo_2.svg.png)
OpenID Connect (OIDC) is an open authentication protocol that profiles and extends OAuth 2.0 to add an identity layer. 

OIDC allows clients to confirm an end user's identity using authentication by an authorization server.
# Authorization and Authentication flows

## 5. What is the difference between authorization and authentication?
authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to. 
## 6. What is Authorization Code Flow?
Authorization code flow is used to obtain an access token to authorize API requests. ... Access tokens while having a limited lifetime, can be renewed with a refresh token. 

A refresh token is valid indefinitely and provides ability for your application to schedule tasks on behalf of a user without their interaction.
## 7. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
The Authorization Code Flow + PKCE is an OpenId Connect flow specifically designed to authenticate native or mobile application users. 

This flow is considered best practice when using Single Page Apps (SPA) or Mobile Apps. PKCE, pronounced “pixy” is an acronym for Proof Key for Code Exchange.
## 8. What is Implicit Flow with Form Post?
Implicit Flow with Form Post flow uses OIDC to implement web sign-in that is very similar to the way SAML and WS-Federation operates. 

The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls.
## 9. What is Client Credentials Flow?
The Client Credentials flow is a server to server flow. There is no user authentication involved in the process. ... This flow is useful for systems that need to perform API operations when no user is present. 

It can be nightly operations, or other that involve contacting OAuth protected APIs.
## 10. What is Device Authorization Flow?
The authorization flow defined by this specification, sometimes referred to as the "device flow", instructs the user to review the authorization request on a secondary device, 

such as a smartphone, which does have the requisite input and browser capabilities to complete the user interaction.
## 11. What is Resource Owner Password Flow?

The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, a refresh token. 

The primary difference is that the user's password is accessible to the application. ...








