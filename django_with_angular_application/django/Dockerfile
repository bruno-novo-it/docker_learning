FROM python:3.7

# Install the main app on /app
WORKDIR /app

# Handles apt install via requirements.apt
# Install Python packages
COPY ./requirements.txt /app/requirements.txt
RUN apt-get update \
    && apt-get install -y gcc make g++ build-essential apt-utils \
    && pip3 install --no-cache-dir --upgrade -r requirements.txt \
    && apt-get purge -yqq gcc make g++ build-essential \
	&& apt-get autoremove -yqq \
	&& apt-get clean \
	&& rm -Rf /tmp/* /var/tmp/* /var/lib/apt/lists/*

# Copy all the code to the container
COPY . /app

# Make port 8000 available for the app
EXPOSE 8000

RUN python manage.py makemigrations \
    && python manage.py migrate

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
