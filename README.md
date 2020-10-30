##ProtoSpaceのER図

＃＃usersテーブル
| Column     | Type    | Options          |
|------------|---------|------------------|
| email      | string  | null             |
| password   | string  | null             |
| name       | string  | null             |
| profile    | text    | null             |
| occupation | text    | null             |
| position   | text    | null             |

###Association
- has_many : comments
- has_many : prototypes

＃＃commentsテーブル
| Column     | Type       | Options          |
|------------|------------|------------------|
| text       | text       | null             |
| user       | references | null             |
| prototype  | references | null             |

###Association
- belongs_to : user
- belongs_to : prototype

＃＃prototypeテーブル
| Column     | Type       | Options          |
|------------|------------|------------------|
| title      | string     | null             |
| catch_copy | text       | null             |
| concept    | text       | null             |
| user       | references | null             |


###Association
- belongs_to : user
- has_many : comments