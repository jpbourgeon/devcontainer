# vscode typescript-node devcontainer

> Bootstrap a typescript-node devcontainer for vscode in minutes

Pre-requisites : you need to install Docker (I use Docker Desktop for convenience), VSCode and the Remote-Containers extension, on your dev computer.

1. In VS-Code execute the command `Remote-Containers: Clone Repository in Named Container Volume...`
   1. Clone from URL `jpbourgeon/ts-node-devcontainer`
   1. `Create a new volume` with a meaningful name
   1. Leave the target folder name untouched (this is important for the post-create script execution).
1. Rename the docker image `docker container rename OLD_NAME NEW_NAME`
1. Start hacking
   - Configure Github CLI `gh auth login`
   - Add more extensions inside the container : nx console, github copilot, github copilot labs, ponicode, architect, etc.
   - Git clone your project's repo and/or add workspaces in the `/workspaces` folder
   - ...
