### Deploying a Web Application with Nginx and MySQL

This project demonstrates deploying a Django-based web application on AWS EC2 using Docker Compose.
Nginx acts as a reverse proxy, Django handles application logic, and MySQL manages persistent data storage.

The focus of this project is containerized deployment, infrastructure setup, and real-world debugging, not feature complexity.

### Tech Stack
Django
MySQL
Nginx
Docker and Docker Compose
Gunicorn
AWS EC2

### Architecture
1. Client sends HTTP requests to Nginx.
2. Nginx forwards requests to Django via Gunicorn.
3. Django processes logic and interacts with MySQL.
4. All services run as Docker containers on an AWS EC2 instance.

### Architecture diagram is available here:
docs/architecture.png

### Project Structure
```bash
django-docker-nginx-aws/
├── api/                    # Django app logic
├── mynotes/                # Django app module
├── notesapp/               # Django project settings
├── manage.py               # Django entry point
├── requirements.txt        # Python dependencies
├── staticfiles/             # Collected static assets
├── docker-compose.yml      # Multi-container orchestration
├── Dockerfile              # Django application image
├── nginx/
│   └── default.conf        # Nginx reverse proxy configuration
├── docs/
│   └── architecture.png    # System architecture diagram
├── proof/                  # Deployment proof screenshots
└── README.md               # Project documentation
```

### Demo Video
Full deployment and working demo:
https://drive.google.com/file/d/1QHX96JrnzKqLLFPl2JRiR7yFMU9DOoy6/view?usp=drive_link

### Requirements
Docker
Docker Compose
AWS EC2 instance or local Linux system

### Setup and Run
Clone the repository
```bash
git clone https://github.com/krishfr/django-docker-nginx-aws.git
cd django-docker-nginx-aws
```

### Create environment file
```bash
cp .env.example .env
```

### Build and start the application
```bash
docker compose up --build
```

### Stop the application
```bash
docker compose down
```

### What This Project Demonstrates
Docker Compose based multi-container setup
Nginx reverse proxy configuration
Django production deployment using Gunicorn
MySQL database initialization and persistence
AWS EC2 deployment
Debugging Docker, networking, and database issues

### Proof of Work
Screenshots of running containers and live application are available in the proof folder
Architecture diagram is available in the docs folder

### Project Scope
This project uses Django’s built-in template rendering for the user interface.
There is no separate React frontend.
The application is intentionally simple to emphasize deployment and infrastructure workflows.

### Author
Krish Chaudhari

This project uses Django’s built-in template rendering for the user interface.
There is no separate React frontend.
The application is intentionally simple to emphasize deployment and infrastructure workflows.

Author

Krish Chaudhari
