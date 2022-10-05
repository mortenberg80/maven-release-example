# maven-release-example
Example project to show how to release major, minor or patch versions with maven-release-plugin

This example uses profiles to change how we run the maven-release-plugin, and we use the maven-build-helper-plugin to find out what the next version is.

Major:
`mvn -B initialize release:clean release:prepare release:perform -DdryRun -Pmajor`

Release minor:
`mvn -B initialize release:clean release:prepare release:perform -DdryRun -Pminor`

Relase patch (default):
`mvn -B initialize release:clean release:prepare release:perform -DdryRun`

## Contributions

