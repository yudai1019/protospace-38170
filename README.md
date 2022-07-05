

| Column             | Type   | Options                   |
| -------------------| -------| --------------------------|
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false               |
| name               | string | null: false               |
| profile            | text   | null: false               |
| occupation         | text   | null: false               |
| pation             | text   | null: false               |


- has_many : prototypes
- has_many : comments

| Column             | Type       | Options                       |
| -------------------| -----------| ------------------------------|
| title              | string     | null: false                   |
| catch_copy         | text       | null: false                   |
| concept            | text       | null: false                   |
| user               | references | null: false, foreign_key: true|

- has_many : comments
- belongs_to : users

| Column             | Type       | Options                       |
| -------------------| -----------| ------------------------------|
| content            | text       | null: false                   |
| protoptype         | references | null: false, foreign_key: true|
| user               | references | null: false, foreign_key: true|

- belongs_to : users
- belongs_to : prototypes

