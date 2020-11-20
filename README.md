# Requirements

Docker and Docker-compose are required if you want to run Mongo in a container.
If you have it running on your system, then you don't need Docker.

# Installation

```sh
# Create Python Virtual Environment
virtualenv --no-site-packages -p python3.6 venv
# Activate it
source venv/bin/activate
# Install dependencies
pip install -r requirements.txt
# Launch Mongo
docker-compose -f docker-compose.yml up
# Find ID of the mongo container
docker ps
# Connect to Mongo
docker exec -it MONGO_CONTAINER_ID /bin/bash
cd /data
# Restore backup
mongorestore -d RoboAdvisor dumps
```

# Running

```sh
# Navigate to main folder
cd User\ interfaces/CGM/
# Run Django
python manage.py runserver
```

Open `http://127.0.0.1:8001/#example` in your browser
