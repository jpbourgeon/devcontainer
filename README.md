# VSCode typescript-node devcontainer

> Bootstrap a minimal typescript-node devcontainer for vscode in minutes

## Content

- Based on Microsoft's devcontainer image [Node.js & TypeScript (Debian 16-bullseye)](https://github.com/microsoft/vscode-dev-containers/tree/main/containers/typescript-node)
- [Workspace Explorer v2.3.0](https://marketplace.visualstudio.com/items?itemName=tomsaunders-code.workspace-explorer)  
  a VSCode extension to help manage workspaces inside the devcontainer
- [Github CLI v2.8.0](https://github.com/cli/cli/releases/v2.8.0)

## Pre-requisites

You already have installed the following on your development computer:

- Docker or Docker desktop
- VSCode and the Remote-Development extension pack, or at least the remote-containers extension.

## Installation

1. In VS-Code execute the command `Remote-Containers: Clone Repository in Named Container Volume...`
   1. Clone this repository from URL `jpbourgeon/devcontainer-ts`
   1. `Create a new volume` with a meaningful name
   1. Leave the target folder name untouched (this is important for the post-create script execution).
1. Rename the docker image `docker container rename CURRENT_NAME NEW_NAME`
1. Configure the Github CLI `gh auth login`
1. Add your project's repository to the `/workspaces` folder. You may duplicate the template repository from [`jpbourgeon/devcontainer-repository`](https://github.com/jpbourgeon/devcontainer-repository). It provides you with a basic code workspace and an empty installation script to get started.  
   _Hint : you can host multiple projects in the same devcontainer !_

## Updates

To update the devcontainer to the latest version:

1. Attach VSCode to the devcontainer
1. Open the terminal and `cd /workspaces/devcontainer-ts`
1. `git pull` the latest commit on the `main` branch
1. From the Remote explorer panel, right click on the `devcontainer-ts` container and select `Rebuild container`
