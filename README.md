PicketLink Installer
====================

Introduction
------------

The PicketLink Installer provides an easy way to get started with PicketLink.

It configures a JBoss Enterprise Application Platform 6 installation with all the necessary modules, some basic configurations and quickstarts.

Important Note: Once JBoss Enterprise Application Platform 6 is updated with PicketLink 2.5 libraries and tools, the installer will no longer be necessary.

System Requirements
-------------------

To run the installer, you need the following:

1. Java 1.6, to run Ant and JBoss AS. You can choose from the following:
    * OpenJDK
    * Oracle Java SE
    * Oracle JRockit

2. Apache Ant 1.8.4 or newer

3. Maven 3.0.0 or newer, to build and deploy the examples
    * If you have not yet installed Maven, see the [Maven Getting Started Guide](http://maven.apache.org/guides/getting-started/index.html) for details.
    * If you have installed Maven, you can check the version by typing the following in a command line:

            mvn --version

4. The JBoss Enterprise Application Platform 6 distribution ZIP or the JBoss AS 7 distribution ZIP.
    * For information on how to install and run JBoss, refer to the product documentation.

Check Out the Source
----------------------------------

1. To clone this Git repository, use the following command:

        git clone git@github.com:picketlink/picketlink-installer.git

Usage
----------------------------------

Before starting, make sure you have unzipped the JBoss Enterprise Application Platform 6 distribution ZIP.

1. After you clone the repository, use the following command to create the distribution package:

        cd picketlink-installer
        mvn clean install
2. Enter the target directory and unzip the distribution package:

        cd target
        unzip picketlink-installer-X.X.X (where X.X.X is the current version)

3. Now go to the directory created from the command above and execute the following command:

        cd picketlink-installer-X.X.X
        ant

Now just follow the instructions.

Note for PicketLink Federation 2.1 Users
----------------------------------

The installer updates the PicketLink module(which defaults to 2.1.x) in JBoss EAP 6 with the 2.5 libraries.

You don't need to change any configuration in your deployment to start using this version. The module name is still the same:

        org.picketlink