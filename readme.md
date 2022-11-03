# gh-action-apt-install

Cache `apt-install` in GitHub Actions.

Essentially, this bundles all installed files into a single zstd compressed
tarball cached using [actions/cache](https://github.com/actions/cache) for
future runs. This is much more speedy than going through the `apt install` flow,
but has various caveats (such as post install scripts are not run).

## Usage

```yaml
- name: Dependencies
  uses: daaku/gh-action-apt-install@v3
  with:
    packages: luajit libluajit-5.1-dev
```

Optionally a `version` can be specified to manually bump the cache key.
