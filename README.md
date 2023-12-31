# Kafka examples in Python

# 1. Kafka installation
Before executing the code, we should know there are three main libraries in Python for interacting with Kafka. They are PyKafka, Kafka-python and Confluent Kafka Libraries.
If we are using Amazon MSK clusters then We can use PyKafka or Kafka-python libraries and If we are using Confluent Kafka clusters then We have to use Confluent Kafka Library. We may use local host or external cluster. 
First of all, we need to install the Kafak on the system. You can use the folliwng link to download a version of Kafka which is compatible with your system (in my case, I downloaded kafka-2.7.2-src.tgz):

https://kafka.apache.org/downloads

-----

Verify that you have Java 8 or a later version installed by the following command in terminal:

`java -verson`

if you don't have, you can use the following link for downloading and install:

https://adoptium.net/en-GB/temurin/archive/?version=11

It should be noticed the version of Java and Kafka must be compatible, for this reason, I used Java11. 

------
now, After installing Java, verify that the JAVA_HOME environment variable is set correctly. Open a terminal and run the following command:

`echo $JAVA_HOME`

---------
If the command does not display the path to your Java installation, you need to set the JAVA_HOME variable manually as follows:

1. run the command in terminal to see the versions of Java on your system:

`ls /Library/Java/JavaVirtualMachines/`

in my case, the results were:

Jdk-17.0.2.jdk  temurin-11.jdk

since I had two different vresions of Java. As mentioned earlier, only 11 version was compatible in my case.

2. Open the shell profile file in a text editor
For Bash, open ~/.bash_profile or ~/.bashrc.
For Zsh, open ~/.zshrc.

Add the following line at the end of the Zsh file (Contents/Home MUST BE ADDED at the end of line):

Export JAVA_HOME=/Library/Java/JavaVirtualMachines/temurin-11.jdk/Contents/Home

----------

After setting path, we can check again as follows in the terminal:

`echo $JAVA_HOME`

The results must be /Library/Java/JavaVirtualMachines/temurin-11.jdk/Contents/Home. 

------- 

now, we continue installing Kafka. Extract the source code: Open a terminal and navigate to the directory where you downloaded the Kafka source distribution. 
Use the following command to extract the contents:

`tar -xzf kafka-2.7.2-src.tgz`

Navigate to the extracted Kafka directory:

`cd kafka-2.7.2-src`

Run the following command to initiate the build process:

`./gradlew` 

-----------------

Verify the build: Once the build process is finished, you can run the following command to ensure that Kafka is built successfully:

`./gradlew jar` 

This command compiles and packages Kafka's JAR files.

------------------
Now, we can check the version of installed Kafka by the following command, however, we must be in the directory of downloaded Kafka:

`bin/kafka-server-start.sh --version`


# 2. Starting Kafka server

Before executing any code in Python, the following commands in the directory of Kafka must be executed in two separated terminals:

`bin/zookeeper-server-start.sh config/zookeeper.properties`

`bin/kafka-server-start.sh config/server.properties`

your two treminals will be in runing conditions!

Now, it is the time to run and modify your Python code!






