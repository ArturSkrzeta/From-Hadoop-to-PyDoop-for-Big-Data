# From-Hadoop-to-PyDoop-for-Big-Data
### Hadoop installation
1. Download it form hadoop.apache.org.
2. Unizp to folder on C driver.
3. Rename directory to hadoop.
4. Create dictionary in hadoop.
```
.\data\datanode
.\data\namenode
```
3. Go to file core-site.xml and add below:
```
<configuration>
  <property>
    <name>fs.defaultFS</name>
    <value>hdfs://localhost:9000</value>
  </property>
</configuration>
```
4. Go to file mapred-site.xml and add below:
```
<configuration>
  <property>
    <name>mapreduce.framework.name</name>
    <value>yarn</value>
  </property>
</configuration>
```
5. Go to yarn-site.xml and add below:
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
6. Go to hdfs-site.xml and add below:
```
<configuration>
  <property>
    <name>dfs.replication</name>
    <value>1</value>
  </property>
  <property>
    <name>dfs.namenode.name.dir</name>
    <value>C:\hadoop\data\namenode</value>
  </property>
  <property>
    <name>dfs.datanode.data.dir</name>
    <value>C:\hadoop\data\datanode</value>
  </property>
</configuration>
```
7. Go to hadoop-env.cmd and update below:
```
set JAVA_HOME=C:\jdk1.8.0_261
```
8. Add Hadoop directory to environment variables for user:
```
HADOOP_HOME
C:\hadoop\bin
```
9. Add below dirs to environment variables for system:
```
C:\hadoop\bin
C:\hadoop\sbin
```
10. Replace C:\hadoop\bin with bin from HadoopConfiguration-FIXbin.rar
