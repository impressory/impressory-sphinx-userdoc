Using the distribution zip
==========================

If you want to run your own server, you can download a `distribution zip <https://docs.google.com/uc?id=0Byc3ursv9OXJYlkzenY5dzdua3c&export=download>`_ that has been pre-built

To run the server, you'll need two pieces of software:

* `MongoDB <http://mongodb.org>`_, the database that Impressory uses. (This can be either local or remote)

* A `Java Virtual Machine <http://java.oracle.com>`_. Impressory is written in Scala, which runs on the JVM.


To use the distribution zip

1. `Download the zip <https://docs.google.com/uc?id=0Byc3ursv9OXJYlkzenY5dzdua3c&export=download>`_

2. Unzip it wherever you'd like to run it from::

   $ unzip impressory-0.2-SNAPSHOT.zip

4. To run the server, you now just run the start-up script. The instructions below are for Linux (using nohup so that when you close the terminal the program doesn't also close)::

   $ nohup impressory-0.2-SNAPSHOT/bin/impressory > log.out 2> err.out &

The server should now be up and running, listening on port 9000. Open a web browser and visit it. The first user to register is given administrative rights, so you should make sure that's you!

Although that's compiled and run the server, there are probably a few things you'll still want to configure:

* Database environment variables
* Social media logins
* HTTPS
* Port redirection 
