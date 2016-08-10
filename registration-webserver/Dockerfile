FROM tomcat:7-jre8
MAINTAINER Sophia Parafina <sophia.parafina@docker.com>

# tomcat-users.xml sets up user accounts for the Tomcat manager GUI
# and script access for Maven deployments
ADD tomcat/tomcat-users.xml $CATALINA_HOME/conf/

# MySQL driver jar
ADD tomcat/mysql-connector-java-5.1.36-bin.jar $CATALINA_HOME/lib/

# Install spanners-mvc war from Maven repo
# RUN wget https://s3.amazonaws.com/spara/UserSignup.war -O /usr/local/tomcat/webapps/UserSignup.war
RUN mkdir $CATALINA_HOME/webapps/UserSignup
