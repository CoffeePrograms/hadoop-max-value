What does the app do
---
The program finds the word that is repeated most often and displays it on the screen (look at the result.jpg)

How to install hadoop
---
https://github.com/MuhammadBilalYar/Hadoop-On-Window

How to start hadoop app on Windows
---
1. Open console. 
2. Go to sbin folder: 
    ```
    cd C:\hadoop-2.8.0\sbin
    ```
3. Start hadoop: 
```
        start-dfs.cmd
        start-yarn.cmd
```
4. Disable safe mode to add and remove folders
```
hadoop dfsadmin -safemode leave
```
5. Create folder for input data
```
hadoop fs -mkdir /input_dir
```
6. Add data from disc to hadoop
```
hadoop fs -put C:/input_file.txt /input_dir
```
7. Add data from disc to hadoop
```
hadoop fs -put C:/input_file.txt /input_dir
```
8. View data on hadoop to make sure it is added
```
hadoop dfs -cat /input_dir/*
```
9. Start app
```
hadoop jar C:/WordCount.jar WordCount /input_dir /output_dir
```
10. View result
```        
hadoop dfs -cat /output_dir/*
```
If it does not start
---
Manually delete the files in the datanode (path: C:\hadoop-2.8.0\data\datanode) and type in the console: 
 ```   
 hdfs namenode -format
  ```
  and add the input files again
