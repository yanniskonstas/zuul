zuul API gateway

## Prerequisites to run the sample

* Download and install the Java Development Kit (JDK) for your operating system. JDK is required to compile and build the source code in the samples. You can [download](http://www.oracle.com/technetwork/java/javase/downloads/index.html) the latest JDK from the Oracle website.  We use Java version 11 to test all the samples.
* Download and install Apache [Maven](https://maven.apache.org/install.html). Maven is a project management and comprehension tool that makes it easy to declare third-party (external) dependencies of your Java project required in the compile/build phase. It has various plugins such as the compiler, which compiles your Java source code and produces the runnable artifact (binary). You can download Maven from the Apache website.  Follow the installation instructions  to install Maven on your operating system. We use Maven version 3.5 to test all the samples.
* Download and install the [curl](https://curl.haxx.se/download.html) command line tool from the curl website.  You use curl in the book as a client application to access microservices. Most of the operating systems do have curl installed out of the box.
* Download and install the Git command-line client on your computer. You only use Git client once to clone our samples Git repository. 

## Sample calls

curl http://localhost:9090/retail/orders/c5958cd9-4213-45a4-9a93-dc2f044fa7b5 # This will work only when authorisation is disabled 
curl -u application1:application1secret -H "Content-Type: application/x-www-form-urlencoded" -d "grant_type=client_credentials" http://localhost:9090/token/oauth/token # Get the token through Zuul gateway
curl -H 'Authorization:Bearer 0700acca-97ff-46c0-9b7a-0ddeea096c1d' http://localhost:9090/retail/orders/c5958cd9-4213-45a4-9a93-dc2f044fa7b5 

