# hugo_layoutsghsvs

A collection of more or less dilettantish layouts, templates and more for my Hugo-based sites.

To be mounted in other Hugo-based repositories. I only mount locally. No online mounts tested.

Will be changed regularly according to my needs. Don't rely on backwards compatibility!

I take absolutely no account of build speed and/or security, as I only work with it locally.

If it works, it works. Optimisations follow step by step when I feel like it and have the time.

## Mount example (config.yml)

```
module:
  imports:
    - path: github.com/GHSVS-de/hugo_layoutsghsvs
      mounts:
        - source: dist/assets/.htaccess
          target: assets/.htaccess

        # Contains partials, shortcodes and so on.
        - source: dist/layouts
          target: layouts
        - source: dist/i18n
          target: i18n
        - source: dist/data
          target: data
```

## Mount example part 2 (go.mod)
File in mounting repo named `hugo_herzghsvs` in local folder `/mnt/z/git-kram/hugo_herzghsvs`.

```
module github.com/GHSVS-de/hugo_herzghsvs

go 1.18

replace (
	github.com/GHSVS-de/hugo_layoutsghsvs => /mnt/z/git-kram/hugo_layoutsghsvs
)

require (
	github.com/GHSVS-de/hugo_layoutsghsvs v0.0.0-00010101000000-000000000000 // indirect
)
```
