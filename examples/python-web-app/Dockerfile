# Use the official Python image from the Docker Hub
FROM python:3.11

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt /app/
COPY devops /app


# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt && cd devops
RUN python manage.py migrate

ENTRYPOINT ["python"]
# Start the Django development server (change as needed for production)
CMD ["manage.py", "runserver", "0.0.0.0:8001"]




