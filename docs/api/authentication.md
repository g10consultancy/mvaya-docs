# Mvaya Auth APIs

# Login

Endpoint - `​/auth​/user​/login​/`

##### Request Param

    {
      "username": "darshan",
      "password": "@dmin!23"
    }
    
##### Response Param (Successful)

    {
        "data": {
            "token": {
                "refresh": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTU4NzkxODMwNiwianRpIjoiNTBhMjQyMTY1ZDBkNDFjZjk1YmM2OWZiODg1YWZmMzMiLCJ1c2VyX2lkIjozfQ.BVeGLEnm7_NeqSpW0RikQ18GNhjL61oXEa80mtTY8YM",
                "access": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTg3NDg2MzA2LCJqdGkiOiJmNDRkZDkyYWE5ZjY0NDNmOThmNmJiYzY1MDI5MDBhOCIsInVzZXJfaWQiOjN9.WzsFalSeJlD8zMqtM6YhV4XD9BferiSs7Vh1xVGyNEw"
            },
            "user": {
                "id": 3,
                "avatar": null,
                "gender_str": "",
                "access": null,
                "groups": [],
                "last_login": null,
                "username": "darshan",
                "first_name": "",
                "last_name": "",
                "email": "",
                "is_active": true,
                "date_joined": "2020-04-16T21:42:37",
                "phone": "",
                "gender": ""
            }
        }
    }