-  [POM Syntax](http://maven.apache.org/pom.html)
-  [Sonatype Nexus](http://www.sonatype.org/nexus/): self-hosting a Maven repository

### Commands

General command structure
```shell
    mvn -P<profile> <command> <scope>
```
Simple stuff
```shell
    mvn help
    mvn compile
    mvn validate
    mvn verify
    mvn test
    mvn clean 
    mvn clean package
    mvn clean install
    mvn clean deploy
```
#### Artifacts
```shell
    mvn archetype:create                    # Create pom.xml

    mvn archetype:create -DgroupId=<group> \     # Create JAR
                         -DartifactId=<new id>

    mvn archetype:create -DgroupId=<group> \     # Create WAR
                         -DartifactId=<new id> \
                         -DarchetypeArtifactId=maven-archetype-webapp

    mvn install:install-file <params>            # Install dependencies
```
#### Releasing
```shell
    mvn deploy:deploy-file <params ...>

    # Useful release options:
    #
    #    -P <profile>
    #    -Dusername=<user>
    #    -Dpassword=<password>
    #
    mvn release:prepare
    mvn release:clean
    mvn release:perform
```
#### Tomcat Plugin
```shell
    mvn tomcat:deploy
    mvn tomcat:redeploy
    mvn tomcat:undeploy
    mvn tomcat:stop
    mvn tomcat:start
```
#### IDE integration
```shell
    mvn -Declipse.workspace=<path> eclipse:add-maven-repo
    mvn eclipse:eclipse
```
