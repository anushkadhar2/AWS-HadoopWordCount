# HadoopWC
this repository was created to create custom  hadoop  jar for the word count program and run them in a distributed computer or a single  node cluster or even an  multinode cluster. For now and for testing purpose I am using  a single node cluster ie is on my compter.I have used [Apache Hadoop] tutorial for  the quick setup of hadoop 2.4.1.
You need to install jvm and java in your machine. For this tutorial  I am assuming  that you are using ubuntu as your opreating system. For this experiment I am using ubuntu 14.04 LTS.



##You can still install it using apt-get. To install any version, first execute the following commands:

$ sudo apt-get install python-software-properties
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt-get update

## you are now installing the oracle java
$ sudo apt-get install oracle-java8-installer

$ sudo update-alternatives --config java



$ sudo update-alternatives --config javac


- download the latest  stabe version of hadoop form [hadoop download]

### Setting hadoop 

- For the single node setup please  use  the tutorial from  [hadoop prepare and setup] with in the hadoop folder. And the files with in it.
- Rename the hadoop folder to hadoop. In my computer I made the following changes
```sh
$ mv hadoop-2.6.0  hadoop
```
-In your computer change the loacation to  from you existing folder to /usr/local/hadoop
```sh
$ sudo hadoop  /usr/local/hadoop
```
- type your password and transfer would be complete to the local  folder.

### changes in the .bashrc file
-  you need to set your java home in java bashrc file
- to open the file
```sh
$ sudo gedit .bashrc
```
- you need to set you java path variables in the .bashrc file as
```sh
# Set Hadoop-related environment variables
export HADOOP_HOME=/usr/local/hadoop/


export JAVA_HOME=/usr/lib/jvm/java-8-oracle/

# for hadoop related file you need to have the following settings
# Add Hadoop bin/ directory to PATH

export PATH=$PATH:$HADOOP_HOME/bin
export HADOOP_MAPRED_HOME=$HADOOP_HOME
export HADOOP_COMMON_HOME=$HADOOP_HOME
export HADOOP_HDFS_HOME=$HADOOP_HOME
export YARN_HOME=$HADOOP_HOME
export HADOOP_CONF_DIR=$HADOOP_HOME/etc/hadoop
export YARN_CONF_DIR=$HADOOP_HOME/etc/hadoop
