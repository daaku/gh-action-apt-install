# gh-action-apt-install

Cache `apt-install` in GitHub Actions. Usage:

```yaml
- name: Dependencies
  uses: daaku/gh-action-apt-install@v3
  with:
    packages: luajit libluajit-5.1-dev
```

Optionally a `version` can be specified to manually bump the cache key.
