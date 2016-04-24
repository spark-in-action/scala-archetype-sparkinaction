### Archetype to scaffold projects for the ___Spark in Action___ book

<img src="http://www.manning.com/bonaci/bonaci_cover150.jpg"
 alt="The book cover" title="Spark in Action cover page" align="right" />  
However unlikely, you maybe still haven't purchased the book, so here's the link: [Spark in Action](http://t.co/8dVXGkfits). Use the coupon code `bonaci39` for 39% off.
BTW, you don't need to try `bonaci100`, it won't work :)  
Thanks
<br><br><br><br>


#### Eclipse:
1. `File > New > Project... > Maven > Maven Project`  
2. Click `Next` on the first screen of the _New project_ wizard  
3. Select `Configure... > Add Remote Catalog...`  
4. Enter the following URL in the `Catalog file` field: https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml  
      Enter `Spark in Action` in the `Description` field  
5. After you close the dialog, choose the `Spark in Action` catalog in the `Catalog` dropdown list
6. In the next dialog simply enter you project details and confirm with `Finish`. In case of problems with this step (such as IDE not being able to locate the POM file) try to use a different URL in the step 4: https://raw.githubusercontent.com/spark-in-action/scala-archetype-sparkinaction/master/archetype-catalog.xml
7. Once the new projects generates change the Scala version to 2.10.5:
      Right click on the generated project and select:
      `Scala > Set the Scala Installation > Fixed Scala Installation 2.10.5.(bundled)`

#### IntelliJ IDEA:
1. `File > New > Project... > Maven`
2. Select `Create from Archetype` and click on `Add Archetype` button
3. Fill-in the `Add archetype` dialog:
   * `GroupId`:    `org.sparkinaction`
   * `ArtifactId`: `scala-archetype-sparkinaction`
   * `Version`:    `0.13`
   * `Repository`: `https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master`
   And confirm with OK.
4. In the list of archetypes, find `org.sparkinaction`, the one that you just added, expand it and select the archetype with the version and click `Next`
5. Enter parameters for your new project:
   * `GroupId`:    `org.sia`
   * `ArtifactId`: `chapter-03-app`
   * `Version`:    `0.1-SNAPSHOT`
6. In the next screen, just confirm with `Next`
7. In the last screen, enter `Chapter03App` as the project name and click `Finish`


 <small>
 More detailed, tutorial-style instructions, with all the prerequisites are in chapter 3 of the book.
 </small>

 #### From the terminal (interactive mode):
 <small>
 Select the only possible option (1) and answer subsequent questions.
 </small>

```sh
mvn archetype:generate \
  -DarchetypeCatalog=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml \
  -DarchetypeRepository=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master
```


 #### From the terminal or a shell script (batch mode):
 <small>
 Don't forget to change the parameter values in the last line.
 </small>

```sh
mvn archetype:generate -B \
    -DarchetypeCatalog=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master/archetype-catalog.xml \
    -DarchetypeRepository=https://github.com/spark-in-action/scala-archetype-sparkinaction/raw/master \
    -DarchetypeGroupId=org.sparkinaction \
    -DarchetypeArtifactId=scala-archetype-sparkinaction \
    -DarchetypeVersion=0.13 \
    -DgroupId=com.sia -DartifactId=chapter03App -Dversion=0.1-SNAPSHOT -Dpackage=com.sia
```


#### Generated project example usage
*(run `mvn scala:help` for the full list of commands)*

In Eclipse, you can run the generated project by simply doing `Shift+Alt+x s` (while positioned in `App.scala`), which is the shortcut for `Run As > Scala Application`.

You can also run it from the command line or from Eclipse Maven _Run configuration_ with these _goals_ (adjust main class if needed):

```sh
mvn scala:compile
mvn scala:run -DmainClass=com.sia.Chapter03App
```

If you choose to purchase the book, thank you :)
