# Fast Api Server

Simple API server created to learn Python and FastAPI.

## Creation
### Libraries
You need to have Python 3.6 or higher installed, along with `pip`. Next, install `fastapi` and `uvicorn`.

```
pip install fastapi "uvicorn[standard]"
```

Note: standard version of uvicorn is needed to get some additional libraries that will be necessary.

### File creation
Create a very simple server by setting up a `main.py` file.
```py
from typing import Optional

from fastapi import FastAPI

app = FastAPI()


@app.get("/")
def read_root():
    return {"Hello": "World"}

```

### Run
Run the server with:
```sh
uvicorn main:app --reload
```

Ready! Now check http://127.0.0.1:8000 at your browser.

## Docs
A Swagger documentation has also been created automatically for your app. Check http://127.0.0.1:8000/docs.

## Types
Types can be added with the use of `pydantic`. 

## Technologies

-   [Pydantic](https://pydantic-docs.helpmanual.io/)
-   [FastAPI](https://fastapi.tiangolo.com/)
-   [Uvicorn](https://www.uvicorn.org/)