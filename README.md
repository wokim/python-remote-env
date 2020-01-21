# Python Remote Environment

Python Remote Environment lets you use a Docker container as a full-featured development environment in Visual Studio Code.

- Beyond the advantages of having your team use a consistent environment and tool-chain, this also makes it easier for new contributors or team members to be productive quickly.
- First-time contributors will require less guidance and hit fewer issues related to environment setup.

![Overview](https://code.visualstudio.com/assets/docs/remote/containers/architecture-containers.png)
This environment is based on the [Developing inside a Container](https://code.visualstudio.com/docs/remote/containers)

## Toolchain

For more details, please refer to `.devcontainer/devcontainer.json` and `.devcontainer/Dockerfile` files.

| Name | Version | Name | Version |
| ------ | ------ | ------ | ------ |
| python | 3.8.1 | pip | 19.3.1 |
| autopep8 | 1.5 | pylint | 2.4.4 |
| node.js | 10.17.0 | npm | 6.13.4 |
| yarn | 1.21.1 | docker | 19.03.5 |
| containerd | 1.2.10 | docker-compose | 1.25.0 |
| awscli | 1.17.6 | aws-cdk | 1.21.1 |
| git | 2.20.1 | debian | 10-buster |

## Environment variables

For more details, please refer to `.devcontainer/devcontainer.env` file.

## Prerequisites

Python Remote Environment requires [Docker Desktop 2.0+](https://hub.docker.com/?overlay=onboarding) or Docker CE 18.06+

### Download PowerLine fonts

```sh
# clone
git clone https://github.com/powerline/fonts.git --depth=1

# install
cd fonts
./install.sh

# clean-up a bit
cd ..
rm -rf fonts
```

### Git configuration

```sh
git config --global user.name "name"
git config --global user.email account@yourdomain.com

$ git config --list
user.name=Kim, Wonshik
user.email=wonshikkim.kr@gmail.com
credential.helper=osxkeychain
```

## How to use

By including `devcontainer.json` files in your repository, anyone that opens a local copy of your repo in VS Code will be automatically prompted to reopen the folder in a container, provided they have the Remote - Containers extension installed. You can also try it with `Remote-Containers: Reopen Folder in Container` in the Command Palette (`F1`).

![Reopen in Container](https://code.visualstudio.com/assets/docs/remote/containers/dev-container-reopen-prompt.png)

## Example

```sh
pip install -t vendor -r requirements.txt
python ./src/hello

```
