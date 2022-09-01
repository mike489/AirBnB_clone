![hbnb](https://user-images.githubusercontent.com/88311316/151070609-19608294-829e-408b-b2b3-5d1f2873f1e3.png "hbnb")

# Project Description
**First step: Write a command interpreter to manage your AirBnB objects.**
---
This is the first step towards building your first full web application: the **AirBnB clone**. This first step is very important because you will use what you build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help you to:

put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances
create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
create all classes used for AirBnB (User, State, City, Place…) that inherit from BaseModel
create the first abstracted storage engine of the project: File storage.
create all unittests to validate all our classes and storage engine

The goal of the project is to deploy a replica of the Airbnb Website using my server. The final version of this project will have:
1. A command interpreter to manipulate data without a visual interface, like a shell (for development and debugging)
1. A website (front-end) with static and dynamic functionalities
1. A comprehensive database to manage the backend functionalities
1. An API that provides a communication interface between the front and backend of the system.
1. General concepts in review

## What’s a command interpreter?
Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

Create a new object (ex: a new User or a new Place)
Retrieve an object from a file, a database etc…
Do operations on objects (count, compute stats, etc…)
Update attributes of an object
Destroy an object

## Execution
Your shell should work like this in interactive mode:
```shell
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
$
```
But also in non-interactive mode: (like the Shell project in C)

```shell
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```
All tests should also pass in non-interactive mode: $ echo "python3 -m unittest discover tests" | bash

# Project Contents
This repository constains the following files:

|File|	Description|
|:---|:------------|
|AUTHORS|	Contains info about authors of the project|
|base_model.py|	Defines BaseModel class (parent class), and methods|
|user.py|	Defines subclass User|
|amenity.py|	Defines subclass Amenity|
|city.py|	Defines subclass City|
|place.py|	Defines subclass Place|
|review.py|	Defines subclass Review|
|state.py|	Defines subclass State|
|file_storage.py|	Creates new instance of class, serializes and deserializes data|
|console.py|	creates object, retrieves object from file, does operations on objects, updates attributes of object and destroys object|
|test_base_model.py|	unittests for base_model|
|test_user.py|	unittests for user|
|test_amenity.py| unittests for amenity|
|test_city.py|	unittests for city|
|test_place.py|	unittests for place|
|test_review.py|	unittests for review|
|test_state.py|	unittests for state|
|test_file_storage.py|	unittests for file_storage|
|test_console.py|	unittests for console|

# Installation 
Clone the repository and run the console.py

> $ git clone https://github.com/mike489/AirBnB_clone.git
## Usage 
|Method|	Description|
|:-----:|:------------------:|
|create|	Creates object of given class|
|show|	Prints the string representation of an instance based on the class name and id|
|all|	Prints all string representation of all instances based or not on the class name|
|update|	Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file)|
|destroy|	Deletes an instance based on the class name and id (save the change into the JSON file)|
|count|	Retrieve the number of instances of a class|
|help|	Prints information about specific command|
|quit/ EOF|	Exit the program|
