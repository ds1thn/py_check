# py_check

## How to use

### Python formater  
    docker run --rm -it -v `pwd`:/code pan1c/py_check:1.0.2 black --check .

### Python linter
    docker run --rm -it `pwd`:/code pan1c/py_check:1.0.2 python3 -m flake8 --statistics --count .
