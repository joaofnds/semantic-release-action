## Usage example

will install [semantic-release](https://github.com/semantic-release/semantic-release) and
the additional specified plugins, clone your repo, and run `npx semantic-release`

```yaml
on: [push]

jobs:
  release:
    runs-on: ubuntu-latest
    steps:
      - uses: joaofnds/semantic-release-action@v1.4.0
        with:
          plugins: "@semantic-release/changelog @semantic-release/git"
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

| key     | default | description                   |
| ------- | ------- | ----------------------------- |
| version | 24.0.0  | semantic-release version      |
| plugins | ""      | additional plugins to install |
