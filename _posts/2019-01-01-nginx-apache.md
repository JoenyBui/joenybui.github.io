---
layout: post
author: Joeny Bui
---

# Nginx vs Apache

## Nginx

![](https://anturis.com/blog/nginx-vs-apache/nginx-how-it-works.png)

Nginx is an open source alternative *event-based* web server (select/event based model liekd Zeus).  It was written to address the C10K problem - where one web server can handle 10,000 connections.  (Speed)

Nginx does not create new processes for each web requests, instead the administrator configures how many worker prcoesses to create.  Each of these process is single-threaded.  

Nginx also spins off cache loader and cache manager processess to read data from disk and load it into the cache.

Pros:
- "event" means a user connection
- "asynchronous" means that it handles user interaction for more than one user connections at a time
- "non-blocking" means it does not stop disk I/O because the CPU is busy
- advanced load balancing
- caching
- proxy server

## Apache Tomcat

Apache has been around and it's the more popular configuration. (Power)

HOW IT WORKS
Apache creates processes and threads to handle additional connections. (Admin controls the maximum number of allowable processes - depends on machine memory).  Too many processes will swap memory to disk, severly downgrading performance.

Pre-forked => One thread per process
Worker-mode => One process multiple thread (not thread safe)

Limiting factor in tuning Apache is memory and the potential to dead-locked threads that are contending for the same CPU and memory.

PROS
* Apache web server can be use to serve up static web page
* Apache tomcat with mod_jk module to run Java and JSP

CONS
* Apache slows down under heavy load - because of the need to spawn new processes, thus consuming more computer memory
* It also creates new threads the compete to access memory and CPU
* It will refuse new connections when traffic reaches the limit of process configured