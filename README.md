# PORTFILIO SITE

## REFERENCES
* [Christian Lempa Hugo intro](https://www.youtube.com/watch?v=MX4yy1dTVYg)
* [Hugo GitHub pages guide](https://gohugo.io/host-and-deploy/host-on-github-pages/)
* [Custom domain guide](https://www.geeksforgeeks.org/git/publish-websites-on-github-pages-with-a-custom-domain/)
* [Local Archive](file:///H:\Adobe\portfolio\brianrussellphotography.com\)
* [Nico Kaiser's theme](https://github.com/nicokaiser/hugo-theme-gallery)


## DEVELOPMENT

### Start Hugo
with dynamic updates
```bash
hugo server --disableFastRender --noHTTPCache
```

### GitHub Actions Build Failure
If there is a Go version mismatch, update the version in `.github\workflows\hugo.yaml`
```toml
GO_VERSION: 1.25.6
```

### CUSTOM DOMAIN
1. Set A Records:
    ```
    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153
    ```

2. Set CNAME Record
Name of `www` and target of `bmrussell.github.io.` (NB: period at the end)

3. CNAME File
File named `CNAME` containing the domain name should be in the repository root.

## ADDING IMAGES
### Adding an album
1. Create a folder under `content\newalbum`
2. Add the photos
3. Add an index file as follows:
```yaml
---
title: New Album Titile
resources:
  - src: name of cover photo.jpg
    params:
      cover: true
---
```
4. Set image captions like
```powershell
exiftool -overwrite_original -ImageDescription="Westonbirt Carpet of Leaves" .\westonbirtcarpet.jpg
```