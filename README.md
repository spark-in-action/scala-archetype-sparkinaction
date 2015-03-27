### Archetype to scaffold projects for _Spark in Action_ book

 * In **Eclipse** (or similar in **IntelliJ IDEA**):  
    1 `File > New > Project... > Maven > Maven Project`  
    2 `Next` on the first screen of the _New project_ wizard  
    3 `Configure... > Add Remote Catalog...`  
    4 Enter the following URL in the `Catalog file` field: http://goo.gl/ln2pF0  
      Enter _Spark in Action_ (or whatever you like) in the `Description` field  
    5 After you close the dialog choose the catalog you just created in the Catalog dropdown

<small>
http://goo.gl/ln2pF0 is just a shorthand for  https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml  </small>


 * **From the terminal** (interactive mode): Select the only option (1) and answer subsequent questions:

```sh
mvn archetype:generate -DarchetypeCatalog=http://goo.gl/ln2pF0
```

 * **Batch mode** (change the values in the last line):

```sh
mvn archetype:generate -B \
    -DarchetypeCatalog=http://goo.gl/ln2pF0 \
    -DarchetypeGroupId=org.sparkinaction \
    -DarchetypeArtifactId=scala-archetype-sparkinaction \
    -DarchetypeVersion=0.1 \
    -DgroupId=com.company -DartifactId=project -Dversion=0.1-SNAPSHOT -Dpackage=com.company
```

 * ***Example usage*** *(run `mvn scala:help` for full list of commands):*

```sh
mvn scala:compile
mvn scala:run -DmainClass=com.company.App
```
