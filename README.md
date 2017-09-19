# Introduction

This is an example hello app application on how to bundle a JRE into the application. 

The project folder will be structured in this manner:

```
+ hello-bundled-app
	+ src
		+ main
			+ java
				+ HelloApp.java
	+ bin
		+ run.bat.txt
	+ releases	# this will be generated only if you run the mvn clean package
		+ hello-bundled-app-VERSION
			+ bin
				+ run.bat.txt
			+ lib
				+ hello-bundled-app-VERSION.jar
	pom.xml
```


# Pre-requisite

1. Maven 3.3.9

# Instruction

You can either do a check out of this repository or you can click on the download button to download the project file.
After which, run the following command:

`mvn clean build`

After you see the `BUILD SUCCESS`, go to the folder `release` and you will see the following structure.

```
+ hello-bundled-app-0.0.1-SNAPSHOT
	+ lib
		+ hello-bundled-app-0.0.1-SNAPSHOT.jar
	+ bin
		+ run.bat # click this to run the Java application
```

Remember to put the Java `jre` folder into the `hello-bundled-app-0.0.1-SNAPSHOT` folder. This example does not bundle `jre` due to its large size. Remember to rename the `run.bat.txt` to `run.bat`.