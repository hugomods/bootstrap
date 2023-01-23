---
---

## Shortcodes

## `config-toggle`

{{< bootstrap/config-toggle config >}}
[[module.imports]]
path = "github.com/razonyang/hugo-mod-bootstrap"
{{< /bootstrap/config-toggle >}}

## `toggle`

{{< bootstrap/toggle foobar >}}

{{< bootstrap/toggle-item Foo >}}
Foo Content
{{< /bootstrap/toggle-item>}}

{{< bootstrap/toggle-item Bar >}}
Bar Content
{{< /bootstrap/toggle-item>}}

{{< /bootstrap/toggle >}}

{{< bootstrap/toggle sdk >}}

{{< bootstrap/toggle-item JS >}}
{{< highlight js >}}
console.log('hello world')
{{< /highlight >}}
{{< /bootstrap/toggle-item>}}

{{< bootstrap/toggle-item PHP >}}
{{< highlight php >}}

<?php
echo 'hello world'
{{< /highlight >}}
{{< /bootstrap/toggle-item>}}

{{< bootstrap/toggle-item Go >}}
{{< highlight go >}}
package main

import "fmt"

func main() {
    fmt.Println("hello world")
}
{{< /highlight >}}
{{< /bootstrap/toggle-item>}}

{{< /bootstrap/toggle >}}
