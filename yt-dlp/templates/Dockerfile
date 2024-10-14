# Use the Alpine base image
FROM python:alpine3.20

# Set environment variables for Python to avoid buffer issues
ENV PYTHONUNBUFFERED=1

# Install yt-dlp dependencies: Python3, pip, and ffmpeg for video processing
RUN apk update && \
    apk add --no-cache \
    ffmpeg && \
    pip3 install yt-dlp && \
    # Clean up unnecessary files after installation
    rm -rf /var/cache/apk/* /root/.cache /tmp/*

# Set the working directory
WORKDIR /app

# Default command to run yt-dlp, allowing arguments to be passed from 'docker run'
ENTRYPOINT ["yt-dlp"]
