[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.rabbitmq/tracer/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.rabbitmq/tracer)

## RabbitMQ Tracer

This repository contains source code of the [RabbitMQ AMQP protocol analyzer](https://www.rabbitmq.com/java-tools.html#tracer).
The client is maintained by the [RabbitMQ team at Pivotal](http://github.com/rabbitmq/).

## Installing

This is a standalone tool that is distributed in binary form using
[Bintray](https://bintray.com/rabbitmq/java-tools/tracer) or
[GitHub releases](https://github.com/rabbitmq/rabbitmq-tracer/releases)
and as a JAR file on Maven Central (see above).

## Using

Use `runtracer` (for UNIX-like systems) or `runtracer.bat` (for Windows)
to run the tracer, e.g.:

```
runtracer listenPort connectHost connectPort
```

The program accepts parameters:

 * `listenPort`: port to listen for incoming AMQP connections on - defaults to 5673.
 * `connectHost`: hostname to use when making an outbound connection in response to an incoming connection - defaults to localhost.
 * `connectPort`: port number to use when making an outbound connection - defaults to 5672.

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for an overview of the development process.

## Building

To build the JAR file:

```
mvn clean package
```

Files are then in the `target` directory.

To build the JAR file, source and binary distributions:

```
mvn clean package -P assemblies
```

## License

This package, the RabbitMQ AMQP protocol analyzer library, is triple-licensed under
the Mozilla Public License 1.1 ("MPL"), the GNU General Public License
version 2 ("GPL") and the Apache License version 2 ("ASL").
