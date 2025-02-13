GitHub Example
===================

* goal  
  * simple json client

## How to run ?
* compile it -- via --
  * Gradle
    * `gradle`
      * generate `build/github`
  * Maven
    * `mvn clean compile`
      * generate `target/github`
      * Problems:
        * Problem1: "[ERROR] jdk [ version='1.8' ]"
          * Solution: Create  "~/.m2/toolchains.xml" / contain 2 entries of jdk
            ```
            <?xml version="1.0" encoding="UTF-8"?>
            <toolchains>
                <!-- JDK 8 Toolchain -->
                <toolchain>
                    <type>jdk</type>
                    <provides>
                        <version>1.8</version>
                        <vendor>oracle</vendor>
                    </provides>
                    <configuration>
                        <jdkHome>/path/to/your/jdk8</jdkHome>
                    </configuration>
                </toolchain>
              
                <!-- JDK 11 Toolchain -->
                <toolchain>
                    <type>jdk</type>
                    <provides>
                        <version>11</version>
                        <vendor>oracle</vendor>
                    </provides>
                    <configuration>
                        <jdkHome>/path/to/your/jdk11</jdkHome>
                    </configuration>
                </toolchain>
            </toolchains>

            ```
        * Problem2: "Failed to read artifact descriptor for com.gradle:develocity-maven-extension:jar:1.23.1"
          * Attempt1: `rm -rf .m2/repository/com/gradle/develocity-maven-extension`
          * Attempt2: comment it
          * Note: Where does it come from? 
          * Solution: TODO:
* run it
  * Attempt1: `java -cp target/classes example.github.GitHubExample`
  * Attempt2: `mvn exec:java -Dexec.mainClass="example.github.GitHubExample"`
    * Problems:
      * Problem1: " Plugin not found in any plugin repository"
  * Solution: TODO:
