# hnh

### predict 
```
from typing import Union
from fastapi import FastAPI
import random

app = FastAPI()


@app.get("/")
def read_root():
    return {"Hello": "Hotdog prediction!"}


@app.get("/hotdog")
def prediction():

    hdg = random.randint(0, 1)

    if hdg==1:
        result = "hotdog"
    else:
        result = "not hotdog"

    return {
            "prediction": result,
            "num" : hdg
            }
```
![image](https://github.com/user-attachments/assets/3fa1d1fc-b3f4-4a7c-ae15-ae6984da3526)

