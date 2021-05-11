```uml
@startuml

 未登録

ユーザー -> Webサーバー:ユーザー登録
Webサーバー -> DBサーバー:ユーザー登録
DBサーバー -> DBサーバー:登録処理

end

@enduml
```
