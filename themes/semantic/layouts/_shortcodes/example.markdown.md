{{- $language := .Get "lang" | default "html" -}}
{{- $code := .InnerDeindent | strings.TrimSpace -}}
```{{ $language }}
{{ $code }}
```
