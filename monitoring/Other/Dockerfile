FROM tomcat
RUN mkdir /data
ADD jmx_prometheus_javaagent-0.7-SNAPSHOT.jar /data/jmx_prometheus_javaagent-0.7-SNAPSHOT.jar
ADD prometheus-jmx-config.yaml /data/prometheus-jmx-config.yaml
CMD java -javaagent:/data/jmx_prometheus_javaagent-0.7.jar=8088:/data/prometheus-jmx-config.yaml -jar $TOMCAT_HOME/start.jar