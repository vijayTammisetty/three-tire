# Use the official Python image from Docker Hub
# Uses a slim version of the official Python image to keep the image small.
FROM python:3.10-slim 

# Set the working directory in the container
# Sets the working directory in the container to /app.
WORKDIR /app

# Copy the requirements file into the container at /app
# Copies the requirements.txt file to the container.
COPY requirements.txt ./

# Install any dependencies
# Installs the required Python packages.
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire Django project into the container
# Copies all files from your Django project to the container.
COPY . .

# Set environment variables (optional but useful for production)
ENV PYTHONUNBUFFERED 1

# Expose the port the app runs on (default Django port is 8000)
EXPOSE 8000

# Run the migrations and start the Django development server
# Runs Django's migrations and starts the development server, making the app accessible on all network interfaces (0.0.0.0:8000).
CMD ["sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]
