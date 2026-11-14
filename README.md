# Go Project Template ![CI](https://github.com/ahcodedev/go-template/actions/workflows/ci.yml/badge.svg?branch=main) ![Security](https://github.com/ahcodedev/go-template/actions/workflows/security.yml/badge.svg?branch=main)

[Copier](https://copier.readthedocs.io) template for Go projects. Generated projects include Task, golangci-lint, coverage checks, gitleaks, zizmor and Dependabot.

## Create a project

```sh
copier copy gh:ahcodedev/go-template my-project
```

Pull later template changes into a generated project:

```sh
copier update
```

## Developing the template

Project files live in [template/](template/). Files ending in `.jinja` are rendered with the answers from [copier.yml](copier.yml).

- Install dependencies: `brew bundle install`
- Render into `./rendered` (gitignored): `task render`
- Build, test, coverage and lint the rendered project: `task build`, `task test`, `task coverage`, `task lint`
- Security checks: `task gitleaks`, `task zizmor`, `task security`
- See available commands: `task --list`
