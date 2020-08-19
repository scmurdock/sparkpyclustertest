# Submitting a Spark application to the Spark cluster using the project workspace in the Spark Data Streaming Udacity Course:


## Open a terminal and type the following command:
$ $SPARK_HOME/sbin/start-master.sh

After you type this command, you will see something similar to the following output:

Starting Spark master at spark://67e5ccbadadd:7077

## Clone the repository to the workspace by typing this command:

$ git clone https://github.com/scmurdock/sparkpyclustertest.git

## Submit the sparkpytest.py script to the cluster:

$ SPARK_HOME/bin/spark-submit /home/workspace/sparkpyclustertest/sparkpytest.py | tee /home/workspace/sparkpyclustertest/logs/sparkpytest.log

You should see a lot of console output, including a line similar to the following:

20/08/17 09:41:58 INFO DAGScheduler: Job 1 finished: count at NativeMethodAccessorImpl.java:0, took 0.059077 s
Lines with a: 4, lines with b: 0

This means the application finished running, and has produced the desired output

## Want to get this running locally? Try running a Spark cluster, and submitting a Spark application to the cluster using Docker:

See: https://github.com/scmurdock/sparkdockerclustertest.git