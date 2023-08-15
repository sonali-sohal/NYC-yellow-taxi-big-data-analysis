# NYC-Yellow-Taxi-Big-Data-Analytics
Analysis of New York city yellow taxi data set with Hadoop MapReduce.

## Information to analyze:
1. What is the average number of passengers per trip in general and per day of the week?
2. What is the average trip distance in general and per day of the week?
3. What are the most used payment types?
4. How does the number of Passengers change over the week day and weekend. A graph (using the output of a MapReduce job) showing the average number of passengers over the day (per hour).
5. How does the total distance travelled change over different time of the day for all days of the week. a graph showing the average trip distance over the day (per hour).

## Execution Steps:
- Individual java programs have been created to answer each of the Intial questions that were set up for analysis. The naming convention followed is QuestionX.java where x denotes the question number 
	for example; question 1 is solved in Question1.java

#### step 1: sudo docker exec -it namenode bash
#### step 2: export HADOOP_CLASSPATH=/usr/lib/jvm/java-1.8.0-openjdk-amd64/lib/tools.jar  
#### step 3: hadoop com.sun.tools.javac.Main QuestionX.java ( x denotes question number)
#### step 4: jar cf wc.jar QuestionX*.class
#### step 5:  hadoop jar wc.jar QuestionX /dataset /outputX
#### step 6: hdfs dfs -cat /outputX/part-r*
