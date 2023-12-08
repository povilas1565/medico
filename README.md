
# Medico

* Lets you create and record patient details using openEHR standards.
* Doctors can create and record an e-Prescription for the patients registered


## Tech Stack

**Client:** Flask Jinja2, Vanilla JS, CSS

**Server:** Flask

**Database:** Postgres SQL


## Features

- NGINX proxy server to route all requests to internal flask server
- WSGI load balaning with 3 worker nodes
- Docker Containerized
- CI/CD pipeline using Github Actions
- Automated using Selenium
- Unit tests with pytest
- Light/dark mode toggle


## Install and Run

To run the project, first clone the github repository -

```bash
  git clone https://github.com/povilas1565/medico.git
```
Then, change your working directory to medico

```bash
  cd medico
```
Finally run the project by -
```bash
  sudo docker-compose up --build -d
```
At last, just initialize the database by entering into running docker container -
```bash
  sudo docker exec -it medico_web_1 /bin/bash
  python3
``` 
```bash
  >>> from flaskproject import db 
  >>> db.create_all()
``` 
## Running Tests

Test stage comprises of unit tests(testing view functions and database models) and functional tests(testing flask app routes).

To run tests, run the following command -

```bash
  python3 -m pytest -v
```


## CI/CD Workflow

https://github.com/SJDev2000/medico/blob/main/.github/workflows/main-action.yml

* test-and-build - Run tests and build docker image upon successful test run, that will be published to 




