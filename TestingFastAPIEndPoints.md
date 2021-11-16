Testing FastAPI Endpoints
 

Once you have developed your Applications Programming Interfaces(APIs) using Fast API, the next step is to consider adding automated tests for your API endpoints. You can achieve this using pytest and a TestClient class derived from Starlette.

To get started, let’s consider a bare bones API that returns fruit information. 

```python
from fastapi import FastAPI, HTTPException
app = FastAPI()

fake_db = {}
fake_db[1] = "apple"
fake_db[2] = "banana"
fake_db[3] = "orange"

@app.get("/fruit/{id}")
async def echo(id: int):
    if id in fake_db:
        return {"fruit": fake_db[id]}
    else:
        raise HTTPException(status_code=404, detail="id not found")
``` 
Here I have created a fake database with just three fruit, and a single fruit/id endpoint. Let’s assume that this API is located in the api package, and we run it like so: 

```python
uvicorn api.fruit:app — reload 
```  

You can then try the endpoint by going to: http://localhost:8000/fruit/1 and verify that you get one apple back.
So far, so good. The next step is to add a test suite. To do so, we create a fastapi.testclient.TestClient object, and then define our tests via the standard pytest conventions. For example, we prefix each test method with test_ and use assert to validate responses from the API.

Here is sample code:

```python

from fastapi.testclient import TestClient
from api.fruit import app

client = TestClient(app)

def test_valid_id():
    response = client.get("/fruit/1")
    assert response.status_code == 200
    assert response.json() == {"fruit": "apple"}
```

Here we are calling fruit with an ID of 1, and verifying the response with assert. To run the test, just run pytest like so: 

```python
pytest 
```

Pytest will automatically collect all your tests and run them sequentially. If all goes well, you should also then see all your tests pass.
You can then easily add additional test cases for error conditions or edge cases.

For example, the following code tests for an invalid identifier:


 ```python
def test_invalid_id1():
    response = client.get("/fruit/99")
    assert response.status_code == 404
    assert response.json() == {'detail': 'id not found'}
```

And, the following code tests for a non-integer identifier: 

```python

def test_invalid_id2():
    response = client.get("/fruit/abc")
    assert response.status_code == 422
    assert response.json()["detail"][0]["msg"] == "value is not a valid integer"


Hopefully, you can now see how easy it is to add automated tests for your API endpoints. For further information, refer to the official FastAPI tutorial on Testing. 
