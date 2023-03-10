# Django REST framework Email API

This is a Django-based RESTful API for sending emails. It allows you to send emails by making POST requests to the API with the required data in JSON format.

## Prerequisites

* Docker
* Docker Compose

## Installation

1. Clone the repository:

    ```bash
    git clone git@github.com:datumbrain/django-rest-emailapi.git
    ```
2. Navigate to the project directory:

    ```bash
    cd django-rest-emailapi
    ```
    Open the project in your code editior.

3. Create a virtual environment in the project root directory and activate it.

    ```bash
    python3 -m venv env
    source env/bin/activate
    ```

5. In the project navigate to settings.py file (project path/emailapi/settings.py)and set the values of `SECRET_KEY`, `EMAIL_HOST_USER` and `EMAIL_HOST_PASSWORD` with your own email credentials.

6. Run the Docker containers:

    ```bash
    docker-compose up -d
    ```

7. Visit http://0.0.0.0:8000/email in your web browser to access the email API.


## API Endpoints

### POST /email/
This endpoint sends an email with the provided data in JSON format. Required fields: to_email, subject, body, from_email.

## Response

On success, the API returns a 200 OK response with the message "Email sent".

On failure, the API returns a 400 Bad Request response with the error message or a 500 with a message "Email sending failed".

