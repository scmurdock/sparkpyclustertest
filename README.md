Starting the Spark cluster in the workspace:

$SPARK_HOME/sbin/start-master.sh

After you type this command, you will see something to the following output:

starting org.apache.spark.deploy.master.Master, logging to /opt/spark-2.3.4-bin-hadoop2.7/logs/spark--org.apache.spark.deploy.master.Master-1-67e5ccbadadd.out

To view the logs, you should cat the file mentioned in the output message.

For example, if I received the sample message mentioned earlier, I would type

$ cat opt/spark-2.3.4-bin-hadoop2.7/logs/spark--org.apache.spark.deploy.master.Master-1-67e5ccbadadd.out

Look for a message similar to this: Starting Spark master at spark://67e5ccbadadd:7077

Clone the repository to the workspace by typing this command:

$ git clone https://github.com/scmurdock/sparkpyclustertest.git

Next submit the sparkpytest.py script to the cluster

$ SPARK_HOME/bin/spark-submit /home/workspace/sparkpyclustertest/sparkpytest.py | tee /home/workspace/sparkpyclustertest/logs/sparkpytest.log

You should see a lot of console output, including a line similar to the following:

20/08/17 09:41:58 INFO DAGScheduler: Job 1 finished: count at NativeMethodAccessorImpl.java:0, took 0.059077 s
Lines with a: 4, lines with b: 0

This means the application finished running, and has produced the desired output