# py_docker_hello_world
Containerize simple python app

## Usage

Run the python script, like so:
```bash
docker build -t hello-world .
docker run -it --rm --name hello-world hello-world
```

If you prefer HTTP through Flask you can do this instead:

```bash
docker build -t hello-world .
docker run -it -e FLASK_APP=flask_hello_world.py -p 5000:5000 -e FLASK_RUN_HOST=0.0.0.0 --rm \ 
    --name hello-world hello-world flask run
```
