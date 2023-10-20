# Railsチュートリアル メモ

## 第1章

### 環境設定からhello, worldまで

  - ウェブからWindows向けのRuby3.1.4をインストール  
    ※MSYS2 Setup Wizardを忘れずに実施
  - ruby on rails インストール
  ```
  gem install rails -v 7.0.4
  ```
  - bundlerのバージョンを指定してインストール
  ```
  gem install bundler -v 2.3.14
  ```
  - アプリ作成
  ```
  rails _7.0.4_ new hello_app --skip-bundle
  ```
  - Gemfileを編集しgemインストール  
    ※編集方法はチュートリアルサイト参照
  ```
  bundle _2.3.14_ install
  ```
  - サーバー起動
  ```
  rails server
  ```
  or
  ```
  rails s
  ```
  - localhost:3000にアクセスし表示確認
  - hello, worldを表示させる
    - app/controllers/application_controller.rbを編集（Applicationコントローラにhelloを追加する）
    ```
    class ApplicationController < ActionController::Base
      def hello
        render html: "hello, world!"
      end
    end
    ```
    - config/routes.rbを編集（ルートルーティングを設定する）
    ```
    Rails.application.routes.draw do
      root "application#hello"
    end
    ```
    - サーバーを起動しブラウザにアクセスする

## 第２章

```
rails generate scaffold User name:string email:string
```
```
rails db:migrate
```
```
http://localhost:3000/users
```
