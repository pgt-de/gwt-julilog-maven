# gwt-julilog-maven
Sample project created by the gwt maven plugin archetype.

This projects showcases the classpath issue with tomcat-jdbc/ tomcat-juli and the old jsp dependency introduced by the gwt jetty version.

016-12-19 11:56:49.606:WARN:oejuc.AbstractLifeCycle:main: FAILED org.eclipse.jetty.server.Server@7c1eb0b: java.util.ServiceConfigurationError: org.apache.juli.logging.Log: Provider org.eclipse.jetty.apache.jsp.JuliLog not a subtype
java.util.ServiceConfigurationError: org.apache.juli.logging.Log: Provider org.eclipse.jetty.apache.jsp.JuliLog not a subtype

The tomcat jdbc datasource is started in the servlet init. 
The jsp depencency is excluded in the pom.
Intellij still includes the dependency into the classpath when starting the project...

