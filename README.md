# Project Template

Java / Maven project shell with useful default settings / conventions.

## About 

Fork this project to obtain a good head start and hands on instructions for a useful project layout:

 * Project structure compliant to Maven conventions
 * README template
 * Maven gems enabled:
   * Test pass as build requirement
   * Compile to standalone JAR (all dependencies included)
 * Preconfigured ```.gitignore```

## Usage

Follow below instructions to get your project ready for check-in.

### File Setup

 * Fork / clone this repo
 * Remove the ```.git``` folder
 * Remove this ```README.md``` file
 * Rename the ```README-template.md``` file to ```README.md```

### Maven / Tests

#### GroupId / ArtifactId


 >  Write down your personal ```artifactId``` and ```groupId```:  
```groupid``` should be two words, separated by ```.``` and refer to your name, company or institution. Should be all lowercase and should start with with top level domain. If in doubt, use ```lastname.firstname``` or ```github.yourgithubname```.  
```artifactId``` should be one word, all lowercase and describe your project, e.g. ```satsolver```

 * Edit the ```pom.xml```
   * Update these fields:  
```xml
    <groupId>yourgroupiddomain.yourgroupid</groupId>
    <artifactId>yourartifactid</artifactId>
    <name>yourartifactid</name>
```
   * If you have a main class, register it, otherwise remove the entire plugin. (There are two occurences, one for JARs, one for direct program execution):
```
<mainClass>yourgroupiddomain.yourgroupidname.yourartifactid.Launcher</mainClass>
```
   * Change the final output name (the file name your artifact will have when built). Should be the same as *yourartifactid* but with CamelCase writing.  
(e.g. if your artifactid is ```satsolver``` your output.name should be ```SatSolver```)  
```xml
<output.name>YourArtifactId</output.name>
```

 * Update the folder structure:
   * Update group / groupdomain / artifactid in the source directory structure: ```src/main/java/yourgroupiddomain/yourgroupid/yourartifactid```.  
   * Update group / groupdomain / artifactid in the test directory structure: ```src/test/java/yourgroupiddomain/yourgroupid/yourartifactid```.  
 * Add your code to ```src/main/java/yourgroupiddomain/yourgroupid/yourartifactid```
   * Set the class package statement in your classes to ```yourgroupiddomain.yourgroupid.yourartifactid```

#### Testing

 * For every class in the src folder, create a test class in ```src/test/java/yourgroupiddomain/yourgroupid/yourartifactid```.  
(e.g. for ```src/main/java/yourgroupiddomain/yourgroupid/yourartifactid/Foo.java```, create a test class ```src/test/java/yourgroupiddomain/yourgroupid/yourartifactid/FooTest.java```)
   * Fill the test class with this stub code (then write actual tests)

```java
import org.junit.Test;

public class FooTest {
    @Test
    public void myFirstUnitTest() {
	assertSame("Potatoes", "Potatoes");
    }

    @Test
    public void mySecondUnitTest() {
	assertSame("Squares", "Squares");
    }
}
```

### Instructions / Building

 * Replace all ```UPPERCASE``` instructions in the new ```README.md```.
 * Build your project with ```mvn clean package```. If you defined a launcher class you can run your project with ```mvn clean exec:java```.
 * Create a new project on GitHub, publish your project.

## Legal / Pull Requests

 * Author: Maximilian Schiedermeier
 * Github: [Kartoffelquadrad](https://github.com/kartoffelquadrat)
 * Webpage: https://www.cs.mcgill.ca/~mschie3
 * License: [MIT](https://opensource.org/licenses/MIT)

