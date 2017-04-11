# Documentation

Based on 'Dcoumentation - PHP' at https://docs.openshift.org/latest/using_images/s2i_images/php.html

## Source-to-Image (S2I)

OpenShift Origin provides S2I enabled PHP images for building and running PHP applications. The PHP S2I builder image assembles your application source with any required dependencies to create a new image containing your PHP application. This resulting image can be run either by OpenShift Origin or by Docker.

NOTE: S2I is prefered over a Docker file, because by restricting build operations as an S2I facilitates instead of allowing arbitrary actions, as a Dockerfile would allow, the PaaS operator can avoid accidental or intentional abuses of the build system.

## PHP

Currently, OpenShift Origin provides version ***5.5*** and ***5.6*** of PHP.

## Image

Images can be referenced in image streams.

## Image Stream

An image stream comprises any number of container images identified by tags. It presents a single virtual view of related images, similar to a Docker image repository. 

See https://docs.openshift.org/latest/dev_guide/managing_images.html#dev-guide-managing-images

An image stream in OpenShift Origin comprises zero or more container images identified by tags.

## Image Stream Definitions

The PHP image supports a number of environment variables which can be set to control the configuration and behavior of the PHP runtime.

To set these environment variables as part of your image, you can place them into a .s2i/environment file inside your source code repository.

See also https://docs.openshift.org/latest/dev_guide/builds/build_strategies.html#environment-files

Example .s2i/environment :

```javascript
to do: provide an example
```

If you provide a .s2i/environment file in your source repository, S2I reads this file during the build. This allows customization of the build behavior as the assemble script may use these variables.

## Quick Start Templates

See https://docs.openshift.org/latest/dev_guide/app_tutorials/quickstarts.html

A quickstart is a basic example of an application running on OpenShift Origin. Quickstarts come in a variety of languages and frameworks, and are defined in a template, which is constructed from a set of services, build configurations, and deployment configurations. 

## Web Framework Quickstart Templates

These quickstarts provide a basic application of the indicated framework and language:

- CakePHP: a PHP web framework (includes a MySQL database)

- Dancer: a Perl web framework (includes a MySQL database)

- Django: a Python web framework (includes a PostgreSQL database)

- NodeJS: a NodeJS web application (includes a MongoDB database)

- Rails: a Ruby web framework (includes a PostgreSQL database)

