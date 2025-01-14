# How to contribute  [![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

Welcome contributors.To contribute, first fork our repository into your own Github account, and create a local clone of it as described in the [installation instructions](#installation-instructions). The latter will be used to get new features implemented or bugs fixed. Once done and you have the code locally on the disk, you can get started. We advice to not work directly on the master branch, but to create a separate branch for each issue you are working on. That way you can easily switch between different work, and you can update each one for latest changes on upstream master individually.

## Installation Instructions

Follow the steps below to setup a development environment. Fork our repository into your own github account, and run:

```bash
    #!/bin/bash
    git clone https://github.com/%your_account%/N2-Avionics-BaseStation.git
    cd N2-Avionics-BaseStation/
    npm install
    npm run dev
```

### Note

The `docker-compose.yaml` requires the `DOCKER_CLIENT_IMAGE` environment variable is to be set. To do this create a file named `.env` placed in the same directory as the `docker-compose.yaml` file. Then add:

```text
    DOCKER_CLIENT_IMAGE=/% your image %/
```

# Managing the Repository

## versioning

This project uses [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) for semantic versioning [(semver)](https://semver.org/). Husky is integrated to reject invalid commits. If you are unfamiliar with `conventional commits` we recommend using [commitizen](https://github.com/commitizen/cz-cli)

## Merging Pull Requests

Once a PR is in its final state it needs to be merged into the upstream master branch. For that please `DO NOT` use the Github merge button! But merge it yourself on the command line. Reason is that we want to hvae a clean history. Before pushing the changes to upstream master make sure that all individual commits have been `squashed` into a single one with a commit message.
