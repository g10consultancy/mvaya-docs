# Online Institutes

This related to all forms on Online content. Also knows as online classes/providers.

## Institute (List & Detail)

**GET** `/profile/online/institute/`
    
> Response Schema (List)

    {
        "data": [
            {
                "id": 1,
                "name": "Byju's",
                "avatar": "http://127.0.0.1:8000/files/byjus-logo-E37962D240-seeklogo.com.png"
            },
            {
                "id": 2,
                "name": "Toppr",
                "avatar": "http://127.0.0.1:8000/files/Toppr_logo.png"
            },
            {
                "id": 3,
                "name": "Vedantu",
                "avatar": "http://127.0.0.1:8000/files/Vedantulogo_orange.png"
            },
            {
                "id": 4,
                "name": "Robomate",
                "avatar": "http://127.0.0.1:8000/files/robomate_logo.png"
            },
            {
                "id": 5,
                "name": "Khab Academy",
                "avatar": "http://127.0.0.1:8000/files/1200x630wa.png"
            },
            {
                "id": 6,
                "name": "Ataz Learning",
                "avatar": "http://127.0.0.1:8000/files/ataz.png"
            },
            {
                "id": 7,
                "name": "Meritnation",
                "avatar": "http://127.0.0.1:8000/files/merithnation.png"
            },
            {
                "id": 8,
                "name": "Simplilearn",
                "avatar": "http://127.0.0.1:8000/files/simplilear_logo.png"
            },
            {
                "id": 9,
                "name": "Age of Learning",
                "avatar": "http://127.0.0.1:8000/files/age_of_laraning_logo.jpg"
            },
            {
                "id": 10,
                "name": "Enduguru",
                "avatar": "http://127.0.0.1:8000/files/enduguru_logo.jpeg"
            }
        ]
    }
**GET** `/profile/online/institute/1/`


> Response Schema (Detail)

    {
        "data": {
            "id": 1,
            "board": [
                {
                    "id": 16,
                    "title": "BSE "
                },
                {
                    "id": 26,
                    "title": "BSEB"
                },
                {
                    "id": 31,
                    "title": "SSLC"
                },
                {
                    "id": 30,
                    "title": "KSEEB"
                },
                {
                    "id": 22,
                    "title": "HSC"
                }
            ],
            "grade": [
                {
                    "id": 1,
                    "title": "1st"
                },
                {
                    "id": 2,
                    "title": "2nd"
                },
                {
                    "id": 3,
                    "title": "3rd"
                },
                {
                    "id": 12,
                    "title": "12th"
                }
            ],
            "instructors": [
                {
                    "id": 1,
                    "first_name": "Prof Salim",
                    "last_name": "Khan",
                    "avatar": null
                },
                {
                    "id": 3,
                    "first_name": "Prof Neeraj",
                    "last_name": "Singhaniya",
                    "avatar": "http://165.22.214.137:8005/files/enduguru_logo_RrFJIg3.jpeg"
                }
            ],
            "courses": [
                {
                    "id": 1,
                    "board": {
                        "id": 26,
                        "title": "BSEB"
                    },
                    "grade": {
                        "id": 6,
                        "title": "6th"
                    },
                    "subject": {
                        "id": 24,
                        "title": "Legal Studies"
                    },
                    "language": {
                        "id": 8,
                        "title": "Urdu"
                    },
                    "title": "English",
                    "featured": true,
                    "price": "2999.00",
                    "image": null,
                    "institute": 1
                }
            ],
            "type_str": "Regular, Competitive Exam, Other",
            "language": [
                {
                    "id": 1,
                    "title": "English"
                },
                {
                    "id": 1,
                    "title": "Maths"
                }
            ],
            "featured": true,
            "status": true,
            "name": "Byju's",
            "description": "BYJU'S is the world's most valuable ed-tech company and the creator of India's most loved school learning app. Launched in 2015, BYJU'S offers highly personalised and effective learning programs for classes 1 - 12 (K-12), and aspirants of competitive exams like JEE, IAS etc. With 50 million registered students and 3.5 million paid subscriptions, BYJU'S has become one of the most preferred education platforms across the globe.",
            "avatar": "http://127.0.0.1:8000/files/byjus-logo-E37962D240-seeklogo.com.png",
            "website": "https://byjus.com/",
            "banner": "http://127.0.0.1:8000/files/top-banner.jpg",
            "video": "http://127.0.0.1:8000/files/What_is_BYJUS_The_Learning_App.mp4"
        }
    }

---

## Instructor (List & Detail)

**GET** `/profile/online/instructor/`

> Response Schema (List)

    {
        "data": [
            {
                "id": 1,
                "first_name": "Prof Sandesh",
                "last_name": "Sankhare",
                "avatar": null
            },
            {
                "id": 3,
                "first_name": "Prof Neeraj",
                "last_name": "Singhaniya",
                "avatar": "http://165.22.214.137:8005/files/enduguru_logo_RrFJIg3.jpeg"
            },
            {
                "id": 4,
                "first_name": "Prof Darshan",
                "last_name": "Gupta",
                "avatar": "http://165.22.214.137:8005/files/unnamed.jpg"
            },
            {
                "id": 5,
                "first_name": "Prof Salim",
                "last_name": "Vishwakarma",
                "avatar": "http://165.22.214.137:8005/files/images.jpeg"
            }
        ]
    }

**GET** `/profile/online/instructor/1/`


> Response Schema (Detail)

    {
        "data": {
            "id": 4,
            "board": [
                {
                    "id": 18,
                    "title": "TNBSE"
                },
                {
                    "id": 22,
                    "title": "HSC"
                },
                {
                    "id": 45,
                    "title": "IGCSE"
                }
            ],
            "grade": [
                {
                    "id": 9,
                    "title": "9th"
                },
                {
                    "id": 10,
                    "title": "10th"
                }
            ],
            "education": [
                {
                    "id": 6,
                    "start": "2020-06-24",
                    "end": "2020-06-17",
                    "location": "Mumbai",
                    "logo": "http://165.22.214.137:8005/files/565vBdDA_rvVS0yP.png",
                    "institute": "Raheja",
                    "degree": "MBA",
                    "instructor": 4
                },
                {
                    "id": 5,
                    "start": "2020-06-03",
                    "end": "2020-06-28",
                    "location": "Mumbai",
                    "logo": "http://165.22.214.137:8005/files/GNl8b1uw.png",
                    "institute": "Shree Swaminarayan Gurukul International",
                    "degree": "HSC",
                    "instructor": 4
                },
                {
                    "id": 4,
                    "start": "2020-06-02",
                    "end": "2020-06-29",
                    "location": "Mumbai",
                    "logo": "http://165.22.214.137:8005/files/KApLLTyA_fDbp5DV.png",
                    "institute": "The Doon School",
                    "degree": "SSC",
                    "instructor": 4
                }
            ],
            "experience": [
                {
                    "id": 3,
                    "start": "2020-06-02",
                    "end": "2020-06-30",
                    "location": "Dehli",
                    "logo": "http://165.22.214.137:8005/files/KApLLTyA_TJYGcZn.png",
                    "title": "Vendatu",
                    "company": "institute",
                    "description": "Vedantu is India's leading Online tutoring company which enables students to learn LIVE with some of India's best-curated teachers. ... Vedantu's online tutoring platform enables LIVE interactive learning between a teacher and a student. It offers individual and group classes.",
                    "instructor": 4
                },
                {
                    "id": 2,
                    "start": "2020-06-15",
                    "end": "2020-06-30",
                    "location": "Patna",
                    "logo": "http://165.22.214.137:8005/files/iXcVJU9A_COuFJoZ.png",
                    "title": "Aakash",
                    "company": "couching",
                    "description": "AAKASH. Aakash Educational Services Limited (AESL) is a leading educational institution in India that provides comprehensive test preparatory services to students preparing for medical and engineering entrance exams, school/board exams, KVPY, NTSE, Olympiads and other Foundation level exams.",
                    "instructor": 4
                }
            ],
            "courses": [
                {
                    "id": 8,
                    "board": {
                        "id": 2,
                        "title": "CBSE"
                    },
                    "grade": {
                        "id": 3,
                        "title": "3rd"
                    },
                    "subject": {
                        "id": 1,
                        "title": "English"
                    },
                    "language": {
                        "id": 1,
                        "title": "English"
                    },
                    "title": "English Course for III Standard",
                    "featured": false,
                    "price": "7000.00",
                    "image": null,
                    "institute": 5
                },
                {
                    "id": 9,
                    "board": {
                        "id": 29,
                        "title": "GSEB"
                    },
                    "grade": {
                        "id": 12,
                        "title": "12th"
                    },
                    "subject": {
                        "id": 35,
                        "title": "Engineering Drawing"
                    },
                    "language": {
                        "id": 1,
                        "title": "English"
                    },
                    "title": "Engineering Drawing for XII",
                    "featured": true,
                    "price": "9000.00",
                    "image": null,
                    "institute": 8
                },
                {
                    "id": 10,
                    "board": {
                        "id": 30,
                        "title": "KSEEB"
                    },
                    "grade": {
                        "id": 8,
                        "title": "8th"
                    },
                    "subject": {
                        "id": 2,
                        "title": "Maths"
                    },
                    "language": {
                        "id": 1,
                        "title": "English"
                    },
                    "title": "Maths for VIII Standard",
                    "featured": true,
                    "price": "7000.00",
                    "image": null,
                    "institute": 7
                }
            ],
            "language": [
                {
                    "id": 1,
                    "title": "English"
                },
                {
                    "id": 2,
                    "title": "Marathi"
                }
            ],
            "first_name": "Prof Darshan",
            "last_name": "Gupta",
            "phone": "9275384673",
            "email": "Darshan@gmail.com",
            "avatar": "http://165.22.214.137:8005/files/unnamed.jpg",
            "start": "2020-06-17",
            "end": "2020-06-30",
            "status": true,
            "institute": 2
        }
    }

---

## Courses
**GET** `/profile/online/courses/`

**Available Filters** 


KEY | VALUE | DESCRIPTION
------------ | ------------- | ------------
price_min | 300  | You need to use `price_max` if you use this filter
price_max | 600  | You need to use `price_min` if you use this filter
grade | 1  | Pass ID of the parameter
subject | 2  | Pass ID of the parameter
board | 5  | Pass ID of the parameter


> Response Schema (List w/ Pagination)


    {
        "page": 1,
        "next_page": 2,
        "next_page_link": "http://165.22.214.137:8005/profile/online/courses/?page=2",
        "previous_page": null,
        "previous_page_link": null,
        "count": 10,
        "max_pages": 2,
        "total_count": 2,
        "data": [
            {
                "id": 1,
                "board": {
                    "id": 1,
                    "title": "SSC"
                },
                "grade": {
                    "id": 9,
                    "title": "9th"
                },
                "subject": {
                    "id": 2,
                    "title": "Maths"
                },
                "language": {
                    "id": 1,
                    "title": "English"
                },
                "title": "Knowing Numbers",
                "featured": true,
                "price": "2500.00",
                "image": null,
                "institute": 1
            },
            {
                "id": 2,
                "board": {
                    "id": 20,
                    "title": "BSEM"
                },
                "grade": {
                    "id": 12,
                    "title": "12th"
                },
                "subject": {
                    "id": 33,
                    "title": "Biotechnology"
                },
                "language": {
                    "id": 1,
                    "title": "English"
                },
                "title": "Bioteachnology for XII Science",
                "featured": true,
                "price": "2500.00",
                "image": null,
                "institute": 3
            },
            {
                "id": 5,
                "board": {
                    "id": 27,
                    "title": "UBSE"
                },
                "grade": {
                    "id": 9,
                    "title": "9th"
                },
                "subject": {
                    "id": 14,
                    "title": "History"
                },
                "language": {
                    "id": 1,
                    "title": "English"
                },
                "title": "History for IX Standard",
                "featured": false,
                "price": "3000.00",
                "image": null,
                "institute": 5
            },
            {
                "id": 6,
                "board": {
                    "id": 3,
                    "title": "ICSE"
                },
                "grade": {
                    "id": 12,
                    "title": "12th"
                },
                "subject": {
                    "id": 34,
                    "title": "Computer Science"
                },
                "language": {
                    "id": 1,
                    "title": "English"
                },
                "title": "Computer Science for XII",
                "featured": true,
                "price": "8000.00",
                "image": null,
                "institute": 6
            },
            {
                "id": 7,
                "board": {
                    "id": 1,
                    "title": "SSC"
                },
                "grade": {
                    "id": 5,
                    "title": "5th"
                },
                "subject": {
                    "id": 1,
                    "title": "English"
                },
                "language": {
                    "id": 1,
                    "title": "English"
                },
                "title": "English Course for V Standard",
                "featured": false,
                "price": "5000.00",
                "image": null,
                "institute": 10
            },
            {
                "id": 9,
                "board": {
                    "id": 29,
                    "title": "GSEB"
                },
                "grade": {
                    "id": 12,
                    "title": "12th"
                },
                "subject": {
                    "id": 35,
                    "title": "Engineering Drawing"
                },
                "language": {
                    "id": 1,
                    "title": "English"
                },
                "title": "Engineering Drawing for XII",
                "featured": true,
                "price": "9000.00",
                "image": null,
                "institute": 8
            },
            {
                "id": 10,
                "board": {
                    "id": 30,
                    "title": "KSEEB"
                },
                "grade": {
                    "id": 8,
                    "title": "8th"
                },
                "subject": {
                    "id": 2,
                    "title": "Maths"
                },
                "language": {
                    "id": 1,
                    "title": "English"
                },
                "title": "Maths for VIII Standard",
                "featured": true,
                "price": "7000.00",
                "image": null,
                "institute": 7
            }
        ]
    }

**GET** `/profile/online/courses/1/`

> Response Schema (Detail)

    {
        "data": {
            "id": 2,
            "board": {
                "id": 20,
                "title": "BSEM"
            },
            "grade": {
                "id": 12,
                "title": "12th"
            },
            "subject": {
                "id": 33,
                "title": "Biotechnology"
            },
            "language": {
                "id": 1,
                "title": "English"
            },
            "title": "Bioteachnology for XII Science",
            "featured": true,
            "price": "2500.00",
            "image": null,
            "institute": 3
        }
    }

