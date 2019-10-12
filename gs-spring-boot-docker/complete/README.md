

#### The OpenJDK Docker Image with  all needed memory tools 
I choose openjdk:11 
- it has standard memory check tool  (top, ps, pmap, free ) to check all process cpu and memory
- it has standard jdk tool (jcmd, jstat,jmap, etc) to check jvm's memory and gc 

#### JDK Tools/Commands for JVM memory tools

- jstat
https://dzone.com/articles/jvm-statistics-with-jstat
- jcmd 
https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/tooldescr006.html
- jmap
https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/tooldescr014.html

#### The Commands could be useful for JVM Memory /GC  ####

jcmd <pid> Thread.print
jcmd <pid> VM.native_memory
jstat -gcutil <pid>



kubectl -it exec -n <namespace>   -<podname>    -- /bin/bash 

jhsdb jmap --heap --pid <PID>

jstat -gcutil <PID>

#### Read More

- How to choose Docker image for openjdk
  https://hub.docker.com/_/openjdk
- JVM Native Memory Tracking 
  https://www.baeldung.com/native-memory-tracking-in-jvm
- Simliar Problem reported by others 
  https://stackoverflow.com/questions/16697135/monitor-non-heap-memory-usage-of-a-jvm
- Httpclient-memory-leak
  https://stackoverflow.com/questions/27732546/httpclienthandler-httpclient-memory-leak
- Similar problem reported by others
  https://github.com/kubernetes/kubernetes/issues/70179





