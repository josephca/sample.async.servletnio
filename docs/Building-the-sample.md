This sample can be built using either [Gradle](#building-with-gradle) or [Maven](#building-with-maven).

In addition to publishing the war to the local maven repository, the built war file is copied into the apps directory of the server configuration located in the async-websocket-wlpcfg directory:

```text
async-servlet-nio-wlpcfg
 +- servers
     +- servletNioSample                         <-- specific server configuration
        +- server.xml                            <-- server configuration
        +- apps                                  <- directory for applications
           +- async-servlet-nio-application.war  <- sample application
        +- logs                                  <- created by running the server locally
        +- workarea                              <- created by running the server locally
```

## Building with Gradle

This sample can be built using [Gradle](http://gradle.org/).

```bash
$ gradle build publishToMavenLocal
```

If you want to also run the functional verification tests then you need to set the libertyRoot property in the async-servlet-nio-application/gradle.properties file to point to a Liberty install.

## Building with maven

This sample can be built using [Apache Maven](http://maven.apache.org/).

```bash
$ mvn install
```

## Next step

* [Downloading WAS Liberty](/docs/Downloading-WAS-Liberty.md)