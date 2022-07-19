# hugo-mod-picocss
Thin Hugo Module wrapper around [picocss](https://picocss.com) library. 


## Usage
Edit your ``config.yaml`` as following to add the library as a [hugo module](https://gohugo.io/hugo-modules/). Thereafter, picocss' files are available under ``assets/csslibs/picocss``.

```YAML
module:
  imports:
    - ignoreConfig: false
      disable: false
      ignoreImports: false
      path: github.com/chrische/hugo-mod-picocss
```

In your layout you may use it as following:

```HTML
{{ with resources.Get "/csslibs/picocss/pico.min.css" }}
  <link rel="stylesheet" href="{{ .RelPermalink }}">
{{ end }}
```
