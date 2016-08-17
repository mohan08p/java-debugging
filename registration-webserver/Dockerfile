FROM tomcat:7-jre8
MAINTAINER Sophia Parafina <sophia.parafina@docker.com>

# tomcat-users.xml sets up user accounts for the Tomcat manager GUI
# and script access for Maven deployments
ADD tomcat/tomcat-users.xml $CATALINA_HOME/conf/

# add MySQL JDBC driver jar
ADD tomcat/mysql-connector-java-5.1.36-bin.jar $CATALINA_HOME/lib/

# create mount point for volume with application
RUN mkdir $CATALINA_HOME/webapps/UserSignup

# add jpda debugging environmental variables
ENV JPDA_ADDRESS="8000"
ENV JPDA_TRANSPORT="dt_socket"

# start tomcat7-debug
ENTRYPOINT ["catalina.sh", "jpda", "start"]
