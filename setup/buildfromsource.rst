Building Impressory from source
===============================

Impressory is an open source project. This means that one way to run the server is to compile and run the source code. These instructions assume you intend to run the server on Linux or Mac. (We’ll develop Windows instructions in due course.)

First, we need a few pieces of software:

* `MongoDB <http://mongodb.org>`_, the database that Impressory uses.

* A `Java Virtual Machine <http://java.oracle.com>`_. Impressory is written in Scala, which runs on the JVM.

* `sbt <http://www.sbt-scala.org>`_, the Scala Build Tool. (It’s not very big.)

* `git <http://git-scm.com>`_, to get the source code so we can build it.


Then we can build the software

1. Clone the sourcecode repository from GitHub::

   $ git clone https://github.com/impressory/impressory.git


2. Ask sbt to build the distribution zip file. This builds a zip file containing everything you need to run the server::

   $ sbt dist

3. Unzip the distribution file it made, and make sure the start script has execute permissions. (These instructions are for Linux)::

   $ unzip impressory-0.1.zip
   $ cd impressory-0.1
   $ chmod u+x start


4. To run the server, you now just run the start script. The instructions below are for Linux (using nohup so that when you close the terminal the program doesn't also close)::

   $ nohup ./start > log.out 2> err.out &

The server should now be up and running, listening on port 9000. Open a web browser and visit it. The first user to register is given administrative rights, so you should make sure that's you!

Although that's compiled and run the server, there are probably a few things you'll still want to configure:

* Social media logins
* Port redirection 
* HTTPS
