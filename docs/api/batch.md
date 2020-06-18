# Batches


## Batch (Create, List & Detail)

**POST/GET/PATCH/PUT/DELETE** `panel/batch/{batch_id}/`

KEY | VALUE | DESCRIPTION
------------ | ------------- | ------------
type | 1  | Regular
type | 2  | Competitive Exam
type | 3  | Language Skill
type | 4  | Other
session | 1  | Regular
session | 2  | Live
    
> Request Schema

    {
        "board_id": 2,
        "grade_id": 5,
        "subject_id": 5,
        "title": "string",
        "featured": false,
        "price": 500,
        "start": "2020-06-18",
        "end": "2020-06-18",
        "type": [
            "1",
            "2"
        ],
        "session": 1
    }
    
> Response Schema (List)

    {
      "data": [
        {
          "id": 10,
          "board": {
            "id": 2,
            "title": "CBSE"
          },
          "grade": {
            "id": 5,
            "title": "5th"
          },
          "subject": {
            "id": 5,
            "title": "Pcm"
          },
          "type": [
            "1",
            "2"
          ],
          "students": [
            
          ],
          "type_str": "Regular, Competitive Exam",
          "session_str": "Regular",
          "title": "string",
          "featured": false,
          "price": 500,
          "start": "2020-06-18",
          "end": "2020-06-18",
          "session": 1
        },
        {
          "id": 11,
          "board": {
            "id": 2,
            "title": "CBSE"
          },
          "grade": {
            "id": 5,
            "title": "5th"
          },
          "subject": {
            "id": 5,
            "title": "Pcm"
          },
          "type": [
            "1",
            "2"
          ],
          "students": [
            
          ],
          "type_str": "Regular, Competitive Exam",
          "session_str": "Regular",
          "title": "string",
          "featured": false,
          "price": 500,
          "start": "2020-06-18",
          "end": "2020-06-18",
          "session": 1
        }
      ]
    }


> Response Schema (Detail)

    {
        "data": {
            "id": 11,
            "board": {
                "id": 2,
                "title": "CBSE"
            },
            "grade": {
                "id": 5,
                "title": "5th"
            },
            "subject": {
                "id": 5,
                "title": "Pcm"
            },
            "type": [
                "1",
                "2"
            ],
            "students": [],
            "type_str": "Regular, Competitive Exam",
            "session_str": "Regular",
            "title": "string",
            "featured": false,
            "price": 500,
            "start": "2020-06-18",
            "end": "2020-06-18",
            "session": 1
        }
    }

---

## Add Student to Batch 

**POST** `panel/batch/3/add_student/`

> Request Schema (List)

    {
        "students": [
            1,
            2,
            3
        ]
    }

> Response Schema

--Empty Response--

---
