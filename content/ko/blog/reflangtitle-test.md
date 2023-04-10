+++
title = "KO: <reflangtitle> shortcode 테스트 페이지"
description = "<reflangtitle> shortcode 테스트 페이지"
date = "2022-03-22T15:22:30"
expirydate = 2023-04-10T10:18:00+08:00
slug = "reflangtitle-test"
translationKey = "reflangtitle-test-202281"
+++

Create a link of a `ref`-erenced file with the actual title pulled automatically; and with multilingual support.

<!--more-->

## How to use

<!-- markdownlint-disable -->
This is {{</* relref */>}} expanded.
<!-- markdownlint-enable -->

<!-- markdownlint-disable -->
Syntax: {{</* reflangtitle path="" lang="" */>}}
<!-- markdownlint-enable -->

- If `lang=""` is empty, or not defined, it will search under the same language as the current page.

### Shortcode file: `/layouts/shortcodes/reflangtitle.html`

```golang
{{- $path := .Get "path" -}}
{{- $ref := relref . .Params -}}
{{- with .Site.GetPage $path -}}
  {{- range .AllTranslations -}}
    {{ if eq $ref .RelPermalink }}<a href="{{ .RelPermalink }}">{{ .Title }}</a>{{ break }}{{ end }}
  {{- end -}}
{{- end -}}
```

## Examples

### with `lang`

These codes:

<!-- markdownlint-disable -->
```golang
- {{</* reflangtitle path="reflangtitle-test.md" lang="en-ph" */>}}
- {{</* reflangtitle path="reflangtitle-test.md" lang="ja" */>}}
- {{</* reflangtitle path="reflangtitle-test.md" lang="ko" */>}}
```
<!-- markdownlint-enable -->

Will output:

- {{< reflangtitle path="reflangtitle-test.md" lang="en-ph" >}}
- {{< reflangtitle path="reflangtitle-test.md" lang="ja" >}}
- {{< reflangtitle path="reflangtitle-test.md" lang="ko" >}}

### empty or without `lang`

These codes:

<!-- markdownlint-disable -->
```golang
- {{</* reflangtitle path="reflangtitle-test.md" */>}}
- {{</* reflangtitle path="reflangtitle-test.md" lang="" */>}}
```
<!-- markdownlint-enable -->

Will output:

- {{< reflangtitle path="reflangtitle-test.md" >}}
- {{< reflangtitle path="reflangtitle-test.md" lang="" >}}
