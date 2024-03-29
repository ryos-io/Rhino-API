# Rhino Performance Assessment Platform (PAP)

> **_NOTE:_** We are just getting started with the platform. Feel free to join Rhino PAP community on [Gitter](https://gitter.im/ryos-io/Rhino)

Rhino PAP is a load and performance testing platform, to run automated and distributed load tests against web services,
to assess the performance characteristics of the web and cloud services. Rhino PAP consists of several components, like Management UI, Scheduler,
Archiver, etc. which enable developers:

- to run automated and isolated load and performance tests against web services,
- to collect and visualize metrics on Rhino Management UI,
- to drill down into performance measurements to detect the bottlenecks,
- to determine the performance regression after each run,
- to report load and performance tests with their setup together like type of instances, number of instances, etc.
- to make load and performance test results comparable,
- to archive the test results for long term analysis.

### Architecture Overview from 30K feet

> **_NOTE:_** This is an early draft of architecture design.

<p align="center">
  <img src="https://github.com/ryos-io/Rhino-PAP/blob/master/system_arch.png"  width="600"/>
</p>

## Questions/Contributions?

Feel free to fork the project and make contributions in terms of Pull Requests. For bigger
proposals, architectural discussions and bug reports, use the Github's issue tracker.

## Rhino Scheduler

Task api of the Rhino Load Testing Platform.

Used technologies:

- Spring
- Kotlin

### Build Management

- `./gradlew tasks`: Show available tasks
- `./gradlew bootRun`: Start Spring-Boot server
- `./gradlew clean build`: compile
- `./gradlew test`: test

### Development

For local development activate the Spring `local` profile via JVM parameter:

`-Dspring.profiles.active=local`

This allows you to access protected APIs with preconfigured users
via [Basic Auth](https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication):
`curl -v --user "rhino:rhino" http://localhost:8080/greeting`

### Documentation

- [Swagger REST-API documentation](http://localhost:8080/swagger-ui.html)
  - Server needs to be running
