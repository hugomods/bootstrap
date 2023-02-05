---
---

## `alert`

### `alert` Styles

{{< bootstrap/alert primary >}}
A simple primary alert—check it out!
{{< /bootstrap/alert >}}

{{< bootstrap/alert secondary >}}
A simple secondary alert—check it out!
{{< /bootstrap/alert >}}

{{< bootstrap/alert success >}}
A simple success alert—check it out!
{{< /bootstrap/alert >}}

{{< bootstrap/alert danger >}}
A simple danger alert—check it out!
{{< /bootstrap/alert >}}

{{< bootstrap/alert warning >}}
A simple warning alert—check it out!
{{< /bootstrap/alert >}}

{{< bootstrap/alert info >}}
A simple info alert—check it out!
{{< /bootstrap/alert >}}

{{< bootstrap/alert light >}}
A simple light alert—check it out!
{{< /bootstrap/alert >}}

{{< bootstrap/alert dark >}}
A simple dark alert—check it out!
{{< /bootstrap/alert >}}

### `alert-link`

{{< bootstrap/alert >}}
A simple primary alert with {{< bootstrap/alert-link "an example link" "#alert-link" >}}. Give it a click if you like.
{{< /bootstrap/alert >}}

### `alert-heading`

{{< bootstrap/alert success >}}
{{< bootstrap/alert-heading "Well done!" >}}
Aww yeah, you successfully read this important alert message. This example text is going to run a bit longer so that you can see how spacing within an alert works with this kind of content.
{{< /bootstrap/alert >}}

## `clearfix`

{{% bootstrap/clearfix %}}
<img class="float-start me-2" src="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.3/icons/bootstrap.svg" width="64px" height="64px"> TEXTS AROUND THE FLOATED IMAGE.

WRAP IT INSIDE THE `clearfix` SHORTCODE.
{{% /bootstrap/clearfix %}}

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
