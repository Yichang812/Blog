---
layout: post
title:  "RESTful API, Part I"
date:   2016-02-09 01:58
categories: [Study Notes]
tags: [RESTful]
---

### Introduction
REST stands for REpresentational State Transfer. It typically, but not always, communicates through HTTP (HyperText Transfer Protocol).
Instead of a set of standards, it is more like an architectural style, which is affected by 6 constraints.

 - Client-Server
 - Uniform Interface
 - Stateless
 - Cacheable
 - Layered System
 - Code on Demand _(optional)_
 
#### **Client-Server**
The uniform interface seperates clients from the servers.

#### **Uniform Interface**
4 guiding principles:

 - Resource-Based (URI)
 - Manipulation of Resources Through Representations (HTTP verbs)
 - Self-descriptive Messages (HTTP: Content-Type)
 - Hypermedia as the Engine of Application States 

#### **Stateless**
Stateless is the key. It means during the client-server communication, no client context is stored on the server between requests.
Each request from any client contains all the necessary information fro the server to fulfill the request.

Stateless enables greater scalability, since the server does not have to maintain, update or communicate that session state.

If a design expects you to do things in order, it violate the statelessness principle.

#### **Cacheable**
It means clients can cache response. Therefore, responses must implicityly or explicitly define themselves as cacheable or not.
Well-managed caching partially or completely eliminates some client-server interactions, further improving scalability and performance.

#### **Layered System**
A client should not tell if it is connected directly to the end server, or to an intermediary. 

Intermediary servers may improve system scalability by enabling load-balancing and by providing shared caches. Layers may also enforce security policies.

---

### Tips

#### **Use HTTP Verbs to Mean Something**

**GET**: retrieve;  **POST**: replace;  **PUT**: create;  **DELETE**: delete;

|                          |GET   |POST  |
|-------------------------:|:------:|:------:|
|cached                    | yes    | no     |
|remain in browser history | yes    | no     |
|length restriction        | yes    | no     |
|data type restriction     | ASCII  | no     |
|visibility                |displayed in the URL|not in the URL|


#### **Sensible Resource Names**

Having sensible resource names or paths (e.g., /posts/23 instead of /api?type=posts&id=23).

Resource name should be nouns, avoid verbs as resource names.

#### **Create Fine-Grained Resources**

Start with small, easily defined resources, providing CRUD functionality on those. It is easier to create larger 
resources later from individual resources.


---

### Resources:

- [API design cheatsheet](https://github.com/RestCheatSheet/api-cheat-sheet#api-design-cheat-sheet)
- [Platform building cheatsheet](https://github.com/RestCheatSheet/platform-cheat-sheet#platform-building-cheat-sheet)

---

### Reference 
- _The notes were summarized based on **RESTful Service Best Practices** 
- http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm_