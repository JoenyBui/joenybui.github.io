---
layout: post
author: Joeny Bui
---

# Singleton Design Pattern

Restricts the instantiation of a class to one "single" instance.  This is useful when exactly one object is needed to coordinate actions across the system.

* used for centralized management of internal or external resources 
* provide a global point of access to themselves
* implementation involves a static member in the class and a private constructor
* ensure it works in multi-threaded environment

## Examples

* logger classes - provides a global logging access point in the application component
* configuration classes - design the classes which provide the configuration settings
* accessing resources in shared mode - accessing from multiple classes on a serial port (singleton allows synchronization)
* factories implementation as a singleton
