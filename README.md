# Securing FastAPI with JWT Token-based Authentication

### Want to learn how to build this?

Check out the [post](https://testdriven.io/blog/fastapi-jwt-auth/).

## Want to use this project?

1. Fork/Clone

1. Create and activate a virtual environment:

    ```sh
    $ python3 -m venv venv && source venv/bin/activate
    ```

1. Install the requirements:

    ```sh
    (venv)$ pip install -r requirements.txt
    ```

1. Run the app:

    ```sh
    (venv)$ python main.py
    ```

1. Test at [http://localhost:8081/docs](http://localhost:8081/docs)

1. Login to get token by post:
    ```sh
    curl -X 'POST' \
    'http://127.0.0.1:8081/user/login' \
    -H 'accept: application/json' \
    -H 'Content-Type: application/json' \
    -d '{
    "email": "abdulazeez@x.com",
    "password": "weakpassword"
    }'
    ```

1. Test authorization by post:
    ```sh
    curl -X 'POST' \
    'http://127.0.0.1:8081/{{api-url}}' \
    -H 'accept: application/json' \
    -H 'Content-Type: application/json' \
    -H 'Authorization: Bearer {{access_token}}' \
    -d '{data}'
    ```
