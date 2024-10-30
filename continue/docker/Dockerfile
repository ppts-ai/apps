# Start from the official code-server base image
FROM codercom/code-server:latest

# Install required dependencies
RUN sudo apt-get update && \
    sudo apt-get install -y curl git python3 python3-pip && \
    sudo apt-get clean

# Install Visual Studio Code extensions
RUN code-server --install-extension ms-python.python \
    && code-server --install-extension continue.continue

# Expose the port for code-server
EXPOSE 8080

# Set up code-server's entrypoint
CMD ["code-server", "--bind-addr", "0.0.0.0:8080", "/home/coder/project"]
