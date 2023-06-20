# README
- 以下に、Postmanの設定方法とリクエストの送信方法の詳細な手順を示します。

1. 記事を取得するエンドポイント: GET /api/articles/:slug

   - リクエスト: GET http://localhost:3000/api/articles/how-to-train-your-dragon
   - 必要な場合は、ヘッダーに適切な認証情報を追加します。
   - レスポンス: 取得した記事の詳細情報がJSON形式で返されます。

2. 記事を作成するエンドポイント: POST /api/articles

   - リクエスト: POST http://localhost:3000/api/articles
   - ヘッダー: Content-Type: application/json
   - ボディ（RAW）:
     ```json
     {
       "article": {
         "title": "How to train your dragon",
         "description": "Ever wonder how?",
         "body": "You have to believe",
         "tagList": ["reactjs", "angularjs", "dragons"]
       }
     }
     ```
   - 必要な場合は、ヘッダーに適切な認証情報を追加します。
   - レスポンス: 作成された記事の詳細情報がJSON形式で返されます。

3. 記事を更新するエンドポイント: PUT /api/articles/:slug

   - リクエスト: PUT http://localhost:3000/api/articles/how-to-train-your-dragon
   - ヘッダー: Content-Type: application/json
   - ボディ（RAW）:
     ```json
     {
       "article": {
         "title": "Did you train your dragon?"
       }
     }
     ```
   - 必要な場合は、ヘッダーに適切な認証情報を追加します。
   - レスポンス: 更新後の記事の詳細情報がJSON形式で返されます。

4. 記事を削除するエンドポイント: DELETE /api/articles/:slug

   - リクエスト: DELETE http://localhost:3000/api/articles/how-to-train-your-dragon
   - 必要な場合は、ヘッダーに適切な認証情報を追加します。
   - レスポンス: 削除が成功した場合、ステータスコード204 No Contentが返されます。
# realworld_api
