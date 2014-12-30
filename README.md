lwjgl-packaging
===============

### Goal ###

A `gradle.build` script demonstrating the packaging of an LWJGL-dependent project as either a standalone jar or a Windows executable.

The "Space Invaders" demo LWJGL program is included so as to provide a full-fledged sample.

### Tasks ###

The following Gradle tasks are available:

* `run`: build an application jar and run it. Mostly useful to ensure everything is in place.
* `myCapsule`: build a standalone jar: `build/libs/[ProjectName]-capsule.jar`.
* `launch4j`: build a Windows executable: `build/launch4j/[ProjectName].exe`. 

Both the jar and executable can be launched "as is". In particular, the Capsule framework takes care of setting up `java.library.path` so as to link to the native LWJGL libraries.

### Eclipse Setup ###

To test this under Eclipse:

* Install [Eclipse Gradle tooling](https://github.com/spring-projects/eclipse-integration-gradle/).
* "`Import as general project`" from `Git Repositories` view.
* Right click on project, "`Configure > Convert to Gradle Project`".
* Try "`Ctrl+Alt+Shift+R` > `run`" to ensure that the project is properly set up.

### Acknowledgements ###

This script builds upon the [Capsule](https://github.com/puniverse/capsule), [gradle-capsule-plugin](https://github.com/danthegoodman/gradle-capsule-plugin), [gradle-natives](https://github.com/cjstehno/gradle-natives) and [launch4j](http://launch4j.sourceforge.net/) tools.

It ships with the "Space Invader" [LWJGL example game](http://wiki.lwjgl.org/index.php?title=Space_Invaders_Example_Game), on which I do not claim any right.

The following articles were used as starting points: [Going Native with Gradle](https://github.com/cjstehno/coffeaelectronica/wiki/Going-Native-with-Gradle), [An Opinionated Guide to Modern Java, Part 2](http://blog.paralleluniverse.co/2014/05/08/modern-java-pt2/).