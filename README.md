# maven-release-example
Example project to show how to release major, minor or patch versions with maven-release-plugin.

I couldn't find an easy way to tell the release-plugin if I wanted to increment major, minor or patch-part of the version, so I made this maven-setup based on some blog posts I read.

This example uses profiles to change how we run the maven-release-plugin, and we use the maven-build-helper-plugin to find out what the next version is.

(Remove dryRun-flag doing a real release).

Major:
`mvn -B initialize release:clean release:prepare release:perform -DdryRun -Pmajor`

Release minor:
`mvn -B initialize release:clean release:prepare release:perform -DdryRun -Pminor`

Relase patch (default):
`mvn -B initialize release:clean release:prepare release:perform -DdryRun`


Inspiration to this setup was from the following blog posts / answers:
* https://thihenos.medium.com/maven-release-plugin-a-simple-example-of-package-management-9926506acfb9
* https://itecnote.com/tecnote/r-maven-release-next-development-version-in-batch-mode/
