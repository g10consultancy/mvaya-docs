# User Onboarding - Student

## Student Register


**POST** `​/auth​/register/`


> Request Schema

    {
        "address": [
            {
                "line_1": "string",
                "line_2": "string",
                "landmark": "string",
                "city": "string",
                "zipcode": "string",
                "primary": true,
                "state": "Maharashtra",
                "country": "India"
            }
        ],
        "profile": {
            "board_id": 1,
            "grade_id": 1,
            "title": "string",
            "dob": "2020-04-20"
        },
        "guardian": [
            {
                "first_name": "string",
                "last_name": "string",
                "phone": "9876543210",
                "email": "string@abc.com",
                "relationship": 1
            }
        ],
        "password": 1234,
        "username": "str2i222ng2",
        "first_name": "string",
        "last_name": "string",
        "email": "use1r@exeample.com",
        "phone": "9876143211"
    }
    
    
> Response Schema (Successful)


    {
        "data": {
            "id": 83,
            "address": [
                {
                    "id": 1,
                    "city": "string",
                    "state": "Maharashtra",
                    "zipcode": "string",
                    "primary": true,
                    "line_1": "string",
                    "line_2": "string",
                    "landmark": "string",
                    "country": "India"
                }
            ],
            "profile": {
                "id": 1,
                "board": {
                    "id": 1,
                    "title": "SSC"
                },
                "grade": {
                    "id": 1,
                    "title": "1st"
                },
                "title": "string",
                "dob": "2020-04-20"
            },
            "guardian": [
                {
                    "id": 1,
                    "first_name": "string",
                    "last_name": "string",
                    "phone": "9876543210",
                    "email": "string@abc.com",
                    "relationship": 1
                }
            ],
            "email": "use1r@exeample.com",
            "phone": "9876143211",
            "user_type_char": "Student",
            "complete_name": "string string",
            "code": {
                "id": 1,
                "user": 83,
                "code": 280798
            },
            "last_login": null,
            "username": "str2i222ng2",
            "first_name": "string",
            "last_name": "string",
            "is_active": true,
            "date_joined": "2020-06-17T18:18:01.201351",
            "gender": null,
            "verified": null,
            "user_type": 1
        }
    }

---

**POST** `​/auth​/register/`

> Request Schema (Optional)

    {
        "profile": {
            "board_id": 1,
            "grade_id": 1,
            "title": "string",
            "dob": "2020-04-20"
        },
        "user_type": 1,
        "password": 1234,
        "username": "straqwi4n52l2g9",
        "first_name": "string",
        "last_name": "string",
        "email": "user@example.com",
        "phone": "9876993210"
    }
> Response Schema (Optional)

    {
        "data": {
            "id": 56,
            "address": [],
            "profile": {
                "id": 3,
                "board": {
                    "id": 1,
                    "title": "SSC"
                },
                "grade": {
                    "id": 1,
                    "title": "1st"
                },
                "title": "string",
                "dob": "2020-04-20"
            },
            "guardian": [],
            "email": "user@example.com",
            "phone": "9876993210",
            "user_type_char": "Student",
            "complete_name": "string string",
            "code": {
                "id": 3,
                "user": 56,
                "code": 168705
            },
            "last_login": null,
            "username": "straqwi4n52l2g9",
            "first_name": "string",
            "last_name": "string",
            "is_active": true,
            "date_joined": "2020-06-17T17:21:11.116851",
            "gender": null,
            "verified": null,
            "user_type": 1
        }
    }

## Check for unique email
**GET** `auth/user/unique_email_check/?email=user@example.com'`

Do no proceed without successful response.

> Response Schema (Successful)

    {
        "data": {
            "status": true
        }
    }

> Response Schema (UnSuccessful)

    {
        "data": {
            "status": false,
            "message": "This email is already taken."
        }
    }

---

## Check for unique phone number
**GET** `auth/user/unique_phone_check/?phone=9876543210`

Do no proceed without successful response.


> Response Schema (Successful)


    {
        "data": {
            "status": true
        }
    }


> Response Schema (UnSuccessful)


    {
        "data": {
            "status": false,
            "message": "This phone number is already taken."
        }
    }

---

## Check for unique username
**GET** `auth/user/unique_username_check/?username=mrprasla`

Do no proceed without successful response.


> Response Schema (Successful)


    {
        "data": {
            "status": true
        }
    }


> Response Schema (UnSuccessful)


    {
        "data": {
            "status": false,
            "message": "This username is already taken."
        }
    }

---

## Reminder

Incase if you let the user proceed `failing to pass the 3 checks above`, you'll face an error on the final registration API call.

Example:

    {
        "error": {
            "message": "Error in 3 fields.",
            "status": 400,
            "error": "Fields error",
            "error_code": 21,
            "description": "Fields error.",
            "fields": [
                {
                    "field": "email",
                    "message": [
                        "A user with that email already exists."
                    ]
                },
                {
                    "field": "phone",
                    "message": [
                        "A user with that phone number already exists."
                    ]
                },
                {
                    "field": "username",
                    "message": [
                        "A user with that username already exists."
                    ]
                }
            ]
        }
    }

---

## Failed Registration Check
 **POST** `​/auth​/user​/register/`
 
Sometimes, shit happens. This endpoint is used to check if a user was trying to register and for some reason he aborted
 the registration process due to lost connectivity or corrupt request.
 
> Request Schema

    {
        "phone": "9876543210",
        "email": "user@exeample.com"
    }

> Response Schema (OTP is Unverified)

This means the user already has an account but he/she is not verified by OTP. In this case, straightaway move the user 
to OTP verification screen and hit the resend OTP API mentioned below. The `user_id` is used to capture phone number 
from the failed account.

    {
        "data": {
            "user_id": 2,
            "status": "otp_unverified"
        }
    }

> Response Schema (OTP Verified)

The user is already OTP verified and he's trying to register again. Simply move him to login screen.

    {
        "data": {
            "status": "otp_verified"
        }
    }

---

## Verify OTP

**POST** `/auth/user/{user_id}/verify_otp/`
> Request Schema

    {
        "code": 417172
    }

> Response Schema (Successful)

    {
        "data": {
            "status": true
        }
    }


---

## Resend OTP

**GET** `/auth/user/{user_id}/resend_otp/`

> Response Schema (Successful)

    {
        "data": {
            "code": 417172
        }
    }

> Response Schema (Error)

In this case, the user does not exist.

    {
        "error": {
            "message": "No AppUser matches the given query.",
            "status": 404,
            "error": "Not Found",
            "error_code": 25,
            "description": "Object not found. The resource you are looking for does not exist or is deleted."
        }
    }

---