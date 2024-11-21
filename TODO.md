## TODO NEEDED TO KEEP ME ON TRACK

*[ ] Configure and setup android nanohttpd package build with component selection*  
- [X] Upgrade to Java 11, AGP 7.0.1, Gradel 7.0.2 and setup common.gradle to set optional build sdk configs.
- [X] Get a working AAR build for one of the sub projects modules.
- [X] Cleanup and make a clear separation of module/project dependencies and build specific dependencies.
- [X] Review options to upgrade to Java SDK 17 and realize multiple compile errors in the code hold this off.
- [X] Other cleanup and cherry-pick of commits available from the google source that are not available in master/upstream.
- [X] Review the Android.bp intended for AOSP system builds of nanohttpd for source sets to build app-scoped-private library
- [X] As part of getting a working AAR build reviewed the difference between AndroidLibrary and AndroidApplication build plugins
- [X] As part of getting a workking AAR build reviewed the plugin configurations and namespacing and app id's 
- [X] Cleanup multiple deprecation lint warnings, and cleared all deprecations for the Android AAR build
- [X] Identified the internal deprecations and reviewed the code to understand the correct use, and deprecations w/ java platform build can be ignored.
- [X] Identified and cleared other deprecations due to Gradle upgrade, and should be good to Gradle 8.9.
- [X] Identified the codebase is compatible with maximum of JDK 11, and AGP 7 is only AndroidGradlePlug version supporting, w/ max Gradle version of 7.0.2
- [X] Currently using a copy of the source directory, need to setup the sourceset to pattern match a source directory outside of it's own module directory.
- [] Once source set works, move the module directory to root of project and enforce compilation with AAR and JAR w/ LibraryDesugaringEnabled
- [] Rollup into two separate packages, one using the desugared jars and another with AAR, and keep LIB folder the not rolled up jars/aars
- [] Transform the Java Source Files Package Namespaces during compilation to prepend the package namespace and ensure no namespace collisions (Android)
- [] Add something to the read me explaining what the Android build is why it is App Specific and not AOSP System and provide example run.
- [] Set the source set to pull in and build all of the subprojects/modules into the android library, but make easy to comment out.
- [] Actually test it in an Android App once??? 
- [] Figure out why the libraries don't work, try the JAR files vs the AAR files vs the PKG files, get it working.
- [] Review the requirements for .java files to compile under JDK 17 without issues and start upgrading modules one by one.
- [] Since the project has both a Maven build and a gradle build, and maven is currently working, make sure Maven tags along for the ride.
- [] Since gradle is not generating the documentation use gradle exec task to trigger maven "generatMavenSite" to generate the docs.
- [] Add the Gradle Release plugin then align the release information in the Maven release files and Gradle, add the MavenPublish plugin to Gradle
- [] Test publishing to Maven with another simple library. Then publish. ( I think )

*[ ]*  
*[ ]*  
*[ ]*  