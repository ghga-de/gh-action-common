# GHGA GitHub Action Common

This GitHub Action encapsulates common steps that are executed in GitHub Action workflows within GHGA repositories. Use as follows:

```
- id: common
  uses: ghga-de/gh-action-common@v3
```

The action outputs the following values:
| Variable | Description |
| --- | --- |
| PACKAGE\_NAME | Name of the microservice package |
| MAIN\_SRC\_DIR | The main source directory of the microservice package |
| CONFIG\_YAML\_ENV\_VAR\_NAME | The name of the environment variable pointing to the config yaml file |
| CONFIG\_YAML | The config YAML file |

---

>Note: v3 of this action will only work with an exhaustive `requirements-dev.txt` file. If you only have top-level dependencies in that file, pip will not install the transitive dependencies. This update coincides with the move to pip-tools in the `microservice-repository-template`.