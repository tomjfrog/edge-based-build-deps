# Example of Pulling Build Dependencies from a JFrog Edge and Publishing to a "Full" JPD

This example build process, defined in `./.github/workflows/build-and-deploy.yml` demonstrates a possible approach to using a JFrog Edge as the source of build dependencies.

Refer to the "Actions" tab for the syntax and results of the example build.

The relevant elements to note are:
1. There are *two* different connections that are configured for the JF CLI in the task runner.  One is the default connection that the `@actions/setup-jfrog-cli` Action sets up.  The second is an additional, manually configured connection.  These two different connections are used to resolve build dependencies and define a publish destination, respectively.
2. The JF Maven CLI wrapper allows for the definition of different source and desitination registries.  Most package managers will accomodate this type of setup.  It may require further investigation for NPM, PyPI, etc...
3. Pull requests welcome!

# Enjoy!
