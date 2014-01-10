.. _setup-configuration:

Configuration
=============

An Impressory server can be configured either by setting environment variables, or by passing arguments to the start-up script

.. _setup-configuration-db:

Database
--------

The following environment variables configure the MongoDB connection::

    $IMPRESSORY_MONGO_URL
    $IMPRESSORY_MONGO_DBNAME
    $IMPRESSORY_MONGO_DBUSER
    $IMPRESSORY_MONGO_DBPWD

These can also be set by passing them as arguments to the start script::

    -Dmongo.connection=
    -Dmongo.dbname= 
    -Dmongo.dbuser= 
    -Dmongo.dbpwd= 

Social media logins
-------------------

Students can log in using GitHub or Twitter accounts.

For this to work, you'll need to set an OAuth client key and secret that is issued to you by GitHub or Twitter.

GitHub:

1. Register an application on `GitHub <https://github.com/settings/applications/new>`_

   The authorisation callback URL is {your server URL} + /oauth/github/callback

2. Set the Client ID and Client Secret before starting Assessory. This can be done by setting these environment variables::

     $IMPRESSORY_AUTH_GITHUB_CKEY
     $IMPRESSORY_AUTH_GITHUB_CSECRET
 
   or by passing them as arguments to the start script::

     -Dauth.github.ckey=
     -Dauth.github.csecret=


Twitter:

1. Register an application on `Twitter <https://dev.twitter.com/apps>`_

   The authorisation callback URL is {your server URL} + /oauth/twitter/callback

2. Set the Client ID and Client Secret before starting Assessory. This can be done by setting these environment variables::

     $IMPRESSORY_AUTH_TWITTER_CKEY
     $IMPRESSORY_AUTH_TWITTER_CSECRET

   or by passing them as arguments to the start script::

     -Dauth.twitter.ckey=
     -Dauth.twitter.csecret=


HTTPS
------

To make Impressory listen using HTTPS, you'll need to pass a few more parameters to the start script, as described `here <http://www.playframework.com/documentation/2.2.x/ConfiguringHttps>`_