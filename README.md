# From-Hadoop-to-PyDoop-for-Big-Data
### Hadoop installation
1. Download it form hadoop.apache.org.
2. Unizp to folder on C driver.
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
5. yarn-site.xml
6. hdfs-site.xml
7. hadoop-env.cmd


