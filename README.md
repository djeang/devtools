# dev-tools ![Build](https://github.com/reugn/dev-tools/workflows/Build/badge.svg)

A collection of developer utilities in a single desktop application.

* [JSON Editor](#json-editor)
* [Image Editor](#image-editor)
* [Rest API Tester](#rest-api-tester)
* [JWT Decoder](#jwt-decoder)
* [UUID/Password Generator](#uuid-password-generator)
* [Hash Calculator](#hash-calculator)
* [Epoch Converter](#epoch-converter)
* [Regular Expression Tester](#regular-expression-tester)
* [ASCII Graphics](#ascii-graphics)
* [Log Generator](#log-generator)

## Installation

The application is built with [JeKa](https://jeka-dev.github.io/jeka/), so you can run or install it from its Git
repository, without cloning it yourself. It shows how JeKa builds a JavaFX application (with the `javafx` plugin),
and packages it as a desktop application with *jpackage* (`bundle` KBean).

[Install JeKa](https://jeka-dev.github.io/jeka/installation/) if you don't have it. JeKa downloads the JDK and JavaFX it needs.

Install the desktop application:
```shell
jeka app: install repo=devtools@djeang runtime=BUNDLE
```

`devtools@djeang` refers to this repository in the *djeang* catalog. JeKa builds the application, packages it,
and opens the folder holding the package. On the first run, JeKa asks you to confirm that you trust this repository.

Run the application without installing it:
```shell
jeka -r https://github.com/djeang/devtools -p
```

See the other tools of the catalog:
```shell
jeka app: catalog name=djeang
```

From a clone of this repository, run it with `jeka -p`, or create the package in `jeka-output/` with `jeka bundle: pack`.
`-p` reuses the jar already in `jeka-output/`: after `jeka bundle: pack`, run `jeka -c -p` to rebuild it as a runnable jar.

### How it works

- [jeka.properties](jeka.properties): JeKa and Java versions, the `javafx` plugin (JavaFX follows the Java version),
  the main class, and the *jpackage* options: modules of the bundled runtime, and icons per platform.
- [jeka.project.deps](jeka.project.deps): the dependencies. JavaFX is `compile-only`, as the plugin adds it to the module path.

Learn more: [app KBean](https://jeka-dev.github.io/jeka/reference/kbeans-app/),
[bundle KBean](https://jeka-dev.github.io/jeka/reference/kbeans-bundle/),
[source-runnable applications](https://jeka-dev.github.io/jeka/tutorials/source-runnable-apps/).

## Getting Started

* Explore the main menu and its options.
* Select a tool from the `Tools` dropdown menu. See below for a complete list with screenshots.
* Switch between light and dark themes using the `View -> Theme` menu option.
* Utilize keyboard shortcuts for faster navigation.

## Tool List

### JSON Editor

Edit and analyze JSON using syntax highlighting, formatting, and validation.
Use the built-in search (Ctrl+F) to find items. Navigate between documents using the multi-tab interface.

![](docs/images/json_editor.png)

### Image Editor

This tool incorporates an essential suite of functions for creating and editing images.

![](docs/images/image_editor.png)

### Rest API Tester

This tool provides a core set of functionalities for REST API testing.
Manage and share your testing process via the export and import of HTTP request history.
Access history features by Ctrl-clicking the history pane. Navigate between requests using the multi-tab interface.

![](docs/images/rest_api.png)

### JWT Decoder

Paste your JSON Web Token (JWT) into the input area to decode it. Use the provided buttons to
decode, encode, and verify the JWT signature. For signature verification, select the correct algorithm and provide
the necessary secrets.

![](docs/images/jwt_decoder.png)

### UUID-Password Generator

Generate a series of UUIDs (Universally Unique Identifiers) or passwords according to the provided configuration
controls.

![](docs/images/generator.png)

### Hash Calculator

This utility performs cryptographic hashing and various encoding/decoding operations on input data.

![](docs/images/hash_calculator.png)

### Epoch Converter

Epoch Converter is a utility for converting between Unix epoch time (seconds since January 1, 1970, 00:00:00 UTC)
and human-readable dates. Features include displaying the current Unix epoch, timestamp to date/time
conversion, and date/time to timestamp conversion.

![](docs/images/epoch_converter.png)

### Regular Expression Tester

Regular Expression Tester is a tool for testing and debugging regular expressions (regex) featuring full regex flag
support (i, m, u, etc.), comprehensive capturing group visualization and match highlighting.

![](docs/images/regex_tester.png)

### ASCII Graphics

Easily turn your text into ASCII art. Customize the look with adjustable settings.

![](docs/images/ascii_graphics.png)

### Log Generator

Log Generator creates customizable synthetic log data for testing and development.
Choose from a selection of pre-defined standard log formats.
Write the generated logs directly to the output pane, or save them to a file for later use.

![](docs/images/log_generator.png)

## License

Licensed under the Apache 2.0 license.
