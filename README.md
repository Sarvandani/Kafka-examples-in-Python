# Kafka-examples-in-Python
Before executing the code, we should know there are three main libraries in Python for interacting with Kafka. They are PyKafka, Kafka-python and Confluent Kafka Libraries.
first of all, we need to install the Kafak on the system. You can use the folliwng link to download a version of Kafka which is compatible with your system (in my case, I downloaded kafka-2.7.2-src.tgz):

https://kafka.apache.org/downloads

-----

Verify that you have Java 8 or a later version installed by the following command in terminal:

`java -verson`

if you don't have, you can use the following link for downloading and install:

https://adoptium.net/en-GB/temurin/archive/?version=11

It should be noticed the fersion of Java and Kafka must be compatible, for this reason, I used Java11. 

------
now, After installing Java, verify that the JAVA_HOME environment variable is set correctly. Open a terminal and run the following command:

`echo $JAVA_HOME`

---------
If the command does not display the path to your Java installation, you need to set the JAVA_HOME variable manually as follows:
1. run the command in terminal to see the versions of Java on your system:
`ls /Library/Java/JavaVirtualMachines/`

2. 
