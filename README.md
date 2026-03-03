# 参考サイト
https://zenn.dev/redamoon/articles/article38-cursor-skills-rules-commands

# Cursorに簡単にインポートする方法
Cursorの「Rules, Skills, Subagents」のALLに以下のコマンドを設定してください。
```
# import-orders

## 概要
外部リポジトリの`.cursor`設定を現在のプロジェクトに統合します。

## 実行手順（ステップバイステップで実行してください）
1. ターミナルで `git clone https://github.com/KurisuWataru/cursor_orders cursor_orders_tmp` を実行する。
2. `cursor_orders_tmp/cursor` 内のファイル一覧を確認する。  
   ※ これは「参照元」であり、コピー先ではありません。
3. 以下のルールに従って、`cursor_orders_tmp/cursor` 配下のファイル、フォルダを構造を維持したまま **必ずプロジェクト直下の `.cursor`** にコピーする：
   - 既存のファイルがない場合は単にコピー。
   - 同名のファイルがある場合は、内容をマージするか上書きするかを、必ずユーザーに1つずつ確認する。
   - **`cursor` ディレクトリ（ドットなし）にはコピーしない。**
   - **プロジェクト直下の `.cursor`**が存在しない場合は作成する。
4. コピー完了後、`cursor_orders_tmp` ディレクトリを削除する。
```

# 注意点
Cursorの「Legacy Terminal Tool」を有効にしないと正しく動作しない場合があります。