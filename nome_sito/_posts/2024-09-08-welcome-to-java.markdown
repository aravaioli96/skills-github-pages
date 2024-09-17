---
layout: post
title:  "Java documentation"
date:   2024-09-05 15:20:53 +0200
categories: jekyll update
---
# JAVA
## NAME
java - launch a Java application

## SYNOPSIS
To launch a class file:

`java [options] mainclass [args ...]`

To launch the main class in a JAR file:

`java [options] -jar jarfile [args ...]`

To launch the main class in a module:

`java [options] -m module[/mainclass] [args ...]`

or

`java [options] --module module[/mainclass] [args ...]`

To launch a single source-file program:

`java [options] source-file [args ...]`

options
- Optional: Specifies command-line options separated by spaces. See Overview of Java Options for a description of available options.

mainclass
- Specifies the name of the class to be launched. Command-line entries following classname are the arguments for the main method.

-jar jarfile
- Executes a program encapsulated in a JAR file. The jarfile argument is the name of a JAR file with a manifest that contains a line in the form Main-Class:classname that defines the class with the public static void main(String[] args) method that serves as your application's starting point. When you use -jar, the specified JAR file is the source of all user classes, and other class path settings are ignored. If you're using JAR files, then see jar.

-m or --module module[/mainclass]
- Executes the main class in a module specified by mainclass if it is given, or, if it is not given, the value in the module. In other words, mainclass can be used when it is not specified by the module, or to override the value when it is specified.

source-file
- Only used to launch a single source-file program. Specifies the source file that contains the main class when using source-file mode. See Using Source-File Mode to Launch Single-File Source-Code Programs

args ...
- Optional: Arguments following mainclass, source-file, -jar jarfile, and -m or --module module/mainclass are passed as arguments to the main class.

## DESCRIPTION
The java command starts a Java application. It does this by starting the Java Virtual Machine (JVM), loading the specified class, and calling that class's main() method. The method must be declared public and static, it must not return any value, and it must accept a String array as a parameter. 