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

### `toggle` Shortcode

The `toggle` is a universal toggle/tabs component.

```markdown
{{< bootstrap/toggle [name] >}}

PUT TOGGLE ITEMS HERE

{{< /bootstrap/toggle >}}
```

| Parameter | Position |  Type  | Required | Description                                  |
| --------- | :------: | :----: | :------: | -------------------------------------------- |
| `name`    |   `#0`   | String |    Y     | The name of toggle, MUST be unique per page. |

### `toggle-item` Shortcode

The `toggle-item` must be used within the `toggle` shortcode.

```markdown
{{< bootstrap/toggle-item [name] >}}
TOGGLE ITEM CONTENT HERE, MARKDOWN AND SHORTCODE ARE SUPPORTED.
{{< /bootstrap/toggle-item >}}
```

| Parameter | Position |  Type  | Required | Description                                         |
| --------- | :------: | :----: | :------: | --------------------------------------------------- |
| `name`    |   `#0`   | String |    Y     | The name of toggle item, MUST be unique per toggle. |
