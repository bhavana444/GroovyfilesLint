![Branch main](https://img.shields.io/badge/branch-main-brightgreen.svg?style=flat-square) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/bhavana444/GroovyfilesLint/blob/main/LICENSE)

# GroovyfilesLint

This pre-commit hook uses [nvuillam/npm-groovy-lint](https://github.com/nvuillam/npm-groovy-lint) docker image for linting Groovy files.


Table of Contents
-----------------

  * [Requirements](#requirements)
  * [Installation](#installation)
  * [Contributing](#contributing)
  * [License](#license)
  * [Author](#author)

Requirements
------------
 GroovyfilesLint requires the following to run:

  * [pre-commit](http://pre-commit.com)
  * [Docker](https://docs.docker.com/engine/install/)
    

Installation
---------

1. Please refer the list of available tags [here](https://github.com/bhavana444/GroovyfilesLint/tags)
2. create .pre-commit-config.yaml in your git project
3. pre-commit install 


A sample **.pre-commit-config.yaml** may look like the following:

```yaml
- repo: https://github.com/govindsme/JenkinsfileLint
    rev: v1                                        # tag
    hooks:
      - id: GroovyfilesLinter
        args: ['$PWD/*/*.groovy']                  # path to all groovy files
```

You may require to add **.groovylintrc.json** to have the required exclusion

```json
{
    "extends": "recommended-groovyfile",
    "rules": {
        "ignoreVariableNames": "off",
        "VariableName": {
            "severity": "info"
        }
    }
}


```

Contributing
------------

To contribute to GroovyfilesLint, fork this repo and raise a pull request. 


Author
------

> GitHub [@bhavana444](https://github.com/bhavana444)     


License
-------

pre-commit-shell is licensed under the [MIT](https://github.com/govindsme/JenkinsfileLint/blob/main/LICENSE) license.  
