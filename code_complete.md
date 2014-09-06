# Code Complete

## ch2

* software development is, as a metaphor, similar to building a construction
  * careful preparation
  * difference between large and small projects
* tools are like a builder toolbox
  * there are many
  * choose the right one

## ch3

* emphasize on construction practices from the beginning
* a good project planner clears all major risks as early as possible
	* poor requirements and poor project planning are the biggest risks in software development
* architect components
	* program organization - broad terms about the app
	* major classes - strive for 20% of classes do 80% of job
	* data design - tables
	* business rules - information should not be stale for more then 30 secs
	* UI design - command line can be plugged in a GUI
	* resource management - IO, memory, threads
	* security
	* performance
	* scalability, interoperability
	* i18n, l10n
	* error processing, fault tolerance
	* buy components, reuse
	* design for possible change


## ch4 key construction decisions

* programmers are about 30% more productive in a programming language in which they have experience
* every programming language has strengths and weaknesses

## ch5 - design in construction

* design is a problem that you know the solution after you solved the problem
* projects fail technically because of uncontrolled complexity
* **managing complexity** is the most important technical topic in software dev
* design characteristics
	* minimal complexity - simple and easy to understand
	* ease of maintenance - design it for the maintenance programmer
	* minimal connectedness - loose coupling
	* extensibility
	* reusability
* common subsystems
	* business logic
	* UI
	* database access
	* system/platform dependencies
* design heuristics
	* find real-world objects
	* form consistent abstractions
	* encapsulate implementation details
	* inheritance can simplify the design
	* hide information complexity - get into the habit of asking what should I hide
	* identify areas that will change - great designers do that
	* loosely coupled criterias
	   * size - number of arguments, number of public methods
	   * flexibility - don’t make a method take an object if it only needs 2 properties
	* design patterns
	* design for test
* design practices
	* iterate
	* divide and conquer = no one’s skull is big enough to contain all the details of a complex program

## ch6 - classes

* good encapsulation
	* favor read-time convenience to write-time convenience
	* tight coupling occurs when an abstraction is leaky or when encapsulation is broken
* class interfaces should hide something
* containment (has a relationships) - 7±2 data members
* inheritance - subclasses must be usable through the base class interface w/out the need for the user to know the difference
* be suspicious of classes of which there is only one instance - maybe you could instantiate it and attribute the data
* do not design ahead a base class
* limit inheritance to 7±2
* use mixins for Displayable, Persistant, Serializable or Sortable
* rules
	* multiple classes share common data but not behavior, then create a common object that those classes can contain
	* multiple classes do not share common data but behavior, then derive from a common base class
	* if data and behavior, then inherit
* account.ContactPerson().DaytimeContactInfo() is not ok, because Object A calls a routine from Object B
* prefer deep object copies - they are safer and easily maintainable
* reasons to create classes
	* model real-world objects (Circle)
	* model abstract objects (Shape)
	* reduce and isolate complexity
	* hide implementation details
	* hide global data behind an object
	* streamline parameter passing
	* make central points of control
	* facilitate reusable core
	* package related operations
* classes to avoid
	* avoid creating a god class that spends time retrieving data from other classes
	* eliminate irrelevant classes - if a class does not have behavior, move the properties to another class
	* avoid classes with names after like StringBuilder - transform them to methods


## ch7 - routines

* reasons to create a routine
	* reduce complexity
	* make a section of code readable
	* avoid duplicate code
* design for routines - **cohesion** - how closely the operations in a routine are related
* the name of a routine is an indication of quality


