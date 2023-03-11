
0x00. AirBnB clone - The console
0x00. AirBnB clone - Table of contents

* https://github.com/Perkunz/AirBnB_clone#0x01-Introduction
* https://github.com/Perkunz/AirBnB_clone#0x02-Environment
* https://github.com/Perkunz/AirBnB_clone#0x02-Installation
* https://github.com/Perkunz/AirBnB_clone#0x02-Testing
* https://github.com/Perkunz/AirBnB_clone#0x02-Usage
* https://github.com/Perkunz/AirBnB_clone#0x02-Authors

0x01 Introduction
Team project to build a clone of AirBnB.

The console is a command interpreter to manage objects abstraction between objects and how they are stored.

To see the fundamental background of the project visit the Wiki.

The console willl perform the following tasks:

create a new object
retrive an object from a file
do operations on objects such as updating the content
destroy an object(i.e delete)
Storage
All the classes are handled by the Storage engine in the FileStorage Class.

0x02 Environment
Suite CRM terminal python Suite CRM Suite CRM git distributed version control system Github

Style guidelines:
pycodestyle (version 2.8.0)
PEP8
All the development and testing was runned over an operating system Ubuntu 20.04 LTS using programming language Python 3.8.3. The editors used were VIM 8.1.2269, VSCode 1.6.1 and Atom 1.58.0 . Control version using Git 2.25.1.

0x03 Installation
git clone https://github.com/uniqueel/AirBnB_clone.git
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
Use help to see the available commands present in the console:
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
6cc437c1-a213-4da7-ac03-8904c61035
(hbnb)
Show
show <class> <id>
(hbnb) show BaseModel 6cc437c1-a213-4da7-ac03-8904c61035
[BaseModel] (a) [BaseModel] (6cc437c1-a213-4da7-ac03-8904c61035) {'id': '6cc437c1-a213-4da7-ac03-8904c61035', 'created_at': datetime.datetime(2022, 11, 24, 1, 56, 30, 826045), 'updated_at': datetime.datetime(2022, 11, 24, 53, 68, 21, 805349)}
(hbnb)
Destroy
Deletes an instance of a given class with a given ID. Update the file.json

(hbnb) create User
0c98d2b8-7ffa-42b7-8009-d9d54b69a472
(hbnb) destroy User 0c98d2b8-7ffa-42b7-8009-d9d54b69a472
(hbnb) show User 0c98d2b8-7ffa-42b7-8009-d9d54b69a472
** no instance found **
(hbnb)
all
Prints all string representation of all instances of a given class. If no class is passed, all classes are printed.

(hbnb) create BaseModel
e45ddda9-eb80-4858-99a9-226d4f08a629
(hbnb) all BaseModel
["[BaseModel] (4c8f7ebc-257f-4ed1-b26b-e7aace459897) [BaseModel] (4c8f7ebc-257f-4ed1-b26b-e7aace459897) {'id': '4c8f7ebc-257f-4ed1-b26b-e7aace459897', 'created_at': datetime.datetime(2022, 11,24 , 11, 19, 19, 447155), 'updated_at': datetime.datetime(2022, 11, 24, 22, 19, 19, 447257), 'name': 'My First Trial', 'my_number': 77}"]
["[BaseMode
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
Updates an instance based on the class name, id, and kwargs passed. Update the file.json

(hbnb) create User
1afa163d-486e-467a-8d38-3040afeaa1a1
(hbnb) update User 1afa163d-486e-467a-8d38-3040afeaa1a1 email "ighokarop@gmail.com"
(hbnb) show User 1afa163d-486e-467a-8d38-3040afeaa1a1
[User] (s) [User] (1afa163d-486e-467a-8d38-3040afeaa1a1) {'id': '1afa163d-486e-467a-8d38-3040afeaa1a1', 'created_at': datetime.datetime(2023, 09, 24, 23, 42, 10, 502157), 'updated_at': datetime.datetime(2023, 10, 24, 23, 42, 10, 502186), 'email': 'ighokarop@gmail.com'}
(hbnb)
Authors
Perkins Perkins 
