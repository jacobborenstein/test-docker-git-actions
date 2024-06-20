# Use an official Python runtime as a parent image
FROM python:3.8-slim

# Set the working directory in the container
WORKDIR /app

# Copy the contents of the python directory into the /app directory in the container
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r /app/requirements.txt

# Make port 80 available to the world outside this container
EXPOSE 80

# Set PYTHONPATH environment variable
ENV PYTHONPATH=/app/code

# Run code.main:app using Uvicorn
CMD ["uvicorn", "code.main:app", "--host", "0.0.0.0", "--port", "80"]