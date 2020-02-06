
## クラス図

※これはdbの作成順番も大事。外部キーがあるものは後

Room

has_many :users
has_many :messages

User
 email:string
 name:string
 age:string
 admin:boolean
 born:string

belongs_to room
has_many :message

Message
 body:string
 is_read:boolean

belongs_to room
belongs_to user
