Apache Nutch WebApp README
==========================

<img src="https://nutch.apache.org/assets/img/nutch_logo_tm.png" align="right" width="300" />

For the latest information about Nutch, please visit our website at:

   https://nutch.apache.org/

and our wiki, at:

   https://cwiki.apache.org/confluence/display/NUTCH/Home

Introduction
------------
The Nutch WebApp is built using the [Apache Wicket Java web framework](http://wicket.apache.org/) and [Spring](https://spring.io/).

Running locally
---------------
**N.B.** Currently, you must have a running [Nutch REST Server]() on the same host.

You can easily run the WebApp by executing the following
```bash
% mvn jetty:run
```

If you want to run the WebApp in a [Jakarta Servlet](https://projects.eclipse.org/projects/ee4j.servlet) container i.e. [Apache Tomcat](https://tomcat.apache.org/), then run the following
```bash
% mvn clean install -DskipTests
5 cp target/nutch-webapp-1.0-SNAPSHOT.war $CATALINA_HOME/webapps
```
You can then access the WebApp on the Tomcat host on port 8080.

Contributing
------------
To contribute a patch, follow these instructions (note that installing
[Hub](https://hub.github.com/) is not strictly required, but is recommended).

```
0. Download and install hub.github.com
1. File JIRA issue for your fix at https://issues.apache.org/jira/projects/NUTCH/issues
- you will get issue id NUTCH-xxx where xxx is the issue ID.
2. git clone https://github.com/apache/nutch-webapp.git
3. cd nutch-webapp
4. git checkout -b NUTCH-xxx
5. edit files (please try and include a test case if possible)
6. git status (make sure it shows what files you expected to edit)
7. Make sure that your code complies with the [Nutch codeformatting template](https://raw.githubusercontent.com/apache/nutch/master/eclipse-codeformat.xml), which is basially two space indents
8. git add <files>
9. git commit -m “fix for NUTCH-xxx contributed by <your username>”
10. git fork
11. git push -u <your git username> NUTCH-xxx
12. git pull-request
```

IDE setup
---------

Generate Eclipse project files

```
mvn eclipse:eclipse
```

and follow the instructions in [Importing existing projects](https://help.eclipse.org/2019-06/topic/org.eclipse.platform.doc.user/tasks/tasks-importproject.htm).

IntelliJ IDEA users can also import Eclipse projects using the ["Eclipser" plugin](https://www.tutorialspoint.com/intellij_idea/intellij_idea_migrating_from_eclipse.htm)https://plugins.jetbrains.com/plugin/7153-eclipser), see also [Importing Eclipse Projects into IntelliJ IDEA](https://www.jetbrains.com/help/idea/migrating-from-eclipse-to-intellij-idea.html#migratingEclipseProject).