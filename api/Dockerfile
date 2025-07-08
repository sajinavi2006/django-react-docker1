# Pull base image
FROM python:3.8-slim-buster

# Set environment variables
ENV PIP_DISABLE_PIP_VERSION_CHECK 1
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work directory
WORKDIR /api
COPY requirements.txt .
RUN pip install -r requirements.txt
# Install dependencies
RUN pip install django django-cors-headers

# Copy project
COPY . .

EXPOSE 8000
