AirBnB Clone - The ALX-Holberton BnB
hbnb

Description of the project
The ALX-Holberton B&B sums up the implementation of my four months of studies at the ALX-Holberton School - the fullstack software engineering program. The goal of the project is to deploy a replica of the Airbnb Website using my server. The final version of this project will have:

1. A command interpreter to manipulate data without a visual interface, like a shell (for development and debugging)
2. A website (front-end) with static and dynamic functionalities
3. A comprehensive database to manage the backend functionalities
4. An API that provides a communication interface between the front and backend of the system.
5. General concepts in review

As you navigate this code base, it is great to note the following concepts, while completing this project;
How to create a Python package
How to create a command interpreter in Python using the cmd module
What is Unit testing and how to implement it in a large project
How to serialize and deserialize a Class
How to write and read a JSON file
How to manage datetime
What is an UUID
What is *args and how to use it
What is **kwargs and how to use it
How to handle named arguments in a function
Environment 💻
The console was developed in Ubuntu 14.04LTS using python3 (version 3.4.3).

Further information 📑
For further information on python version, and documentation visit python.org.

Requirements 📝
Knowledge in python3, how to use a command line interpreter, a computer with Ubuntu 14.04, python3 and pep8 style corrector.

Repo Contents 📋
This repository constains the following files:

File	Description
AUTHORS	Contains info about authors of the project
base_model.py	Defines BaseModel class (parent class), and methods
user.py	Defines subclass User
amenity.py	Defines subclass Amenity
city.py	Defines subclass City
place.py	Defines subclass Place
review.py	Defines subclass Review
state.py	Defines subclass State
file_storage.py	Creates new instance of class, serializes and deserializes data
console.py	creates object, retrieves object from file, does operations on objects, updates attributes of object and destroys object
test_base_model.py	unittests for base_model
test_user.py	unittests for user
test_amenity.py	unittests for amenity
test_city.py	unittests for city
test_place.py	unittests for place
test_review.py	unittests for review
test_state.py	unittests for state
test_file_storage.py	unittests for file_storage
test_console.py	unittests for console
Installation 🛠️
Clone the repository and run the console.py

$ git clone https://github.com/------/AirBnB_clone.git
Usage 🔧
Method	Description
create	Creates object of given class
show	Prints the string representation of an instance based on the class name and id
all	Prints all string representation of all instances based or not on the class name
update	Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file)
destroy	Deletes an instance based on the class name and id (save the change into the JSON file)
count	Retrieve the number of instances of a class
help	Prints information about specific command
quit/ EOF	Exit the program
0x00. AirBnB clone - The console
0x00.Table of contents
0x01 Introduction
0x02 Environment
0x03 Installation
0x04 Testing
0x05 Usage
0x06 Authors
0x01 Introduction
Team project to build a clone of AirBnB.

The console is a command interpreter to manage objects abstraction between objects and how they are stored.

To see the fundamental background of the project visit the Wiki.

The console will perform the following tasks:

create a new object
retrive an object from a file
do operations on objects
destroy an object
Storage
All the classes are handled by the Storage engine in the FileStorage Class.

0x02 Environment
Suite CRM terminal python Suite CRM Suite CRM git distributed version control system Github

Style guidelines:
pycodestyle (version 2.7.*)
PEP8
All the development and testing was runned over an operating system Ubuntu 20.04 LTS using programming language Python 3.8.3. The editors used were VIM 8.1.2269, VSCode 1.6.1 and Atom 1.58.0 . Control version using Git 2.25.1.

0x03 Installation
git clone https://github.com/Eloagbawe/AirBnB_clone.git
change to the AirBnb directory and run the command:

 ./console.py
Execution
In interactive mode

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
$
in Non-interactive mode

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
0x04 Testing
All the test are defined in the tests folder.

Documentation
Modules:
python3 -c 'print(__import__("my_module").__doc__)'
Classes:
python3 -c 'print(__import__("my_module").MyClass.__doc__)'
Functions (inside and outside a class):
python3 -c 'print(__import__("my_module").my_function.__doc__)'
and

python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'
Python Unit Tests
unittest module
File extension .py
Files and folders star with test_
Organization:for models/base.py, unit tests in: tests/test_models/test_base.py
Execution command: python3 -m unittest discover tests
or: python3 -m unittest tests/test_models/test_base.py
run test in interactive mode
echo "python3 -m unittest discover tests" | bash
run test in non-interactive mode
To run the tests in non-interactive mode, and discover all the test, you can use the command:

python3 -m unittest discover tests
0x05 Usage
Start the console in interactive mode:
$ ./console.py
(hbnb)
Use help to see the available commands:
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb)
Quit the console:
(hbnb) quit
$

Commands
The commands are displayed in the following format Command / usage / example with output

Create
Creates a new instance of a given class. The class' ID is printed and the instance is saved to the file file.json.

create <class>
(hbnb) create BaseModel
6cfb47c4-a434-4da7-ac03-2122624c3762
(hbnb)
Show
show <class> <id>

Destroy
Deletes an instance of a given class with a given ID. > Update the file.json

(hbnb) create User
0c98d2b8-7ffa-42b7-8009-d9d54b69a472
(hbnb) destroy User 0c98d2b8-7ffa-42b7-8009-d9d54b69a472
(hbnb) show User 0c98d2b8-7ffa-42b7-8009-d9d54b69a472
** no instance found **
(hbnb)

all
Prints all string representation of all instances of a given class. > If no class is passed, all classes are printed.

(hbnb) create BaseModel
e45ddda9-eb80-4858-99a9-226d4f08a629
(hbnb) all BaseModel

count
Prints the number of instances of a given class.

(hbnb) create City
4e01c33e-2564-42c2-b61c-17e512898bad
(hbnb) create City
e952b772-80a5-41e9-b728-6bc4dc5c21b4
(hbnb) count City
2
(hbnb)


update
Updates an instance based on the class name, id, and kwargs passed. > Update the file.json

(hbnb) create User
1afa163d-486e-467a-8d38-3040afeaa1a1
(hbnb) update User 1afa163d-486e-467a-8d38-3040afeaa1a1 email "aysuarex@gmail.com"
(hbnb) show User 1afa163d-486e-467a-8d38-3040afeaa1a1

Author
agboola Olalekan Samson
