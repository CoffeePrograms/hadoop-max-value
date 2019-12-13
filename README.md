How to start hadoop app on Windows
1. Open console. 
2. Go to sbin folder: 
    cd C:\hadoop-2.8.0\sbin
3. Start hadoop: 
        start-dfs.cmd
        start-yarn.cmd
4. Disable safe mode to add and remove folders
        hadoop dfsadmin -safemode leave
5. Create folder for input data
        hadoop fs -mkdir /input_dir
6. Add data from disc to hadoop
        hadoop fs -put C:/input_file.txt /input_dir
7. Add data from disc to hadoop
        hadoop fs -put C:/input_file.txt /input_dir
8. View data on hadoop to make sure data is added
        hadoop dfs -cat /input_dir/*
9. Start app
        hadoop jar C:/WordCount.jar WordCount /input_dir /output_dir
10. View result
        hadoop dfs -cat /output_dir/*
