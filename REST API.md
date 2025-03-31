# REST API

## REST APIs Should Use Uniform Resource Identifiers (URI)

No Verbs in URI!

## REST API Should return Contents of the URI

I’m of the opinion all requests that use the same URI should return the same data. Consider the following:

### But what if I Create an Item with it’s Unique URI?

That’s a PUT or a PATCH, not a POST!

## Hypertext As The Engine Of Application State

[[Hateoas]] states your state should be baked into the markup of your requests and responses. This means the actions you can take on entities should be returned within the response of the previous request. As a guide, The  URI for the subsequent request taken should be within the response of the current request.
