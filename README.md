# Neo4j and Django tutorial

This is not _the_ way to do it, just _a_ way but the only way using the
new neo4j-embedded Python bindings that I have seen.
This tutorial is written for Ubuntu (10.10) but it should work for any
GNU Linux flavor and I have seen a similar setup in OS X.

# Installation

Download a sample database, I will use the Twitter database from
example-data.neo4j.org.
(http://example-data.neo4j.org/files/twitter.s12gx.zip)

Download jpype (0.5.4.2).
(http://sourceforge.net/projects/jpype/files/)

### Install python-virtualenv.
    sudo apt-get install virtualenv

### Clone out my neo4j-django-tutorial git repository.
    git clone git://github.com/johanlundberg/neo4j-django-tutorial.git
    cd neo4j-django-tutorial

### Create a new virtual python environment.
    virtualenv --no-site-packages env

### Activate your environment.
    source env/bin/activate

### Install openjdk-6-jdk and python-dev packages.
    sudo apt-get install openjdk-6-jdk python-dev

### Set your JAVA_HOME evironment variable.
    export JAVA_HOME=/usr/lib/jvm/java-6-openjdk/

### Build and install JPype.
    pip install /path/to/JPype-0.5.4.2.zip

### Install Django (1.3.1) and neo4j-embedded Python bindings (1.6.b1).
    pip install django neo4j-embedded

### Make a directory to hold the neo4j database.
    mkdir neo4jdb

### Unzip twitter.s12gx.zip to the neo4jdb directory.
    unzip twitter.s12gx.zip -d neo4jdb

### Start a new Django project and create a new app.
    mkproj.sh project_name
    mkapp.sh project_name app_name

### To make it easier to use the Lucene indexes you should install lucene-querybuilder (0.1.5).
    pip install lucene-querybuilder

# Going forward

Have a look in the neo4jtut projects generic_settings.py and
neo4jclient.py file for some tips on how to I use Neo4j and Django.
