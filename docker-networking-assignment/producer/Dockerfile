# Use an official Python image
FROM python:3.8-alpine

# Set the working directory
WORKDIR /app

# Copy necessary files
COPY requirements.txt .
COPY app.py .

# Install dependencies 
#--no-cache-dir is used to keep the image size as small as possible by avoiding caching the dependencies.
#But if we frequently rebuild the image and install the same packages, caching might actually speed up the build process.
#So, for local development, caching is beneficial,but in production, smaller images are better.
RUN pip install --no-cache-dir -r requirements.txt

# Expose port 5000 for communication
EXPOSE 5000

# Start the application
CMD ["python", "app.py"]
