#init container with a prebuild java arm image including jce libraries
FROM wdjenane/java-8-armv7l-jce

#Add your springboot app
ADD app.jar /opt/app.jar

#Expose port used by the application
EXPOSE 8080

#Run app
#If you need to add some custom params to JVM you can do that like below (-Dspring.profiles.active=dev)
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-Dspring.profiles.active=dev,"-jar","/opt/zmanager.jar"]

