# mq-test-apps

This my attempt to preserve MQ test cases to present Instana observability demonstrations. 

Original code was obtained from tutorials and development sites, augmented to specific behaviors, and then execute.

As this was performed on a Mac, the instruction on setup and execution may be different from a Windows machine.

=============

As instructed in tutorials:
1.  In the /Users/<user id>/ directory, create a directory called MQCLient
2.  Within the MQCLient directory, create the project directory:  /com/ibm/mq/samples/jms


=============
Use Cases


Use Case 1:  Normal processing flow (1000 messages - Q1 - 3)
javac -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com/ibm/mq/samples/jms/NormalFlow.java
javac -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com/ibm/mq/samples/jms/NormalFlow2.java
javac -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com/ibm/mq/samples/jms/NormalFlow3.java


java -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com.ibm.mq.samples.jms.NormalFlow
java -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com.ibm.mq.samples.jms.NormalFlow2
java -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com.ibm.mq.samples.jms.NormalFlow3


Use Case 2:  Limited Queue Depth (DEV.QUEUE.4 with 50 messages, max length 500)

javac -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com/ibm/mq/samples/jms/LimitQueueDepth.java
java -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com.ibm.mq.samples.jms.LimitQueueDepth

Use Case 3:  Connectivity issue (DEV.QUEUE.4 employing TLS)

javac -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com/ibm/mq/samples/jms/ConnectivityTest.java
java -cp ./com.ibm.mq.allclient-9.1.4.0.jar:./javax.jms-api-2.0.1.jar:. com.ibm.mq.samples.jms.ConnectivityTest
