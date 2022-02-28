# Instructions
### Create parent project using following command:
```
mvn archetype:generate -DgroupId=com.lotuslake.app -DartifactId=parent-project -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```
- update parent-project/pom.xml to add <packaging>pom</packaging>
- update maven.compiler.source and maven.compiler.target to match the JDK version that you currently have on your machine. It could either be 11 or 17 in your case.

### Create children projects using following command:
```
mvn archetype:generate -DgroupId=com.lotuslake.app -DartifactId=core -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
mvn archetype:generate -DgroupId=com.lotuslake.app -DartifactId=service -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
mvn archetype:generate -DgroupId=com.lotuslake.app -DartifactId=webapp -DarchetypeArtifactId=maven-archetype-webapp -DarchetypeVersion=1.4 -DinteractiveMode=false
```
- update each of the child projects pom.xml to remove <properties>...</properties>, <dependencies>...</dependencies> and <build>...</build>
