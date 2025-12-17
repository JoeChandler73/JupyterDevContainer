# Base image
FROM mcr.microsoft.com/devcontainers/python:3-bookworm

# Set the working directory
WORKDIR /usr/src/app

# Copy the requirements file
COPY ./requirements.txt .

# Install torch
RUN pip install --no-cache-dir torch torchvision --extra-index-url https://download.pytorch.org/whl/cpu

# Install the Python dependencies (this layer gets cached!)
RUN pip install --no-cache-dir -r requirements.txt

USER vscode

CMD ["/bin/bash"]