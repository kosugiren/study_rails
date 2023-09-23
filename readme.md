# Railsチュートリアルメモ

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
  - localhost:3000にアクセスし表示確認
  
  
  
