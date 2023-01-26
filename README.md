# Hugo Bootstrap Module

[![Used By](https://img.shields.io/badge/dynamic/json?color=success&label=used+by&query=repositories_humanize&logo=hugo&style=flat-square&url=https://api.razonyang.com/v1/github/dependents/razonyang/hugo-mod-bootstrap)](https://github.com/razonyang/hugo-mod-bootstrap/network/dependents)
![Hugo Requirements](https://img.shields.io/badge/dynamic/json?color=important&label=requirements&query=requirements&logo=hugo&style=flat-square&url=https://api.razonyang.com/v1/hugo/modules/github.com/razonyang/hugo-mod-bootstrap)
[![License](https://img.shields.io/github/license/razonyang/hugo-mod-bootstrap?style=flat-square)](https://github.com/razonyang/hugo-mod-bootstrap/blob/main/LICENSE)
[![Version](https://img.shields.io/github/v/tag/razonyang/hugo-mod-bootstrap?label=version&style=flat-square)](https://github.com/razonyang/hugo-mod-bootstrap/tags)

This module ships with handy partials and shortcodes.

## Shortcodes

### `alert` Shortcode

```markdown
{{< bootstrap/alert [style] >}}
...
{{< /bootstrap/alert >}}
```

| Parameter | Position |  Type  | Required | Default   | Description                                                                |
| --------- | :------: | :----: | :------: | --------- | -------------------------------------------------------------------------- |
| `style`   |   `#0`   | String |    -     | `primary` | The style, such as `primary`, `secondary`, `warning`, `info` and `danger`. |

You can nest the `alert-heading` and `alert-link` shortcodes inside it.

### `alert-heading` Shortcode

```markdown
{{< bootstrap/alert-heading [heading] >}}
```

| Parameter | Position |  Type  | Required | Description  |
| :-------: | :------: | :----: | :------: | ------------ |
|     -     |   `#0`   | String |    Y     | The heading. |

### `alert-link` Shortcode

```markdown
{{< bootstrap/alert-link [text] [url] >}}
```

| Parameter | Position |  Type  | Required | Description    |
| :-------: | :------: | :----: | :------: | -------------- |
|     -     |   `#0`   | String |    Y     | The link text. |
|     -     |   `#1`   | String |    Y     | The link URL.  |

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
