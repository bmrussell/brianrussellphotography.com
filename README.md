# PORTFILIO SITE

## REFERENCES
https://www.geeksforgeeks.org/git/publish-websites-on-github-pages-with-a-custom-domain/

https://gohugo.io/host-and-deploy/host-on-github-pages/

https://www.youtube.com/watch?v=MX4yy1dTVYg

### ORIGINAL
file:///H:/Adobe/portfolio/brianrussellphotography.com/abstract-1

## DEVELOPMENT

###
with dynamic updates
```bash
hugo server --disableFastRender --noHTTPCache
```

### Github Actions Build Failure
If there is a Go version missmatch, update the version in `.github\workflows\hugo.yaml`
```toml
GO_VERSION: 1.25.6
```

### CUSTOM DOMAIN
Set A Records:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Set CNAME Record
Name of `www` and target of `bmrussell.github.io.` (NB: period at the end)