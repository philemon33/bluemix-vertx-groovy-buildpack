# Bluemix-compatible Buildpack: Vert.x

This is a buildpack for [Vert.x](http://vertx.io/) apps, used to deploy vert.x apps in IBM Bluemix. An example app can be found [here](https://github.com/mthenw/vertx-sample).

Currently it uses the following versions:

* JDK **1.7**
* Vert.x **2.1.4**

You can vary those versions by adjusting the OPENJDK7_URL and VERTX_URL constants in the bin/compile file

## Usage

This buildpack assumes that there are at least one file in repository:

* ```server.groovy``` - file launched by default (of course this can be overrided by Procfile)

Example usage:

    $ ls
    server.groovy

    $ cf push myapp -b https://github.com/philemon33/bluemix-vertx-buildpack.git


This buildpack is based on  [mthenw/heroku-buildpack-vertx.git](https://github.com/mthenw/heroku-buildpack-vertx.git), which is itself based on [tomaslin/heroku-buildpack-vertx-jdk7](https://github.com/tomaslin/heroku-buildpack-vertx-jdk7).

## License

MIT
