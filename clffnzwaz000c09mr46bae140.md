---
title: "Maven Commands every developer needs to know"
seoTitle: "Common and Important Maven commands every developer should know"
seoDescription: "Maven Cheatsheet - Common and important maven commands every software developer should know"
datePublished: Sun Mar 19 2023 17:21:19 GMT+0000 (Coordinated Universal Time)
cuid: clffnzwaz000c09mr46bae140
slug: maven-commands-every-developer-needs-to-know
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679245547761/336c9d4c-e797-428c-9b57-04a968b8745b.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679246410167/8c0bc2bc-e114-4607-bad4-53fdd3a0025d.jpeg
tags: java, maven, cheatsheet, springboot, commands

---

Below are some of the important Maven commands we need to know in software development.

### Compile source code

```bash
mvn compile
```

### Clean old build files

```bash
mvn clean
```

### Deploy the JAR/WAR files in local

```bash
mvn install
```

### Deploy the JAR/WAR files in remote

```bash
mvn deploy
```

### Run the tests

```bash
mvn test
```

### Check the maven dependency tree

```bash
mvn dependency:tree
```

### Create a JAR/WAR package

```bash
mvn package
```

### Skip the tests and clean install

```bash
mvn clean install -DskipTests=true
```

### Run spring boot app

```bash
mvn spring-boot:run
```

### Setup project for Intellij IDEA

```bash
mvn idea:idea
```

### Test with multiple params

```bash
mvn test -DskipTests=true -DsuiteXmlFile=<xml-file-path> -DapplicationHostname=<host-name> -DapplicationProtocol=<protocol-name> -DapplicationPort=<port-number>
```