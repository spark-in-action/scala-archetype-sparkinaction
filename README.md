### Archetype to scaffold projects for the ___Spark in Action___ book

<img src="http://www.manning.com/bonaci/bonaci_cover150.jpg"
 alt="The book cover" title="Spark in Action cover page" align="right" />  
However unlikely, you maybe still haven't purchased the book, so here's the link: [Spark in Action](http://t.co/8dVXGkfits). Use the coupon code `mlbonaci` for 50% off.  
Thanks
<br><br><br><br>


 * In **Eclipse** (for **IntelliJ IDEA** first use interactive or batch mode in terminal to generate a new project then import it as existing maven project):  
1. `File > New > Project... > Maven > Maven Project`  
2. Click `Next` on the first screen of the _New project_ wizard  
3. Select `Configure... > Add Remote Catalog...`  
4. Enter the following URL in the `Catalog file` field: https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml  
      Enter `Spark in Action` in the `Description` field  
5. After you close the dialog, choose the `Spark in Action` catalog in the `Catalog` dropdown list
6. In the next dialog simply enter you project details and confirm with `Finish`
7. Once the new projects generates change the Scala version to 2.10.5:
      Right click on the generated project and select:
      `Scala > Set the Scala Installation > Fixed Scala Installation 2.10.5.(bundled)`

 <small>
 More detailed, tutorial-style instructions, with all the prerequisites are in chapter 3 of the book.
 </small>

 * **From the terminal** (interactive mode):  
 <small>
 Select the only possible option (1) and answer subsequent questions.
 </small>

```sh
mvn archetype:generate \
  -DarchetypeCatalog=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml \
  -DarchetypeRepository=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master
```


 * **From the terminal or a shell script** (batch mode):  
 <small>
 Don't forget to change the parameter values in the last line.
 </small>

```sh
mvn archetype:generate -B \
    -DarchetypeCatalog=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml \
    -DarchetypeRepository=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master \
    -DarchetypeGroupId=org.sparkinaction \
    -DarchetypeArtifactId=scala-archetype-sparkinaction \
    -DarchetypeVersion=0.11 \
    -DgroupId=com.company -DartifactId=project -Dversion=0.1-SNAPSHOT -Dpackage=com.company
```


 * ***Generated project example usage*** *(run* `mvn scala:help` *for the full list of commands):*

You can run the generated project by simply doing `Shift+Alt+x s` (while positioned in `App.scala`), which is the shortcut for `Run As > Scala Application`.

You can also run it from the command line or from Eclipse Maven _Run configuration_ with these _goals_:

```sh
mvn scala:compile
mvn scala:run -DmainClass=com.company.App
```

Thank you for purchasing the book :)
