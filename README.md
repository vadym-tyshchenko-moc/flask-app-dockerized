# Flask App - Dockerized

This is Python web application with a single endpoint (/) exposed on port 8000.
The application is containerized using the Docker.

# Technology
- Python 3.13.0
- Flask 2.3.2
- Docker 27.2.0

# How to run without Docker?
1. Create the Virtual Environment:
```
$ python3 -m venv venv
```
<br>

2. Activate the Virtual Environment:
```
$ source venv/bin/activate  # on macOS and Linux

$ venv\Scripts\activate     # on Windows
```
<br>

3. Install Dependencies:
```
$ pip install -r requirements.txt
```
<br>

4. Run the Application:
```
python main.py
```
<br>

5. Test the Application
```
$ curl http://localhost:8000/
```
Expected result:
```
{"first_name":"Hyper","id":"90","last_name":"Skill"}
```

# How to run with the Docker?
1. Navigate to the project root directory and build the Image:
```
$ docker build -t flask-app .
```
<br>

2. Run the Docker Container:
```
$ docker run -d -p 8000:8000 flask-app
```
<br>

3. Test the Application:
```
$ curl http://localhost:8000/
```
Expected result:
```
{"first_name":"Hyper","id":"90","last_name":"Skill"}
```

# Licence
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
