# AWS CLI Tools
A docker image for running AWS CLI commands.

## Usage

- Open aws-shell with default aws profile:

  ```
  docker run --rm -it --volume "$HOME/.aws:/root/.aws" \
    --volume "$(pwd):/code" carlosesilva/aws-tools
  ```

- Open bash with a specific aws profile:

  ```
  docker run --rm -it --volume "$HOME/.aws:/root/.aws" \
    --volume "$(pwd):/code" -e AWS_PROFILE=<aws_profile> \
    carlosesilva/aws-tools /bin/bash
  ```

- Persist the the shell history and other things across runs:

  ```
  docker run --rm -it --volume aws-tools:/root \
    --volume "$HOME/.aws:/root/.aws" --volume "$(pwd):/code" \
    carlosesilva/aws-tools /bin/bash
  ```

## Includes

### AWS

- aws-cli
- aws-shell
- awsebcli

### Other

- terraform
- bash
- less
- curl
- git
- jq
- groff
- py-pip
- python
- nodejs
- npm
