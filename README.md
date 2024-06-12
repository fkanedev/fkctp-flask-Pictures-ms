![Python](https://img.shields.io/badge/Python-3.9-blue.svg)
![Built with Flask](https://img.shields.io/badge/Built%20with-Flask-b5f05d.svg)
![Unit Tests](https://img.shields.io/badge/tests-passing-brightgreen.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

# Pictures Microservice Project

This project involves developing a microservice for managing pictures and implementing CRUD endpoints. Its primary goal is to showcase the practical application of Flask in a real-world scenario as part of my training in the [IBM Back-End Development Professional Certificate](https://www.coursera.org/professional-certificates/ibm-backend-development), utilizing a [template](https://github.com/ibm-developer-skills-network/luggb-Back-End-Development-Pictures) provided by IBM Developer Skills Network.

## Table of Contents
1. [Introduction](#introduction)
2. [Technologies Used](#technologies-used)
3. [Installation and Configuration](#installation-configuration)
4. [Usage](#usage)
5. [Development](#development)
6. [Testing](#testing)
7. [Sources](#sources)
8. [License](#license)
9. [Contact](#contact)

## 1. Introduction <a name="introduction"></a>

### Project Objective:
The main goal of this project is to create a microservice for retrieving and managing picture data and implementing CRUD (Create, Read, Update, Delete) endpoints using Flask. Since tests for the routes have been written in the [original template](https://github.com/ibm-developer-skills-network/luggb-Back-End-Development-Pictures) following the TDD process, the aim here is to implement the routes so that the code can pass all tests. This microservice, along with the [Songs Microservice](https://github.com/fkanedev/fkctp-flask-Song-ms), will be integrated into the backend of a [main application built with Django](https://github.com/fkanedev/fkctp-django-Music-Band-Site-ma-ui). The project demonstrates the usage and implementation of these technologies in a practical scenario.

### Key Features:
- Retrieve and manage picture data from a JSON file.
- Implement CRUD operations for managing picture data.
- Provide endpoints for health check, count, and CRUD operations.
- Utilize Flask framework for building the microservice.
- Integrate with a Django-based main application as part of a larger backend architecture.

## 2. Technologies Used <a name="technologies-used"></a>

### Programming Languages:
- Python 3.9

### Tools and Frameworks:
- Flask 2.2.2: A micro web framework for Python.
- pytest: A framework for testing Python code.
- gunicorn: A Python WSGI HTTP Server for UNIX.

## 3. Installation and Configuration <a name="installation-configuration"></a>

### Prerequisites:
- Python 3.9 installed on your system.
- Virtual environment tool (e.g., venv).

### Installation Steps:
1. Clone the GitHub repository:
    ```bash
    git clone https://github.com/fkanedev/fkctp-flask-Pictures-ms
    cd fkctp-flask-Pictures-ms
    ```

2. Create and activate a virtual environment:
    ```bash
    python3.9 -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Environment Configuration:
Ensure the Python environment is properly set up with Python 3.9. Dependencies should be installed via pip.

### Environment Variables:
- `FLASK_ENV=development`
- `MONGODB_SERVICE=localhost`
- `MONGODB_USERNAME=root`
- `MONGODB_PASSWORD=password`

## 4. Usage <a name="usage"></a>

### Usage Instructions:
To start the application, use the following command:
```bash
flask run
```
### Use Case Examples:
- Retrieve all pictures:
    ```bash
    curl --request GET -i -w '\n' --url http://localhost:5000/picture
    ```

- Retrieve a picture by ID:
    ```bash
    curl --request GET -i -w '\n' --url http://localhost:5000/picture/1
    ```

- Add a new picture:
    ```bash
    curl --request POST \
    -i -w '\n' \
    --url http://localhost:5000/picture \
    --header 'Content-Type: application/json' \
    --data '{
            "id": 323,
            "url": "http://example.com/image.png",
            "description": "Sample picture description."
        }'
    ```

- Update an existing picture:
    ```bash
    curl --request PUT \
    -i -w '\n' \
    --url http://localhost:5000/picture/1 \
    --header 'Content-Type: application/json' \
    --data '{
            "url": "http://example.com/updated_image.png",
            "description": "Updated picture description."
        }'
    ```

- Delete a picture:
    ```bash
    curl --request DELETE \
    -i -w '\n' \
    --url http://localhost:5000/picture/14 \
    --header 'Content-Type: "application/json"'
    ```
## 5. Development <a name="development"></a>

### Project Structure:
This backend project is primarily organized around the Flask framework. The directory structure includes the following folders:

- `backend/`: Contains the core of the microservice, specifically `routes.py`, which defines the API endpoints and their logic.
- `backend/data`: Contains the data about pictures, in `pictures.json` file.
- `tests/`: Contains the unit tests for the microservice, specifically `test_routes.py`, which tests the functionality of the API endpoints.

```plaintext
.
├── backend/
│   └── data/
│   │   └── pictures.json
│   ├── __init__.py
│   └── routes.py
├── bin/
│   └── ...
├── tests/
│   └── test_routes.py
├── LICENSE
├── README.md
├── requirements.txt
└── ....
```
### Data Model:
The data model for this project includes the following fields for a picture:

- id: Unique identifier for the picture.
- url: URL of the picture.
- description: Description of the picture.

### Testing:
Tests for the routes have been written using pytest in the original template. The objective is to implement the routes so that the code can pass all tests. To run the tests, use the following command:

```bash
pytest
```
This command will execute all the tests in the tests/ directory and provide a report of the results.

## Sources <a name="sources"></a>

- **Template: [IBM Developer Skills Network - Pictures microservice Template](https://github.com/ibm-developer-skills-network/luggb-Back-End-Development-Pictures)**

- **Useful links**:
  - **[Back-end Application Development Capstone Project](https://www.coursera.org/learn/backend-development-capstone-project/home/week/1)**
  - **[IBM Back-End Development Professional Certificate](https://www.coursera.org/professional-certificates/ibm-backend-development)**

## License <a name="license"></a>

This project is licensed under the MIT License - see the [LICENSE](/LICENSE) file for details.

## Contact <a name="contact"></a>

### Contact Information :

- Send me email : **fkanecloudtech@gmailcom**
- Connect with me on [LinkedIn](https://www.linkedin.com/in/your-profile/)
- Visit my [portfolio](https://yourname.github.io) to explore my projects and services.


### Contribution and Support :

Contributions are welcome. Please refer to the [CONTRIBUTING](/CONTRIBUTING) file for more information on how to contribute.
