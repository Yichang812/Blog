---
layout: post
title:  "RESTful API, Part II"
date:   2016-02-11 19:31
categories: [Study Notes]
tags: [RESTful API]
---

### HTTP Verbs
The primary HTTP verbs are **POST**, **GET**, **PUT**, and **DELETE**, which correspond to create, read, update and delete (CRUD) operations.
THere are number of other verbs, too. Of those less-frequent methods, **OPTIONS** and **HEAD** are used more often than others.

#### GET

- Used to retrieve (or read) a representation of a resource.
- It returns a representation in XML or JSON and an HTTP response code of 200.
- In error request, it most often returns a 404 (NOT FOUND) or 400 (BAD REQUEST).
- DO NOT expose unsafe operations via GET.

#### PUT

- Used for update.
- It put the newly-updated representation of the original resource to the URI of the resource.
- It can also be used to create a resource, when the resource ID is chosen by client rather than the server.
- It returns 200 or 204(NO CONTENT) when executed successfully. 
- Error: 404 if ID not found or invalid.
- Idempotent but not safe.

#### POST

- Used for creation of new resource.
- In particular, it is used to create subordinate resources.
- Neither idempotent nor safe.
- Error: 404
- PUT vs. POST for Creation

#### DELETE

- Used to delete a resource identified by a URI.
- Error: 404
- Idempotent but not safe

---

_**Idempotence**: describe an operation that will produce the same result when executed multiple times_

_**Safety**: (read only operation) describe an operation that is intended only for information retrieval and not change the state of the server.
Which means the operation should have no side effects (except harmless effects: logging, caching, etc.)_