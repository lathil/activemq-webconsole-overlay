# activemq-webconsole-overlay
Example project to deploy activemq and broker as embedded in a war for deployment in Tomcat

The project configuration show how to use maven-war-plugin overlay configuration to use and overload activemq webconsole war to be deployed in a container such as Tomcat.

The web console in this case is run as embedded and takes its configuration from its files in WEB-INF/webconsole-embedded.xml, WEB-INF/webconsole-query.xml and WEB-INF/activemq.xml
You can overload those files with your configuration by copying them in the project folder src/main/webapp/WEB-INF and modifying them there.

The actual project does that by modifying WEB-INF/activemq.xml with adding a location to the PropertyPlaceholderConfigurer. This allows to add a .properties file to the class path with configuration values.

This allows the web console + broker to be integrated in other projects.

The webconsole + activemq broker with the defined version deploy ok in a Tomcat 8 under Java8. 
