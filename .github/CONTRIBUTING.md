# プルリクエスト(Pull Request)の作成手順
## 1.マージ先を指定する

- マージ元`compare:`が正しいことを確認する（主にfeatureブランチ）。
- マージ先`base:`を指定する（主にdevelopブランチ）。

## 2.タイトルを入力する

タイトルだけで対応の内容が把握できるように記載すること

## 3.コメントを入力する

- テンプレートに従い実装・修正内容を記載する
- 必要に応じてテンプレートの項目は変更して良い。ただし、レビュアーや後で読んだ人が内容がわかるようにすること

:warning: コメントに記載する情報についてはルール化することによる弊害が大きいため、ルールの設定はしません。  
一般的に記載した方が良い情報については下記URLが参考になるので意識しておくこと。

#### 参考URL
- [チーム開発におけるプルリクの作法](https://qiita.com/ikuwow/items/fb52a54c086398eb5b92#%E3%83%97%E3%83%AB%E3%83%AA%E3%82%AF%E3%82%A8%E3%82%B9%E3%83%88%E3%81%AB%E5%BF%85%E8%A6%81%E3%81%AA%E6%83%85%E5%A0%B1%E3%82%92%E5%85%A5%E3%82%8C%E3%82%88%E3%81%86)

## 4.Assignee & Reviewer

- assign yourselfをクリックし、**自分をAssignees**に追加する
- **レビュー担当者二人をReviewersに**追加する

※その他にコメントが欲しい人がいる場合はメンションをつけて知らせる

## 5.ラベルを指定する

### WIP（Work In Progress）
修正中のため、まだレビューをしなくても良い場合に指定する

### 優先度（高）
優先度が高く、急ぎレビューが必要な場合に指定する

## 6.プルリクエストの作成
入力内容に間違いがないことを確認し、「Create Pull Request」をクリックする。

#### 参考URL
- [プルリクエストの作成方法](https://help.github.com/ja/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request#creating-the-pull-request)
- [GitHubでのプルリクエスト活用方法まとめ](https://ics.media/entry/14449/)

## コンフリクト時の対応について

- プルリクを出した際にコンフリクトが発生した場合は、ローカルで修正を行い動作確認を行った後、修正をpushすること。
    - 不明点があれば、コンフリクトが発生した箇所の修正担当者に確認を行い修正を行うこと。（自明な修正であれば自分で対応しても良い）
    - :exclamation: 当然のことながら、自分の修正を優先して過去の対応を消すのはNG


# レビュー担当者の対応
## 1. レビューの実施
レビューを実施し、問題がある箇所についてはコメントする

#### 参考URL
- [プルリクエストへコメントする](https://help.github.com/ja/github/collaborating-with-issues-and-pull-requests/commenting-on-a-pull-request)

## 2.プルリクの承認・マージ
- 自分が一人目のレビュー担当者であれば、「File Changed」タブ「Review Changes」ボタンの「Approve」を選択し、プルリクを承認する

#### 参考URL
- [必須レビューでのプルリクエストの承認](https://help.github.com/ja/github/collaborating-with-issues-and-pull-requests/approving-a-pull-request-with-required-reviews)

- 自分が最後のレビュー担当であれば、マージ先が正しいことを確認し、「Merge Pull Request」をクリックしマージを行う。

※マージ後、マージ元ブランチは特に必要がなければ削除する

#### 参考URL
- [プルリクエストをマージする](https://help.github.com/ja/github/collaborating-with-issues-and-pull-requests/merging-a-pull-request)

## :warning: レビュー担当者に求めてはいけないこと
- バグを発見してくれること
- 仕様通りに動作すること

-> 実装者がしっかりと仕様通りに動作すること、バグがないことを確認した上でレビュー依頼を出すこと

# イシュー(Issue)の作成手順
## 1.テンプレートを選択する

報告する内容に合わせてテンプレートを選択する。

## 2.タイトルを入力する

タイトルだけで対応の内容が把握できるように記載すること

## 3.イシューの内容を入力する

- テンプレートに従い実装・修正内容を記載する
- 必要に応じてテンプレートの項目は変更して良い。ただし、レビュアーや後で読んだ人が内容がわかるようにすること

## 4.Assigneeを指定する

- **Assignee**に**担当者**を割り当てる
  - 担当者は各セクションのリーダーを指定(例：フロントエンドに関わるイシューの場合、フロントエンドのリーダーを指定する)

## 5.ラベルを指定する

### WIP（Work In Progress）
対応中の場合に指定する。

### 優先度（高）
優先度が高く、急ぎ対応が必要な場合に指定する。

### バグ
バグ・不具合を報告する場合に指定する。

### 提案・要望
追加機能や機能改善の提案や要望を出す場合に指定する。

### 重複
過去に報告されているIssueと重複しているときに使う。重複先のIssueのリンクを記載した上でクローズする。  
※ クローズ時に使用(起票者は使用しない)

### 対応不要
調査・検討の結果、対応が不要なものに使う。対処しない理由(影響範囲が少ない、再現しない、イシューの内容が誤り等)を記載した上でクローズする。  
※ クローズ時に使用(起票者は使用しない)

## 6. イシューを作成する
入力内容に間違いがないことを確認し、「Submit new Issue」をクリックする。
