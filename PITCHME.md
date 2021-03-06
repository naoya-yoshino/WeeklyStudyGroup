### 週次勉強会

2019/05/22

---

### はじめに

---

* この会の趣旨

要件定義/設計を行っていく上で

様々なことを人に説明することになるがこれが意外と難しい

---

そういった説明をする機会というのも中々無く、

ぶっつけ本番のような形で展示会などに出席することになってしまうので

この会を通してそういった能力を向上させようという試みです

---

対お客さんとのやり取りを想定するので、

聞き手側の人は疑問や不明点があれば

都度質問を上げて下さい！

---

### 何をするのか

---

毎週代表の1人が

お題を持ってきて10~20分話す

（10分未満/20分以上は不可だそうです）

---

それぞれが約1ヶ月に1回何かしらのテーマで話してもらう

具体的には、関わっているプロジェクト内容の共有とか、プロジェクトを通して知ったことや個人で勉強したことの発表など

---

先程の趣旨どおり人前に出て喋るのがメインなので、そんなに固い内容でなくてもOKだけど最低限仕事に関することということでお願いします

---

### 今回の議題

---

今回は僕の関わったプロジェクト共有として、

どんなことをやってきたかを何件か説明します


---

### FreeWave

---

* 外国人タレント事務所の基幹業務システム

FileMakerというソフトを利用した既存システムでは、社内サーバーにシステムがあって外部からはシステムにアクセスできない

HPがあり、タレントのデータをシステム/HP両方に持って二重管理している

などの問題があった

---

AWS上にシステムを構築

クラウド上のDBをHP側と共有

などによる問題解決を目的としてシステムの再構築を行いました

---

* 主なシステムの内容

顧客や社員、所属しているタレントなどのマスタ情報管理

案件/請求/支払情報の作成

実績情報の集計や目標管理など

（ややボリュームの少なめな一般的な業務システムという感じ）

---

主に既存システムを踏襲していて、実務的に便利な機能を追加していったような形

（フリーテキストのデータを整備してリスト化して検索可能にしたり、支払の源泉税/消費税や手数料などの煩雑な計算を画面で行うことによる自動化など）

---

加えてマスタ/トランザクションの過去データ、HP側で管理していたデータのシステムへの移行もリリース時に行いました

---

* やったこと

打ち合わせに同席して仕様の聞き取り、設計書の作成

HTMLで作成した画面イメージのモック修正

---

開発時のテスト

など一通りサポートのような形で入っていました

（今現在も保守対応や改修などで継続中です）

---

### JOBNETマイページ改修

---

* 求人サイト利用者向けのマイページ機能改修

マンパワーグループの求人サイト、JOBNETの登録者向けの機能

既存の機能は求人情報のお気に入り登録や派遣登録のための登録会の予約

稼働している人向けに源泉徴収票の送付申請などができる

---

* 改修内容

扶養控除申告、社会保険の扶養者申請などを

システムから簡単な質問や氏名の入力をユーザーが行うことで

帳票に出力できる様にするための機能作成

（帳票出力自体は改修対象外）

---

質問の回答内容/入力内容をセッション（Redis Cache）に保持（一度手続きを行った後の情報もDBからストアード経由で同様にセッションに格納）

---

セッションに保持した情報を利用して、回答内容に応じた画面遷移を行い必要な情報のみをユーザーが入力していくような流れ

（書類を見ながら何を書くべきかなどを考えたり、差し戻しを少なくさせる仕様）

---

* やったこと

改修対象全機能の設計書作成とテスト

お客さんと別会社の人の打ち合わせを元に内容を共有してもらい、

システムに落とし込む部分を担当

---

前述のようなセッションを利用した大まかな流れなどは決定していて、画面単位の細かい仕様などを考えることが多かった

---

### IJ写真帳アプリ

---

* 現場工事の写真帳作成アプリ

給水ポンプや換気ダクト工事などのビル管理会社の基幹システムのIJ-NetをBriswellで開発/保守運用している

---

そのシステムの中で、現場での工事状況などの写真を工事依頼ごとに工程のメモなどと一緒にまとめる写真帳機能があるがWebだと処理が重いためアプリ化することに

windowsアプリとandroidアプリの2つを開発

---

* 主な機能

Web側と同じ様な形で工事依頼の検索を行い、

写真帳作成画面を起動

写真をローカルフォルダから選択してドラッグアンドドロップによる並べ替えなどを行い写真帳を作成する

追加対応としてandroidアプリでは一部オフライン対応行った

---

### 伊坂美術印刷

---

* 印刷会社の基幹業務システム

東京に本社があり、埼玉に工場をもっている印刷会社の業務システム構築

基幹システムがパッケージで使い勝手の悪さなどがあったり

本社と工場間でFAXによる仕事の連絡や仕事の詳細を紙に印刷して手書き修正を行っていたり

といった諸問題をシステム上で管理可能にするためにリプレイスをすることに

---

* やっていること

現在進行中で、打ち合わせに出て詳細設計を行っている最中

主に画面のモック作成を担当していて、簡単なscriptを実装したり

---

### 以上です
ありがとうございました


---

### 来週はだれがやる？

---




