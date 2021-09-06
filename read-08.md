## What does REST stand for?


A REST API (also known as RESTful API) is an application programming interface (API or web API) that conforms to the constraints of REST architectural style and allows for interaction with RESTful web services. 

REST stands for representational state transfer and was created by computer scientist Roy Fielding.


## REST APIs are designed around a ____.

When a client request is made via a RESTful API, it transfers a representation of the state of the resource to the requester or endpoint. This information, or representation, is delivered in one of several formats via HTTP: JSON (Javascript Object Notation), HTML, XLT, Python, PHP, or plain text. JSON is the most generally popular file format to use because, despite its name, it’s language-agnostic, as well as readable by both humans and machines. 

Something else to keep in mind: Headers and parameters are also important in the HTTP methods of a RESTful API HTTP request, as they contain important identifier information as to the request's metadata, authorization, uniform resource identifier (URI), caching, cookies, and more. 

There are request headers and response headers, each with their own HTTP connection information and status codes

## What is an identifer of a resource? Give an example.

The target of an HTTP request is called a "resource", whose nature isn't defined further; it can be a document, a photo, or anything else. 

Each resource is identified by a Uniform Resource Identifier (URI) used throughout HTTP for identifying resources.

**Example**

URLs and URNs

URLs

The most common form of URI is the Uniform Resource Locator (URL), which is known as the web address

https://developer.mozilla.org

https://developer.mozilla.org/en-US/docs/Learn/

https://developer.mozilla.org/en-US/search?q=URL

URNs

A Uniform Resource Name (URN) is a URI that identifies a resource by name in a particular namespace.

urn:isbn:9780141036144
urn:ietf:rfc:7230

## What are the most common HTTP verbs?

The primary or most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE. 

These correspond to create, read, update, and delete (or CRUD) operations, respectively. 

There are a number of other verbs, too, but are utilized less frequently.

## What should the URIs be based on?

The universal syntax allows access of objects available using existing protocols, and may be extended with technology.

The specification of the URI syntax does not imply anything about the properties of names and addresses in the various name spaces which are mapped onto the set of URI strings. 

The properties follow from the specifications of the protocols and the associated usage conventions for each scheme.



## Give an example of a good URI.

https://www.w3schools.com/


## What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

Chatty API is one that requires consumer to make tremendous (subjective matter) amount of distinct API calls to get needed information about a resource. 

George Reese has defined chatty API as any API that requires consumer to do more than a single call to perform a single, common operation. 

That sounds possibly a bit too rigid to be followed in real life but a good guideline. Common is context dependant and subjective matter.

**Why chatty API is bad?**

Reason why chatty APIs are considered poor quality is because requiring multiple network calls will slow down an application. 

This is because each call contains data overhead (i.e. sender information, headers, authentication) which will slow down an application as well as network latency per each request.

## What status code does a successful GET request return?

200  or 201- the server successfully returned the page


## What status code does an unsuccessful GET request return?

If not valid, 400 Bad Request is returned. Order is processed.



## What status code does a successful POST request return?

POST: The resource describing the result of the action is transmitted in the message body.

201 Created
200 OK




## What status code does a successful DELETE request return?


A successful response of DELETE requests SHOULD be HTTP response code 200 (OK) if the response includes an entity describing the status, 

202 (Accepted) if the action has been queued, or 204 (No Content) if the action has been performed but the response does not include an entity.





















