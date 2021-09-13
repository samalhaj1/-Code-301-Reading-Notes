# CRUD And Status Code
![](https://1.bp.blogspot.com/-k1ORhC6_IsE/XmdOqDVKX6I/AAAAAAAAAB4/3ZOOVJEoU9I4DMYXUtd1fh0efqxV-yY2gCLcBGAsYHQ/s1600/crud.jpg)

## 1. In your own words, describe what each group of status code represents:
* 100’s =everything so far is OK and that the client should continue with the request or ignore it if it is already finished.
* 200’s =the request has succeeded. 
* 300’s =the request has more than one possible responses.
* 400’s =the server cannot or will not process the request due to something that is perceived to be a client error 
* 500’s =Internal Server Error server error response, the server encountered an unexpected condition that prevented it from fulfilling the request. 

## 2. What is a status code 202?
 the request has been accepted for processing, but the processing has not been completed; in fact, processing may not have started yet. 
 
 The request might or might not eventually be acted upon, as it might be disallowed when processing actually takes place.
## 3. What is a status code 308?
the resource requested has been definitively moved to the URL given by the Location headers. 

A browser redirects to this page and search engines update their links to the resource
## 4. What code would you use if an update didn’t return data to a client?
status code 404 
## 5. What code would you use if a resource used to exist but no longer does?
 409 Conflict
The request could not be completed due to a conflict with the current state of the resource
## 6. What is the ‘Forbidden’ status code?
![](https://image.slidesharecdn.com/404-error-160921100722/95/404-error-page-5-638.jpg?cb=1474452859)

**404 Not Found**

The server has not found anything matching the Request-URI. No indication is given of whether the condition is temporary or permanent.

## 7. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
To keep it secret and don't be shown to the user
## 8. What is middleware?
A middleware is basically a function that will the receive the Request and Response objects, just like your route Handlers do. 

As a third argument you have another function which you should call once your middleware code completed
## 9. What does app.use(express.json()) do?
express. json() is a method inbuilt in express to recognize the incoming Request Object as a JSON Object. 

This method is called as a middleware in your application using the code: app.
## 10. What does the /:id mean in a route?
The req. params property is an object containing properties mapped to the named route “parameters”. 

For example, if you have the route /student/:id, then the “id” property is available as req.params.id. This object defaults to {}.
## 11. What is the difference beween PUT and PATCH?
The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource.
## 12. How do you make a defalut value in a schema?
We can specify a default value for an item using the default keyword. 

When a data doesn't have a corresponding value, the value of this keyword will be used instead to do the validation checks. 

This keyword is not mandatory and the value of this keyword can be anything.
## 13. What does a 500 error status code mean?
Internal Server Error server error response, the server encountered an unexpected condition that prevented it from fulfilling the request. 
## 14. What is the difference between a status 200 and a status 201?

The 200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed. 

A 201 status code indicates that a request was successful and as a result, a resource has been created
