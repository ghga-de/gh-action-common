# GHGA GitHub Action Common

This GitHub Action encapsulates common steps that are executed in GitHub Action workflows within GHGA repositories. Use as follows:

```
- id: common
  uses: ghga-de/gh-action-common@v2
```

The action outputs the following values:
| Variable | Description |
| --- | --- |
| PACKAGE\_NAME | Name of the microservice package |
| MAIN\_SRC\_DIR | The main source directory of the microservice package |
| CONFIG\_YAML\_ENV\_VAR\_NAME | The name of the environment variable pointing to the config yaml file |
| CONFIG\_YAML | The config YAML file |
