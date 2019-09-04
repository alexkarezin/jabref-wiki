## Setting up Eclipse for developing JabRef 5.x with Java 11


1. Run gradlew eclipse
2. Go to build path  -> Libraries
3.  Move all test related libs to classpath
4. Move jmh to classpath as well
5. Go to Source -> Mark src/jmh as test folder
6. Go to Module dependencies 
6.1. Select `org.controlsfx.controls` in the list
6.2. Add export and opens entry  for `impl.org.controlsfx.autocompletion`, `impl.org.controlsfx.skin` and `org.controlsfx.control.textfield`  to `org.jabref`
6.3. Select `javafx.controls` add epxorts and opens entry for `com.sun.javafx.scene.control`  to `org.jabref`

JPMS options should look like this:
```
--add-exports org.controlsfx.controls/impl.org.controlsfx.autocompletion=org.jabref --add-exports org.controlsfx.controls/impl.org.controlsfx.skin=org.jabref --add-exports org.controlsfx.controls/org.controlsfx.control.textfield=org.jabref --add-opens org.controlsfx.controls/impl.org.controlsfx.autocompletion=org.jabref --add-opens org.controlsfx.controls/impl.org.controlsfx.skin=org.jabref --add-opens org.controlsfx.controls/org.controlsfx.control.textfield=org.jabref --add-exports javafx.controls/com.sun.javafx.scene.control=org.jabref --add-opens javafx.controls/com.sun.javafx.scene.control=org.jabref
```

7. Create a run/debug configuration for main class `org.jabref.JabRefLauncher` 
8. In the arguments tab enter this for VM arguments.
```
-Djabref.theme.css --patch-module test=fastparse_2.12-1.0.0.jar --patch-module test2=fastparse-utils_2.12-1.0.0.jar --patch-module test3=sourcecode_2.12-0.1.4.jar --patch-module org.jabref=build\resources\main --add-exports javafx.controls/com.sun.javafx.scene.control=org.jabref --add-exports org.controlsfx.controls/impl.org.controlsfx.skin=org.jabref --add-opens javafx.controls/javafx.scene.control=org.jabref --add-opens org.controlsfx.controls/org.controlsfx.control.textfield=org.jabref --add-exports javafx.graphics/com.sun.javafx.scene=org.controlsfx.controls --add-exports javafx.graphics/com.sun.javafx.scene.traversal=org.controlsfx.controls --add-exports javafx.graphics/com.sun.javafx.css=org.controlsfx.controls --add-exports javafx.controls/com.sun.javafx.scene.control.behavior=org.controlsfx.controls --add-exports javafx.controls/com.sun.javafx.scene.control=org.controlsfx.controls --add-exports javafx.controls/com.sun.javafx.scene.control.inputmap=org.controlsfx.controls --add-exports javafx.base/com.sun.javafx.event=org.controlsfx.controls --add-exports javafx.base/com.sun.javafx.collections=org.controlsfx.controls --add-exports javafx.base/com.sun.javafx.runtime=org.controlsfx.controls --add-exports javafx.web/com.sun.webkit=org.controlsfx.controls --add-exports javafx.graphics/com.sun.javafx.css=org.controlsfx.controls --add-opens javafx.controls/javafx.scene.control.skin=org.controlsfx.controls --add-opens javafx.graphics/javafx.scene=org.controlsfx.controls"
```
