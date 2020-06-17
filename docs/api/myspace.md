# Coaching/Online Classes & Instructor Profiles API

## Coaching Instructor (List & Detail)

**GET** `/auth/mycourses/`
    
> Response Schema (List)

    {
        "data": [
            {
                "id": 1,
                "name": "Khateeb Classes",
                "avatar": null,
                "courses": [
                    {
                        "id": 1,
                        "board": {
                            "id": 1,
                            "title": "CBSE"
                        },
                        "grade": {
                            "id": 1,
                            "title": "7th"
                        },
                        "subject": {
                            "id": 1,
                            "title": "Science"
                        },
                        "title": "Engineering Mechanics",
                        "featured": true,
                        "price": "29.99",
                        "image": null,
                        "language": 1,
                        "institute": 1,
                        "instructors": []
                    }
                ]
            }
        ]
    }


**GET** `/auth/mybatches/`

> Response Schema (List)


    {
        "data": [
            {
                "id": 1,
                "name": "Khateeb Classes",
                "avatar": null,
                "batches": [
                    {
                        "id": 1,
                        "board": {
                            "id": 1,
                            "title": "CBSE"
                        },
                        "grade": {
                            "id": 1,
                            "title": "7th"
                        },
                        "subject": {
                            "id": 1,
                            "title": "Science"
                        },
                        "title": "Engineering Mechanics",
                        "featured": true,
                        "price": "29.99",
                        "image": null,
                        "language": 1,
                        "institute": 1,
                        "instructors": []
                    }
                ]
            }
        ]
    }

---

## Online Instructor (List & Detail)

**GET** `/profile/online_instructor/`

> Response Schema (List)

    {
        "data": [
            {
                "id": 1,
                "name": "Stephane Maarek",
                "avatar": "http://165.22.214.137:8005/files/16122994_284f_14.jpg",
                "designation": "Kafka Guru, AWS Certified Developer",
                "organization": "Udemy"
            }
        ]
    }

**GET/PATCH/PUT/DELETE** `/profile/coaching_instructor/{coaching_instructor_id}`

> Response Schema (Detail)


    {
        "data": {
            "id": 1,
            "board": [
                {
                    "id": 1,
                    "title": "SSC"
                },
                {
                    "id": 2,
                    "title": "CBSE"
                }
            ],
            "grade": [
                {
                    "id": 5,
                    "title": "9th"
                },
                {
                    "id": 6,
                    "title": "10th"
                }
            ],
            "name": "Stephane Maarek",
            "description": "Stephane is a solutions architect, consultant and software developer that has a particular interest in all things related to Big Data, Cloud & API. He's also a many-times best seller instructor on Udemy for his courses in Apache Kafka and AWS.",
            "primary_contact": "123",
            "secondary_contact": "",
            "email": "abc@gmail.com",
            "avatar": "http://165.22.214.137:8005/files/16122994_284f_14.jpg",
            "status": false,
            "designation": "Kafka Guru, AWS Certified Developer",
            "organization": "Udemy",
            "start_date": "2020-04-10",
            "end_date": "2020-04-10",
            "online_institute": 1
        }
    }

---

## Coaching Institutes (List & Detail)
**GET** `/profile/coaching_institute/`

> Response Schema (List)

    {
        "data": [
            {
                "id": 1,
                "name": "Mahesh Tutorials",
                "avatar": "http://165.22.214.137:8005/files/mteducarelogo.png"
            }
        ]
    }

> Response Schema (Detail)

**GET/PATCH/PUT/DELETE** `/profile/coaching_institute/{coaching_institute_id}`


    {
        "data": {
            "id": 1,
            "board": [
                {
                    "id": 1,
                    "title": "SSC"
                },
                {
                    "id": 2,
                    "title": "CSBE"
                }
            ],
            "grade": [
                {
                    "id": 1,
                    "title": "7th"
                },
                {
                    "id": 2,
                    "title": "10th"
                }
            ],
            "batches": [
                {
                    "id": 2,
                    "board": {
                        "id": 1,
                        "title": "SSC"
                    },
                    "grade": {
                        "id": 1,
                        "title": "7th"
                    },
                    "subject": {
                        "id": 1,
                        "title": "English"
                    },
                    "category": {
                        "id": 1,
                        "title": "test"
                    },
                    "name": "string",
                    "code": "string",
                    "start_date": "2020-05-19",
                    "end_date": "2020-05-19",
                    "institute": 1
                },
                {
                    "id": 3,
                    "board": {
                        "id": 1,
                        "title": "SSC"
                    },
                    "grade": {
                        "id": 1,
                        "title": "7th"
                    },
                    "subject": {
                        "id": 1,
                        "title": "English"
                    },
                    "category": {
                        "id": 1,
                        "title": "test"
                    },
                    "name": "string",
                    "code": "str2ing",
                    "start_date": "2020-05-19",
                    "end_date": "2020-05-19",
                    "institute": 1
                }
            ],
            "courses": [
                {
                    "id": 1,
                    "board": {
                        "id": 1,
                        "title": "SSC"
                    },
                    "grade": {
                        "id": 1,
                        "title": "7th"
                    },
                    "subject": {
                        "id": 1,
                        "title": "English"
                    },
                    "title": "Goa — the state for your soul — literally!",
                    "image": null,
                    "institute": 1
                }
            ],
            "name": "John Doe",
            "description": "wwwww",
            "primary_contact": "9876543210",
            "secondary_contact": "",
            "email": "johndoe@outlook.com",
            "avatar": null,
            "status": true,
            "website": "https://mteducare.com/",
            "video": null,
            "banner": null,
            "android_app": true,
            "ios_app": true,
            "api_integration": true,
            "sale_type": 1
        }
    }
---

## Online Institutes (List & Detail)

**GET** `profile/online_institute/`

Do no proceed without successful response.


> Response Schema (Successful)

**GET/PATCH/PUT/DELETE** `profile/online_institute/{online_institute_id}`

> Response Schema (Detail)


---