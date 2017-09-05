# heroku-buildpack-custom-jvm

This build pack only installs a user provided JVM. It does not assume anything about the application deployment, so it probably makes sense to use this build pack in conjunction with other build packs that handle the application deployment.

Configure the URL that points to the location of the JDK as a Heroku Configuration Variable named *JDK_URL_1_[X]*, where [X] is the desired Java version (6, 7, 8 or 9).

The Java version (ex: "1.8") is determined by a property named *java.runtime.version* defined inside a *system.properties* file that should exist in the root of your application directory. Alternatively it may be defined in a Heroku Configuration Variable named *DEFAULT_JDK_VERSION*.

