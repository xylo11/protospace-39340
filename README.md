## ProtoApaceのER図
  
**usersテーブル**

| Column             | Type   | Null  | Key              |
| ------------------ | ------ | ----- | ---------------- |
| email              | string | false | uniqueness: true |
| encrypted_password | string | false | uniqueness: true |
| name               | string | false |                  |
| profile            | text   | false |                  |
| occupation         | text   | false |                  |
| position           | text   | false |                  |


**prototypesテーブル**

| Column     | Type       | Null  | Key                    |
| ---------- | ---------- | ----- | ---------------------- |
| title      | string     | false |                        |
| catch_copy | text       | false |                        |
| concept    | text       | false |                        |
| user       | references | false | foreign Key: users(id) |


**commentsテーブル**

| Column    | Type       | Null  | Key                         |
| --------- | ---------- | ----- | --------------------------- |
| content   | text       | false |                             |
| prototype | references | false | foreign Key: prototypes(id) |
| user      | references | false | foreign Key: users(id)      |

