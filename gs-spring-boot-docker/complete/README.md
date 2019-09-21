Use docker ps to get the name of the existing container.
Use the command docker exec -it <container name> /bin/bash to get a bash shell in the container.

How to choose DOCKER IMAGE for openjdk11
https://hub.docker.com/_/openjdk

I choose openjdk:11 which provides 
standard memory check tool  (top, ps, pmap, free ) to check all process cpu and memory
also standard jdk tool (jcmd, jstat,jmap, etc) to check jvm's memory and gc 

more to read
jstat
https://dzone.com/articles/jvm-statistics-with-jstat
jcmd 
https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/tooldescr006.html
jmap
https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/tooldescr014.html

https://www.baeldung.com/native-memory-tracking-in-jvm
https://stackoverflow.com/questions/16697135/monitor-non-heap-memory-usage-of-a-jvm


jcmd <pid> Thread.print
jcmd <pid> VM.native_memory
jstat -gcutil <pid>




