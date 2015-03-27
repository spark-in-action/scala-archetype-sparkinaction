### Archetype to scaffold projects for the ___Spark in Action___ book

 * In **Eclipse** (or similar in **IntelliJ IDEA**):  
    1 `File > New > Project... > Maven > Maven Project`  
    2 `Next` on the first screen of the _New project_ wizard  
    3 `Configure... > Add Remote Catalog...`  
    4 Enter the following URL in the `Catalog file` field: https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml  
      Enter `Spark in Action` in the `Description` field  
    5 After you close the dialog, choose the `Spark in Action` catalog in the `Catalog` dropdown list

<small>
We experienced some intermittent problems with GitHub hosted archetype catalogs when trying to use them from Eclipse/Idea. If that happens to you, please use one of the following two methods from the terminal. After the project materializes, simply _Import existing Maven project_ from your IDE of choice.
</small>



 * **From the terminal** (interactive mode):  
 <small>
 Select the only possible option (1) and answer subsequent questions.
 </small>

```sh
mvn archetype:generate -DarchetypeCatalog=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml
```



 * **From the terminal or a shell script** (batch mode):  
 <small>
 Don't forget to change parameter values in the last line.
 </small>

```sh
mvn archetype:generate -B \
    -DarchetypeCatalog=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml \
    -DarchetypeGroupId=org.sparkinaction \
    -DarchetypeArtifactId=scala-archetype-sparkinaction \
    -DarchetypeVersion=0.1 \
    -DgroupId=com.company -DartifactId=project -Dversion=0.1-SNAPSHOT -Dpackage=com.company
```



 * ***Generated project example usage*** *(run `mvn scala:help` for full list of commands):*


```sh
mvn scala:compile
mvn scala:run -DmainClass=com.company.App
```
