# Use the official Python image from the Docker Hub
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /usr/src/manim

# Clone the Manim repository from GitHub
RUN apt-get update && apt-get install -y git \
    && git clone https://github.com/3b1b/manim.git .

# Install additional dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose any ports the app is expecting in the environment
# (if Manim requires any specific ports, you can expose them here)

# Command to run the Manim animation script
CMD ["manim", "-pl", "example_scenes.py"]
