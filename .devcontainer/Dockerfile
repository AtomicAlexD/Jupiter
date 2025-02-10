# Use a lightweight Python image
FROM python:3.11-alpine

# Set the working directory inside the container
WORKDIR /workspace

# Install system dependencies
RUN apk update && apk add --no-cache git mysql-client

# Copy the requirements file from the app folder
COPY ./app/requirements.txt /workspace/requirements.txt

# Install dependencies
RUN pip install --no-cache-dir -r /workspace/requirements.txt

# Expose any necessary ports
EXPOSE 5000

# Start the application
CMD ["python", "app/main.py"]
