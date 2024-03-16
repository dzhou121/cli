#  Copyright (c) Microsoft Corporation. All rights reserved.
#  Licensed under the MIT License. See License.txt in the project root for license information.
FROM mcr.microsoft.com/vscode/devcontainers/typescript-node:18-bookworm

RUN mkdir -p /workspaces && chown node:node /workspaces

ARG USERNAME=node
USER $USERNAME

EXPOSE 6666

# Save command line history
RUN echo "export HISTFILE=/home/$USERNAME/commandhistory/.bash_history" >> "/home/$USERNAME/.bashrc" \
	&& echo "export PROMPT_COMMAND='history -a'" >> "/home/$USERNAME/.bashrc" \
	&& mkdir -p /home/$USERNAME/commandhistory \
	&& touch /home/$USERNAME/commandhistory/.bash_history \
	&& chown -R $USERNAME /home/$USERNAME/commandhistory
