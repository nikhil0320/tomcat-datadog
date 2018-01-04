This is the playbook to configure the datadog to moniter the tomcat server.<br>
<b>Prerequrities</b><br>
-Datadog-agent to be installed.<br>

<b>Steps</b>
1.Run the playbook to configure the tomcat.<br>
2.Variables:
  JMX_port:It is port in which the app server sent the metrics to the particular port called jmx port

3.create a file in tomcat folder bin/setenv.sh in the tomcat server and to enable jmxromote.port:copy the below code and execute the setenv.sh file

JAVA_OPTS="-Dcom.sun.management.jmxremote
<br> -Dcom.sun.management.jmxremote.port=9998
 -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false "<br>

 5.Restart  tomcat server<br>
 6.Restart datadog-agent from /etc/init.d/dd-agent  Restart<br>
 7.check the status of datadog-agent /etc/init.d/dd-agent  info<br>

 <b>Note:</b>
The playbook Works for amazon-linux
