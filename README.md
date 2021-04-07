# Recipegram

# DB設計

## user
| Column        | Type      | Options                    |
| ------------- | --------- | -------------------------- |
| name          | string    | NOT NULL                   |
| profile       | text      | NOT NULL                   |
| profile_image | image     | NOT NULL                   | 
| email         | string    | NOT NULL                   | 
| password      | string    | NOT NULL                   |

### Association
- has_many :recipes



## recipe
| Column       | Type       | Options                    |
| ------------ | ---------- | -------------------------- |
| user         | references | foreign_key: true          |
| recipe_title | string     | NOT NULL                   |
| recipe_body  | text       | NOT NULL                   |

### Association
- belongs_to :user
