# Use the official Python base image
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements.txt (if any) and install dependencies
COPY requirements.txt .

# Install Flask and any other dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Python app and templates directory into the container
COPY app.py .
COPY templates/ /app/templates/

# Expose port 80 for the web application
EXPOSE 80

# Run the application
CMD ["python", "app.py"]
