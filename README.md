# Parent POM

 - __Build Status:__ [![Build Status](https://travis-ci.com/mathieucarbou/parent-pom.png?branch=master)](https://travis-ci.com/mathieucarbou/parent-pom)
 - __Issues:__ https://github.com/mathieucarbou/parent-pom/issues

## Maven ##

 __Releases__

Available in Maven Central Repository: http://repo1.maven.org/maven2/com/mycila/pom/

 __Snapshots__

Available in OSS Repository:  https://oss.sonatype.org/content/repositories/snapshots/com/mycila/pom/

__Declaration__

    <parent>
        <groupId>com.mycila</groupId>
        <artifactId>pom</artifactId>
        <version>X</version>
    </parent>

## Maven Sites ##

- - [Version 4](https://mathieucarbou.github.io/index.html)
- - [Version 3](https://code.mathieu.photography/parent-pom/reports/3/index.html)
- - [Version 2](https://code.mathieu.photography/parent-pom/reports/2/index.html)

[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/a20ded47d7533f559376e3f026b94f84 "githalytics.com")](http://githalytics.com/mycila/pom)

## Releasing ##

```
mvn release:prepare
mvn release:perform -Darguments="-Dgpg.keyname=EDEA921A"
```

If some aspects of your project are non-standard, you may override the defaults via either `mvn -Dsome.property` or declaring them in your pom:
```xml
<properties>
    <!-- change this if you deploy to github enterprise instead -->
    <parameter.site.domain>github.com</parameter.site.domain>
    <!-- change this if your github org does not match what this parent pom is in -->
    <parameter.site.subdomain>mathieucarbou</parameter.site.subdomain>
    <!-- change this if your project's repository is not named the same as the artifactId -->
    <parameter.site.root.uri>${project.artifactId}</parameter.site.root.uri>
    <!-- set to true to disable site publishing altogether, bound to site phase by default -->
    <parameter.site.github.deploy.skip>false</parameter.site.github.deploy.skip>
    <!-- set to false to enable vanilla site deploy plugin -->
    <parameter.site.maven.deploy.skip>true</parameter.site.maven.deploy.skip>
</properties>
```

First create a [personal access token](https://github.com/settings/tokens/) with the following permissions:
* public_repo
* read:enterprise
* read:org
* read:user
* user:email

and a section in your ~/.m2/settings.xml like:

```xml
    <server>
      <id>github.com</id>
      <password>your-token-probably-starting-with 'ghp_'</password>
    </server>
```

Now you may run:
```
mvn site site-deploy
```

If you would like to preview a single-module site, you may run:
```sh
mvn org.apache.maven.plugins:maven-site-plugin:run
```
