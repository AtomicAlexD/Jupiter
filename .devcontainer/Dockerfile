# Use a lightweight Python image
FROM python:3.11-alpine

# Set the working directory inside the container
WORKDIR /workspace

# Install system dependencies
RUN apk update && apk add --no-cache git mysql-client

# Copy project files into the container
COPY requirements.txt .
RUN pip install -r requirements.txt

# Expose any necessary ports
EXPOSE 5000

# Start the application
CMD ["python", "app/main.py"]
