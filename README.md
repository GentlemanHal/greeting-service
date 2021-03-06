# TODO: Service Name

TODO: Add a simple description of the service.

## Prerequisites

You'll need the following tools installed to run locally:

* [Java](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

The following **optional** tools may also be installed depending on your use cases:

* [Docker](https://www.docker.com/)

### Java

This project requires at least Java 8.

### Docker

This is only required if you plan on running the service as a Docker container.

## Development

### Getting started

This project includes the [Gradle Wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html) which will
automatically downloaded and install the correct version of Gradle. Gradle will automatically download all project
dependencies on demand, so there are no specific commands to run.

### Running locally

To run a dev server locally use `./gradlew run`, this will start the server using the configuration in
`src/config/app_config.yml`.

### Debugging

The Gradle build file adds the JVM argument to allow a remote debugger to be attached on port `5006`

### Debugging in Intellij

To run the project in debug mode directly from Intellij, you need to edit the run configuration and add the following program arguments:
`server src/config/app_config.yml`

### Testing

To run all the tests use `./gradlew test`

#### Unit tests

To run just the unit tests use `./gradlew unitTest`

#### Integration tests

To run just the integration tests use `./gradlew integrationTest`

### Checking for dependency updates

To check if any dependencies are out of date use `./gradlew dependencyUpdates` 

## Releasing

### Building a jar

To create a fat jar containing all the dependencies as well as the service code use `./gradlew shadowJar`

### Docker

To create a Docker image use `./gradlew docker`
