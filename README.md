# hadoop2.1

# hadoop-Assignment2.1

[acadgild@localhost ~]$ hadoop fs -ls
17/01/15 14:23:01 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 4 items
drwxr-xr-x   - acadgild supergroup          0 2017-01-15 14:14 hadoop
drwxr-xr-x   - acadgild supergroup          0 2015-11-17 02:03 oozie-acad
drwxr-xr-x   - acadgild supergroup          0 2015-11-17 02:00 share
drwxr-xr-x   - acadgild supergroup          0 2017-01-14 19:59 test
[acadgild@localhost ~]$ hadoop fs -test -d /user/acadgild/hadoop
17/01/15 14:23:56 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
[acadgild@localhost ~]$  hadoop fs -mkdir  -f /user/acadgild/hadoop/Word-count.txt
-mkdir: Illegal option -f
Usage: hadoop fs [generic options] -mkdir [-p] <path> ...
[acadgild@localhost ~]$  hadoop fs -mkdir  -p /user/acadgild/hadoop/Word-count.txt
17/01/15 14:26:42 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
mkdir: `/user/acadgild/hadoop/Word-count.txt': Is not a directory
[acadgild@localhost ~]$ hadoop fs -ls
17/01/15 14:27:42 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 4 items
drwxr-xr-x   - acadgild supergroup          0 2017-01-15 14:14 hadoop
drwxr-xr-x   - acadgild supergroup          0 2015-11-17 02:03 oozie-acad
drwxr-xr-x   - acadgild supergroup          0 2015-11-17 02:00 share
drwxr-xr-x   - acadgild supergroup          0 2017-01-14 19:59 test
[acadgild@localhost ~]$ echo "1,ramesh,software,2500" | hadoop fs -put - /user/acadgild/hadoop/Word-count.txt
17/01/15 14:30:21 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
put: `/user/acadgild/hadoop/Word-count.txt': File exists
[acadgild@localhost ~]$ hadoop fs -rm -r /user/acadgild/hadoop/Word-count.txt
17/01/15 14:31:19 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
17/01/15 14:31:25 INFO fs.TrashPolicyDefault: Namenode trash configuration: Deletion interval = 0 minutes, Emptier interval = 0 minutes.
Deleted /user/acadgild/hadoop/Word-count.txt
[acadgild@localhost ~]$ echo "1,ramesh,software,2500" | hadoop fs -put - /user/acadgild/hadoop/Word-count.txt
17/01/15 14:31:45 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
[acadgild@localhost ~]$ echo "2,maheshh,mentor,4500" | hadoop fs -appendToFile - /user/acadgild/hadoop/Word-count.txt17/01/15 14:33:16 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
[acadgild@localhost ~]$  hadoop fs -cat /user/acadgild/hadoop/Word-count.txt
17/01/15 14:34:00 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
1,ramesh,software,2500
2,maheshh,mentor,4500
[acadgild@localhost ~]$ 
