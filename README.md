# Readme

Website using hugo templates - that describes 'my' photography projects.

Minimalistc layout, 3 columns | menu | content | images (single column below 992px)

Change /content for adding your 'data' - polish `name.md` (default, /), english `name.en.md` (/en/, images taken from polish page)
Img, are stored in assets/images/ - hugo converts them to webp (q95) with 640px variant at build time

## Hosting

| environment | url | config | deploy |
|---|---|---|---|
| production | https://patrykjanota.pl | `config/production/` | `hugo --minify` |
| sandbox | https://pljanot.github.io/patrykjanota.pl/ | `config/sandbox/` | GitHub Actions on push to `main` |

* build production into /public dir
```bash
hugo --minify
```

* build sandbox into /public dir
```bash
hugo --environment sandbox --minify
```

* build and start server using different baseUrl=>localhost:1313
```bash
hugo server -D --baseURL="http://localhost:1313/"
```
