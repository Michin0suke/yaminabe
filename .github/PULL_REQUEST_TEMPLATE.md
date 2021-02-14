<!-- タイトルに、対応した内容をざっくりまとめて書いて下さい。 -->
<!-- この報告書は、分かる範囲ですべての項目を埋めましょう -->

## このプルリクエストを一言で言うと
- 
<!-- 例） ヘッダーのデザインをおしゃれにするものです -->
<!-- 例） issue #123 を解決するものです -->

## このプルリクエストを取り入れるとここが良くなるよ！
-
<!-- このプルリクエストを取り入れる事でプロジェクトに与える良さみを書きましょう -->
<!-- 例）js類を整理したのでファイルがすっきりするよ！ -->
<!-- 例）issue #123 のバグが消えるよ！ -->

## このプルリクエストを送ろうと思った理由/きっかけはこれだよ！
-
<!-- あなたがこのプルリクエストを送ろうと思った理由を簡単に教えて下さい -->
<!-- 例）cssに秩序が無かったのでこのままだと開発し辛いと思った！ -->
<!-- 例）issue #123 のバグに対応したかったからだよ！ -->
<!-- 例）なんとなくだよ！ -->

## このプルリクエストの影響範囲とコードレビュー
<!-- このプルリクエストの中で編集したものにチェックをつけて下さい -->

| ラベル | 重要度 | 必要な対応 |
----|----|---- 
| ★ 　　| 軽微 　| github上での目視コードレビューでOK
| ★★ 　| 中 　　| github上での目視コードレビューでOKだけど、それだとバグを見落とす可能性がちょっとある
| ★★★ | 超重要 | 手元でcheckoutして一通り確認が必要

- view /src/views/**.njk 
  - [ ] 【★】文字の修正
  - [ ] 【★】tailwind / inline styleを使ったデザインの修正
  - [ ] 【★】<style>を使ったデザインの修正
  - [ ] 【★★★】ファイルを削除した

- layout /src/_includes/layouts/**.njk 
  - 全てのviewで呼ばれるのでstyleをグローバルにしていないか確認する
  - [ ] 【★】文字の修正
  - [ ] 【★★】tailwind / inline styleを使ったデザインの修正
  - [ ] 【★★】<style>を使ったデザインの修正
  - [ ] 【★★★】ファイルを削除した

- component /src/_includes/components/**.njk 
  - コンポーネントを呼び出している場所を全てgrepして確認が必要
  - [ ] 【★】文字の修正
  - [ ] 【★★】tailwind / inline styleを使ったデザインの修正
  - [ ] 【★★】<style>を使ったデザインの修正
  - [ ] 【★★★】ファイルを削除した
  
- css
  - [ ] 【★★】グローバルなcssの変更（/src/packs/**.css）
  - [ ] 【★★★】ファイルを削除した

- javascript
  - [ ] 【★】cdnを追加した（/src/app/_includes/layouts/default_layout/_include_cdn.njk）
  - [ ] 【★★】グローバルなjsの変更（/src/packs/**.js）
  - [ ] 【★★★】ファイルを削除した

- 画像
  - [ ] 【★】画像を追加した
  - [ ] 【★★★】ファイルを削除した

- package.json
  - [ ] 【★★】scriptsを変更した
  - [ ] 【★】ライブラリを追加した（cdnが使えるなら出来る限りcdnを優先する）

- core
  - [ ] 【★★★】11tyの読み込み設定を変更した（/.eleventy.js）
  - [ ] 【★★★】webpackの読み込み設定を変更した（/webpack.config.js）
  - [ ] 【★★★】tailwindの読み込み設定を変更した（/tailwind.config.js）
  - [ ] 【★★★】pre commitの設定を変更した（/.lintstagedrc）
  - [ ] 【★】stylelintの設定を変更した（/stylelint.config.js）
  - [ ] 【★】html hintの読み込み設定を変更した（/.htmlhintrc）


- .vscode
  - [ ] 【★】推奨の拡張を追加（/.vscode/extensions.json）
  - [ ] 【★★】エディタにルールを追加（/.vscode/settings.json）

- .github
  - [ ] 【★】issueテンプレを変更した
  - [ ] 【★】pull requestテンプレを変更した

## 特にここを重点的にレビューして欲しい！

<!-- ロジック部分など、ちょっと自信がない部分、問題があった時に影響が大きそうな部分があったらここに記載しましょう！ -->