---
tags:
  - cs151
---
## Strategy Design Pattern

Closed for modification, open for extension
### Design Principle #1
* Identify the aspects of your application that vary and separate them from what stays the same
* Take the parts that vary and [[Pillars of OOP#2 - Encapsulation|encapsulate]] them in a class
	* You can later alter or extend the parts that vary without affecting those that don't.
### Design Principle #2
* …
### Design Principle #3
* Favor composition over inheritance
* The **has a** relationship is interesting
* Creating systems using composition …
## Observer Pattern
* The Subject object manages some important data
* When data in the Subject changes, the observers are notified
* The observers (Observer Objects) have subscribed to (registered with) the Subject to receive updates when the Subject's data changes
* New data values are communicated to the observers in some form when they change
![[observers|500]]
* The observer can subscribe or unsubscribe to the subject
* A one to many dependency between objects
	* When one object changes state
	* all of its dependents are notified/updated automatically
### Design Principle #4
* Strive for loosely coupled designs between objects that interaction
## Singleton Design Pattern
* How to prevent more than one object from being instantiated?
* If we make the constructor private, an instantiation of an object can only be made inside the class