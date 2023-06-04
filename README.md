Apache Tomcat11 Config
----------------------

This project takes apache tomcat distribution from maven central, extracts configuration needed items and jars not otherwise released to maven central and repackages.

For more information on tomcat, please see [tomcat](https://github.com/apache/tomcat)

# Motivation #

Apache tomcat does not distribute the bootstrap to maven central separately not does it deliver just the configuration.  This project aims to solve that by cutting down the distribution into pieces that cannot otherwise be procured individually only.
This is helpful for situations where one needs to review the configuration updates but doesn't need or is unable to retrieve the entire tomcat distribution package.  In such a case, this is more of a review solution and the remainder of tomcat can
otherwise be constructed directly from central binaries as needed.

# Current Retained Contents #

- bootstrap.jar
- tomcat-native.tar.gz
- All sh files
- All xml files
- Catalina.policy
- catalina.properties
- All xsd files
- LICENSE
- NOTICE
- RELEASE-NOTES
- RUNNING.txt

# Currently Excludes following items some might find useful #

- All libs - use maven directly to pickup or just use tomcat distribution itself
- All webapps
- All windows bat files, use git bash and just work like *nix
- Doesn't include logging.properties - Use tomcat-slf4j-logback for better solution for tomcat-juli
