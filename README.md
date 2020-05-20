## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|pw|string|null: false|
|e-mail|string|null: false|

### Association
- has_many :groups_users
- has_many :comments

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|text|null: false|

### Association
- has_many :groups_users
- has_many :comments


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## commentsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|picture|string|
|user_id|integer|foreign_key: true|
|group_id|integer|foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user