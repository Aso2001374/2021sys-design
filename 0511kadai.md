```uml
@startuml

opt 未登録

ユーザー -> Webサーバー:ユーザー登録
Webサーバー -> DBサーバー:ユーザー登録
DBサーバー -> DBサーバー:登録処理

  alt 登録成功
    Webサーバー ->ユーザー:登録メッセージの表示
  else 登録失敗
  end
  
end

@enduml
```
