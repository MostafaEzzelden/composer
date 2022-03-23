# Creating a PHP package

## What is composer?
Composer is an application-level package manager for the PHP programming language that provides a standard format for managing dependencies of PHP software and required libraries. It was developed by `Nils Adermann` and `Jordi Boggiano`, who continue to manage the project (Wikipedia)

## Why is composer needed?
Composer is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you. To start using Composer in your project, all you need is a `composer.json` file.

## What is composer.json file?
composer.json is a JSON file placed in the root folder of PHP project. This file describes the dependencies of your project and may contain other metadata as well.

## composer.json schema properties?
- *name* The name of the package. It consists of vendor name and project name, separated by /. Example: `monolog/monolog` Required for published packages (libraries). 
- *description*  A short description of the package. Usually this is one line long. Required for published packages (libraries). 
- *license* The license of the package. This can be either a string or an array of strings. Optional, but it is highly recommended.
- *authors* The authors of the package. This is an array of objects. Each author object can have following properties:(name, email, homepage, role) Optional, but highly recommended.
- *minimum-stability* This defines the default behavior for filtering packages by stability. This defaults to stable, so if you rely on a dev package, you should specify it in your file to avoid surprises.
- *prefer-stable* When this is enabled, Composer will prefer more stable packages over unstable ones when finding compatible stable packages is possible. If you require a dev version or only alphas are available for a package, those will still be selected granted that the minimum-stability allows for it. Use "prefer-stable": true to enable.
- *type* Package Type (e.g. library, project, composer-plugin).
- *require* Map of packages required by this package.
- *require-dev* Map of packages required for developing this package, or running tests, etc.




## Publish a new version number (rule)
info for versioning we should use the semantic versioning system in summary that system says the version number should have a three numbers eg.(1.0.0). 
the first one should change whenever your package has breaking changes. 
the second number should be higher when you add a feature.
the third number should increase when you made a bug fix.
