# Technical Challenge BeenVerified

### Installation Proccess
This API uses Virtual Environment to perform the search, this allows to keep separate the dependencies in this project and the other
dependencies installed in the computer. :+1:

To install Virtual Environment:
```bash
    $ sudo pip install virtualenv
```

Then go to the directory where you have the project.
```bash
	$ cd path_to_my_project
```

Now setup the environment in this directory.
```bash
	$ virtualenv venv
```

In this point you have the enviroment ready to use it, just now activate it.
```bash
	$ source venv/bin/activate
```

You can know if you have correctly activated the environment because before your user name in the command line you can see the indicator (env).

Install the necessary dependencies into the activated environment.
```bash
	$ pip install flask flask-jsonpify flask-sqlalchemy flask-restful
```

### API REST Execution

Now just execute
```bash
	$ python songsearchapi.py
```

Finally to search the information just go to the web browser and type something like:

	http://127.0.0.1:5000/genre=Rock

This will return a result with the data in JSON format.
- Search by genre:  http://127.0.0.1:5000/genre=genre <br />
- Search by song:   http://127.0.0.1:5000/song=name <br />
- Search by artist: http://127.0.0.1:5000/artist=artist <br />
- Search by minimum and maximum length: http://127.0.0.1:5000/song/minimum=value1&maximum=value2 <br />
- Search genres information: http://127.0.0.1:5000/genre/info <br />

Note: The current port is the 5000 but if you have problems with it, you can change it in the API code to an unused port, please see last lines in API code. :smile:

### Deactivating Environment
When you finish using the API, to deactivate the environment just execute.
```bash
	$ deactivate
```

# Summary of bash commands
In your computer:
```bash
    $ sudo pip install virtualenv
    $ cd path_to_my_project
    $ virtualenv venv
    $ source venv/bin/activate
```
In the active environment:
```bash
    $ pip install flask flask-jsonpify flask-sqlalchemy flask-restful
    $ $ python songsearchapi.py
```
To deactivate the environment:
```bash
    $ deactivate
```

### Runnig .sh
If you are in the same directory of this Readme, you can just run the file Execution.sh and then go to the browser to the URLs mentioned above. :smirk:

### Dockerfile
A container allow us to keep separated the environment for the projects and share them with the developers or even with the clients if they want to have a copy of the project, Docker is opensource [Docker](https://www.docker.com/) . Here you have a Dockerfile to build your image and run the API.

To use the Dockerfile, in the currect directory of the Dockerfile you can do:
```bash
    $ docker build -t "repository_name:tag" .
```
Change repository_name for other of your preference and put the tag you like.

When the image is builded you can run it.
```bash
    $ docker run -d -p 5000:5000 container_id
```
Change container_id for the id of the builded image in the last step or use the image name.

### Thank You
Thanks **BeenVerified** for the opportunity :smile: and this challenge, I enjoyed a lot. :clap:  
