# Hugo Bootstrap Module

[![Used By](https://img.shields.io/badge/dynamic/json?color=success&label=used+by&query=repositories_humanize&logo=hugo&style=flat-square&url=https://api.razonyang.com/v1/github/dependents/hugomods/bootstrap)](https://github.com/hugomods/bootstrap/network/dependents)
![Hugo Requirements](https://img.shields.io/badge/dynamic/json?color=important&label=requirements&query=requirements&logo=hugo&style=flat-square&url=https://api.razonyang.com/v1/hugo/modules/github.com/hugomods/bootstrap)
[![License](https://img.shields.io/github/license/hugomods/bootstrap?style=flat-square)](https://github.com/hugomods/bootstrap/blob/main/LICENSE)
[![Version](https://img.shields.io/github/v/tag/hugomods/bootstrap?label=version&style=flat-square)](https://github.com/hugomods/bootstrap/tags)

This module ships with handy partials and shortcodes.

## Requirements

Some shortcodes like `clearfix` require the `markup.goldmark.renderer.unsafe` to be enabled.

```toml
[markup.goldmark.renderer]
unsafe = true
```

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

### `clearfix` Shortcode

The `clearfix` shortcode clear floated content.

```markdown
{{% bootstrap/clearfix %}}
FLOATED CONTENT, SUCH AS FLOATED IMAGES.
{{% /bootstrap/clearfix %}}
```

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
