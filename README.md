
# Task Scheduler (Only works in Linux)

This is a task scheduler project built using Django and Celery. It allows you to schedule tasks and execute them asynchronously.

## Installation

### 1. Set up Virtual Environment

First, create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2. Install Dependencies

Install all required packages using pip:

```bash
pip install -r requirements.txt
```

### 3. Database Migration

Apply migrations to set up the database:

```bash
python manage.py migrate
```

## Usage

### 1. Run Django Server

Start the Django development server:

```bash
python manage.py runserver
```

This will run the server locally at http://127.0.0.1:8000/.

### 2. Run Celery Beat Scheduler

Celery Beat is a scheduler that sends messages to the message broker at specified intervals. Start the Celery Beat scheduler:

```bash
celery -A myceleryproject beat -l info
```

### 3. Run Celery Worker

Celery Worker is responsible for executing tasks. Start the Celery Worker:

```bash
celery -A myceleryproject worker -l info
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)
```

Feel free to customize the instructions and add more details as needed for your specific project setup.