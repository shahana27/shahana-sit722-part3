# Your Solution
# Start with an official Python runtime as the base image
FROM python:3.10-slim

# Define the working directory inside the container
WORKDIR /inventory_management

# Copy the requirements.txt file into the container’s working directory
COPY requirements.txt .

# Install the dependencies listed in the requirements.txt file
RUN pip install --no-cache-dir -r requirements.txt

# Copy all application files from the local 'app' directory into the container
COPY app/ .

# Open port 80 for external access to the container's application
EXPOSE 80

# Execute the FastAPI application using Uvicorn as the web server
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
