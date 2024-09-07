# Use the official Python 3.10 slim image as the base image
FROM python:3.10-slim

# Define the working directory inside the container
WORKDIR /book_catalog

# Add the requirements.txt file to the container's working directory
COPY requirements.txt .

# Install the necessary dependencies from the requirements.txt file
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application files into the container's working directory
COPY app/ .

# Expose port 80 so the application can be accessed externally
EXPOSE 80

# Start the FastAPI application using Uvicorn, listening on all IPs and port 80
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]