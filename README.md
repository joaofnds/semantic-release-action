## Usage example

will install [semantic-release](https://github.com/semantic-release/semantic-release) and
the aditional specified plugins, clone your repo and run `npx semantic-release`

```yaml
on: [push]

jobs:
  release:
    runs-on: ubuntu-latest
    steps:
      - uses: joaofnds/semantic-release-action@1.0.0
        with:
          plugins: "@semantic-release/changelog @semantic-release/git"
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

| key     | default | description                  |
| ------- | ------- | ---------------------------- |
| version | 19.0.2  | semantic-release version     |
| plugins | ""      | aditional plugins to install |
