# Open Source issue labels generator

A GitHub action that generates the labels you want (customizable name and color) in any repository, easy and efficient.

## Usage

To use this Action, you only need the yaml file below.

```yaml
name: Import open source standard labels

on:
  push:
    branches: [ main ]

jobs:
  labels:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/setup-node@v2
      with:
        node-version: '14'
    - uses: Devs-Dungeon/gh-action-open-source-labels@main
      with:
        github-token: ${{ secrets.GITHUB_TOKEN }}
        owner-name: ${{ github.repository_owner }}
        repository-name: ${{ github.event.repository.name }}
        # force: true # optional to clear existing labels, default to true
```

## 🔗 Connect with Us
[<img align="left" alt="Subham | Mail" width="80px" src="https://img.shields.io/badge/-Gmail-000000?logo=gmail&Color=0A66C2&style=flat-square" />][mail]
[<img align="left" alt="Subham | LinkedIn" width="100px" src="https://img.shields.io/badge/-LinkedIn-000000?logo=linkedin&Color=0A66C2&style=flat-square" />][linkedin]
[<img align="left" alt="Subham | Discord" width="92px" src="https://img.shields.io/badge/-Twitter-000000?logo=twitter&Color=0A66C2&style=flat-square" />][twitter]
[<img align="left" alt="Subham | Discord" width="92px" src="https://img.shields.io/badge/-Discord-000000?logo=discord&Color=0A66C2&style=flat-square" />][discord]

[mail]: mailto:devs.dungeon.community@gmail.com
[linkedin]: https://www.linkedin.com/company/devs-dungeon/
[twitter]: https://twitter.com/devs_dungeon
[discord]: https://discord.gg/ceMXzhfaka

