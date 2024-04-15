# GHGA Microservice GitHub Action Common

## Usage

This GitHub Action encapsulates common steps that are executed in GitHub Action workflows within [GHGA repositories](https://github.com/orgs/ghga-de/repositories) for microservices and libraries. Use as follows:

```
- id: ghga-common
  uses: ghga-de/gh-action-common@v5
  with:
    python-version: '3.12'
```

If the `with` block is omitted, the default Python version for the GHGA repositories will be used, which is currently Python 3.9.

## Output

The action outputs the following values:

| Variable | Description |
| --- | --- |
| PACKAGE\_NAME | the name of the microservice package |
| MAIN\_SRC\_DIR | the main source directory of the microservice package |
| CONFIG\_YAML\_ENV\_VAR\_NAME | the name of the environment variable pointing to the config YAML file |
| CONFIG\_YAML | the config YAML file |

## Changelog

### v5

Allows specifying the Python version in the `with` block.

### v4

The lock file must now be located in the `.lock` directory.

### v3

This action will now only work with an exhaustive `requirements-dev.txt` file. If you only have top-level dependencies in that file, pip will not install the transitive dependencies. This update coincides with the move to pip-tools (uv) in the [microservice-repository-template](https://github.com/ghga-de/microservice-repository-template).

### v2

Uses a requirement file for dev requirements instead of relying on the "all" extra.
