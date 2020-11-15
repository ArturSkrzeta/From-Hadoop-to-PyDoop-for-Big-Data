# From-Hadoop-to-PyDoop-for-Big-Data
### Hadoop installation
1. Download it form hadoop.apache.org.
2. Unizp to folder on C driver.
3. Rename directory to hadoop.
4. Create dictionary in hadoop:
```
.\data\datanode
.\data\namenode
```
5. Go to file core-site.xml and add below:
```
<configuration>
  <property>
    <name>fs.defaultFS</name>
    <value>hdfs://localhost:9000</value>
  </property>
</configuration>
```
6. Go to file mapred-site.xml and add below:
```
<configuration>
  <property>
    <name>mapreduce.framework.name</name>
    <value>yarn</value>
  </property>
</configuration>
```
7. Go to yarn-site.xml and add below:
```
<configuration>
  <property>
    <name>yarn.nodemanagaer.aux-services</name>
    <value>mapreduce_shuffle</value>
  </property>
  <property>
    <name>yarn.nodemanager.auxservices.mapreduce.shuffle.class</name>
    <value>org.apache.hadoop.mapred.ShuffleHandler</value>
  </property>
</configuration>
```
8. Go to hdfs-site.xml and add below:
```
<configuration>
  <property>
    <name>dfs.replication</name>
    <value>1</value>
  </property>
  <property>
    <name>dfs.namenode.name.dir</name>
    <value>file:/C:/hadoop/data/namenode</value>
  </property>
  <property>
    <name>dfs.datanode.data.dir</name>
    <value>C:\hadoop\data\datanode</value>
  </property>
</configuration>
```
9. Go to hadoop-env.cmd and update below:
```
set JAVA_HOME=C:\jdk1.8.0_261
```
10. Add Hadoop directory to environment variables for user:
```
HADOOP_HOME
C:\hadoop\bin
```
11. Add below dirs to environment variables for system:
```
C:\hadoop\bin
C:\hadoop\sbin
```
12. Replace C:\hadoop\bin with bin from HadoopConfiguration-FIXbin.rar.
13. Go to CMD and check if it works with command:
```
>hadoop version
>hdfs namenode -format
```
14. Run Hadoop with command:
```
C:\hadoop\sbin>start-all.cmd
```
13. You can check HDFS (namenode and datanode) under port:
```
http://localhost:9870
```
15. Making directions in HDFS:
```
hdfs dfs -mkdir /dir_name
```
16. Listing all directories in HDFS:
```
hdfs dfs –ls /
```
17. Copying local files into HDFS
```
hdfs dfs -copyFromLocal ‪C:\Users\U742905\Downloads\test.txt /sample
```
