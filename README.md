# Hugo Bootstrap Module

This module ships with handy partials and shortcodes.

## Shortcodes

### `config-toggle` Shortcode

The `config-toggle` generates same configuration in multiple formats (`TOML`, `YAML` and `JSON`) from one configuration, it's useful to write docs for projects that support multiple formats configurations.

```markdown
{{< bootstrap/config-toggle >}}
CONFIGURATION WRITTEN IN ONE OF SUPPORTED FORMATS.
{{< /bootstrap/config-toggle >}}
```

| Parameter  | Position |  Type  | Required | Description                                                                                                                                       |
| ---------- | :------: | :----: | :------: | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| `filename` |   `#0`   | String |    -     | The filename of configuration without extension.                                                                                                  |
| `langs`    |   `#1`   | String |    -     | The target languages, separate by commas without white spaces, such as `yaml,toml`, it can also be used to change the default order of languages. |
