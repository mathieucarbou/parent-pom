Parent POM

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

 - [Version 2](https://code.mathieu.photography/parent-pom/reports/2/index.html)
 - [Version 3](https://code.mathieu.photography/parent-pom/reports/3/index.html)

[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/a20ded47d7533f559376e3f026b94f84 "githalytics.com")](http://githalytics.com/mycila/pom)

## Releasing ##

```
mvn release:prepare
mvn release:perform -Darguments="-Dgpg.keyname=EDEA921A"
```
