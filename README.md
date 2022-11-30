# Using GWT with Jakarta

This sample project demonstrates a draft of a patch that enables using GWT-RPC with jakarta.servlet apis. Built from
the `modular-webapp` archetype at https://github.com/tbroyer/gwt-maven-archetypes/, there are a few small changes
to fetch the `2.11.0-jakarta-SNAPSHOT` version from https://repo.vertispan.com/gwt-snapshot/ and run a simple GWT-RPC
servlet and app under Jetty 11.

To develop with this project, run these commands:
 1. First, start a codeserver with `mvn gwt:codeserver -pl jakarta-gwt-app-client -am`
 2. Next, start a Jetty server with `mvn jetty:run -pl jakarta-gwt-app-server -am -Denv=dev`

To deploy to production, either invoke `mvn package` and copy the resulting war in `jakarta-gwt-app-server/target` to
any jakarta.servlet container, or build and run directly via
`mvn package jetty:run-war -Denv=prod`.
