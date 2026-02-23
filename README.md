# FastAPI Beyond CRUD 

This is the source code for the [FastAPI Beyond CRUD](https://youtube.com/playlist?list=PLEt8Tae2spYnHy378vMlPH--87cfeh33P&si=rl-08ktaRjcm2aIQ) course. The course focuses on FastAPI development concepts that go beyond the basic CRUD operations.

For more details, visit the project's [website](https://jod35.github.io/fastapi-beyond-crud-docs/site/).

## Table of Contents

1. [Getting Started](#getting-started)
2. [Prerequisites](#prerequisites)
3. [Project Setup](#project-setup)
4. [Running the Application](#running-the-application)
5. [Running Tests](#running-tests)
6. [Contributing](#contributing)

## Getting Started
Follow the instructions below to set up and run your FastAPI project.

### Prerequisites
Ensure you have the following installed:

- Python >= 3.10
- PostgreSQL
- Redis

### Project Setup
1. Clone the project repository:
    ```bash
    git clone https://github.com/jod35/fastapi-beyond-CRUD.git
    ```
   
2. Navigate to the project directory:
    ```bash
    cd fastapi-beyond-CRUD/
    ```

3. Create and activate a virtual environment:
    ```bash
    python3 -m venv env
    source env/bin/activate
    ```

4. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

5. Set up environment variables by copying the example configuration:
    ```bash
    cp .env.example .env
    ```

6. Run database migrations to initialize the database schema:
    ```bash
    alembic upgrade head
    ```

7. Open a new terminal and ensure your virtual environment is active. Start the Celery worker (Linux/Unix shell):
    ```bash
    sh runworker.sh
    ```

## Running the Application
Start the application:

```bash
fastapi dev src/
```
Alternatively, you can run the application using Docker:
```bash
docker compose up -d
```
## Running Tests
Run the tests using this command
```bash
pytest
```
##Updated ReadMe
	1.Forked the original repository and cloned it locally.
	2.Ran docker compose up --build to rebuild the container and start the application.
	3.Resolved Docker runtime error related to missing FastAPI executable.
	4.Fixed dependency issues in requirements.txt during Docker build.
	5.Created .github/workflows directory for GitHub Actions.
	6.Implemented Conventional Commit validation workflow.
	7.Configured workflow to automatically close PRs on commit validation failure.
	8.Added Ethereal SMTP email notification for failed validation.
	9.Committed and pushed the Conventional Commit workflow.
	10.Created a test branch (test-commit-check) to validate failure behavior.
	11.Verified PR auto-closing and failure screenshot.
	12.Implemented nightly build workflow on the main branch.
	13.Configured Docker build and pytest test execution in CI.
	14.Resolved missing pytest dependency in container.
	15.Configured GHCR authentication and image push.
	16.Verified successful image publication in GitHub Packages.



## Contributing
I welcome contributions to improve the documentation! You can contribute [here](https://github.com/jod35/fastapi-beyond-crud-docs).
