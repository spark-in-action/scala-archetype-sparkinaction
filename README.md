### Archetype to scaffold projects for _Spark in Action_ book

 * Interactive mode (select `scala-archetype-sparkinaction` and respond to questions):  

```sh
mvn archetype:generate
```

 * Batch mode (change values in the last line) :

```sh
mvn archetype:generate -B \
    -DarchetypeGroupId=org.sparkinaction -DarchetypeArtifactId=scala-archetype-sparkinaction -DarchetypeVersion=0.1 \
    -DgroupId=com.company -DartifactId=project -Dversion=0.1-SNAPSHOT -Dpackage=com.company
```

 * Example compile/run (run `mvn scala:help` for full list of commands) :

```sh
mvn scala:compile
mvn scala:run -DmainClass=com.company.App
```

## Changes:

### 0.1 
 * change java to 1.7
 * make all other changes in pom to reflect SiA requirements
  
===
  
  
### 1.5 (davidB scala-archetype-simple)

* upgrade of scala 2.10.0 
* upgrade version of Specs(2), ScalaTest, Surefire, scala-maven-plugin

### 1.4 (davidB scala-archetype-simple)

* move to sonatype for hosting
* change groupId to net.alchim31.maven
* upgrade version of scala to 2.9.2, version of JUnit, Specs(2) and ScalaTest
        
### 1.3

* upgrade to scala 2.8.0 (as default)
* upgrade version of Specs and ScalaTest
* provide sample of Specs and ScalaTest runnable from maven and eclipse (at least)
