# Use the official Python image from the Docker Hub
FROM python:3.9.18-slim-bookworm

# Set the working directory
WORKDIR /python-docker

# Copy the requirements file into the image
COPY requirements.txt .

# Install the dependencies
RUN pip3 install -r requirements.txt

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 50505

ENTRYPOINT ["gunicorn", "app:app"]
