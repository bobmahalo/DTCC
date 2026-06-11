---
title: "FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]"
source_pdf: "file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/JFSA%20Rules%20Rewrite%20Functional%20Change%20-%20v1.0%20JP%20%28Prod%29.pdf"
pages: 81
size: "2420.0 KB"
category: "Rules"
ingested_on: "2026-06-05"
---

# FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]

**Original File:** [JFSA Rules Rewrite Functional Change - v1.0 JP (Prod).pdf](file:///Users/robertjenkins/Desktop/DTCC%20Learning%20Materials%20Unorganized/PDF%20Files/JFSA%20Rules%20Rewrite%20Functional%20Change%20-%20v1.0%20JP%20%28Prod%29.pdf)  
**Category:** Rules  
**Total Pages:** 81  
**File Size:** 2420.0 KB  

---

## Page 1

 
 
 
 
 
 
 
 
 
 
GLOBAL TRADE REPOSITORY 
FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE 
機能変更文書（参照訳） 
金融庁店頭デリバティブ取引情報報告制度改正対応プロジェクト 
バージョン 1.0  
2024 年 2 月 15 日 
 


---

## Page 2

 
 
© 2023 [[DTCC]]. All rights reserved.  [[DTCC]], [[DTCC]] (Stylized), ADVANCING FINANCIAL MARKETS. TOGETHER, and the 
Interlocker graphic are registered and unregistered trademarks of The Depository Trust & Clearing Corporation. 
The services described herein are provided under the “[[DTCC]]” brand name by certain affiliates of The Depository Trust & 
Clearing Corporation (“[[DTCC]]”).  [[DTCC]] itself does not provide such services.  Each of these affiliates is a separate legal 
entity, subject to the laws and regulations of the particular country or countries in which such entity operates. Please see 
www.[[DTCC]].com for more information on [[DTCC]], its affiliates and the services they offer. 
 
 
文書発行日: 2024 年 2 月 15 日 
サービス: RDS 
表題: 金融庁店頭デリバティブ取引情報報告制度改正対応プロジェクト 機能変更文書 
  

---

## Page 3

 
 
 
改訂履歴 
日付 改定者 バージョン 改定内容 
2/10/2023  FA  0.1  Initial Draft  
2/28/2023   FA  0.2  First External Version  
5/12/2023 FA  0.3  (a) FC 5.2 – TSR への時価情報の統合において、
Delta 項目を追加  
(b) FC 6.3, 6.4 – 制度改正時のデータ移行作業で
除外される取引情報の記載  
(c) FC 1 – MQ 設定についての詳細と接続環境設
定関連文書のラーニングセンターリンク先の更新  
(d) FC 3.1 – スキーマ検証シナリオ例の追記  
(e) FC 3.7 – ERR および RCP の検証ルールの条件
内容の更新  
(f) FC 5 – ブランク（空白）レポート提供不可の記
載  
(g) FC 3.5 & 3.6 –満期または解約済みの取引に
対して提出された取引レベルの担保情報および時価情
報の 180 日間の受付期間の時限撤廃。  
(h) FC 5.1 – 担保のアクティビティレポートとステートレ
ポート名（英語）を [[collateral]] から [[Margin]] に変更  
(i) FC 3.8 – アクションタイプと検証ルールの更新  
(j) FC 4.1 – ACK/NACK 応答電文フォーマットの仕
様更新 
7/14/2023 FA 0.4 (a) FC 6.5 – 本番環境稼働後の既存取引の提出
について 
(b) FC 3.8 – アクションタイプ REVI と MARU の使
用時におけるルール更新 
(c) FC 1 – UAT 環境と本番環境における sFTP プ
ロダクト [[ID]] の違いの明確化 
(d) FC 2.1 – メッセージサンプルへのリンク先更新 
(e) FC 3.5 – 担保情報提出の際、ポートフォリオコー
ド提出の必須化について 
(f) FC 2.3 ,3.13,3.14, 3.15, 5.3, 5.4– 新しい
セクション追加 
(g) FC 6.1 – 本番稼働後の MODI による取引情
報再提出の際の要件の明確化  
(h) FC 5.1 – [[EOD]] Allege Report と Intraday 
Allege Activity Report の追加とイベントタイムスタン
プの概念説明。 

---

## Page 4

 
 
(i) FC3.1 - 受領不可の場合のシナリオ詳細追加 
(j) FC4.1 Batch Download Report のファイル名
の詳細追記 
9/15/2023 FA 0.5 (a) FC 5.4 – JFSA Trade State Report CSV レ
ポートファイル名の誤植の訂正および各種レポートに
JFSA 向けを明示およびファイル名の命名規則の更新 
(b) FC 3.8 –項番５の明確化のための図式更新
（実際のワークフローに変更はなし） 
(c) FC 3.1 – ファイルレベルでの受領不可シナリオ(d)
を追加 
(d) FC 7 – 請求金額に関する記載追加 
(e) FC4.1 -応答ファイルに zip ファイル形式を追記 
(f) FC 2.3 – メッセージヘッダー内の from タグにおけ
る値と各取引レコードの SubmitgAgt タグの妥当性
検証についての追記  
(g) FC 3.3 – Unique transaction identifier 
(UTI) 項目に Proprietary [[ID]] タグを導入することに
ついての説明を追記 
(h) FC 6 – 取引識別子として Proprietary [[ID]] タグ
を導入するにあたり、全セクションの内容更新 
(i) FC 4.3 – MQ の Reply to キューで
ACK/NACK 応答を返信する場所を指定できる機能
の紹介 
(j) FC4.3- MQ Reply の ACK/NACK 応答のキュ
ー指定機能 
(k)FC3.14 Other Payment Fields 項目の独自
性の鍵についての説明と使用事例の更新 
11/17/2023 FA 0.6 (a) [[DTCC]] ラーニングセンターに掲載されている FC5.3
レポート管理機能のリンク先追加 
(b) FC6.2 取引情報のデータ初期化におけるアクショ
ンタイプとイベントタイプの検証ルールの明確化 
(c) FC4.1 sFTP ファイル名の BizMsgIdr の前に入っ
ていた余計なスペースを削除。ファイル名の冒頭 SFTP
から小文字の sFTP に更新。 
(d) FC 3.16 新たに追加したセクション 
(e) FC3.14 Other Payment 項目の独自性判断
のキー項目を Other Payment Currency から
Other Payment Date に更新。それに伴う使用事
例の更新。 
(f) FC5.4 レポートのファイル名の明確化と ERR によ
る Trade Submission Report および [[Margin]] 
Submission Report へのアクセス権限の追記。 
(g) FC2.3 BizMsgIdr タグの検証ルールの導入。 
(h) FC3.13 集約型 O-code 導入時期の更新。 

---

## Page 5

 
 
01/31/2024 FA 0.7 (a) FC4.1 応答ファイル BDR の現状のファイル名と将
来変更後のファイル名の記載 
(b) FC6.2 本番環境データを使用したドライラン作業
の内容について更新 
(c) FC3.1 データ書式の記載の違いについての解説
追記 
02/15/2024 FA 1.0  (a) FC3.8 イベントタイプの表を追加で記載。導入に
あたっての詳細に変更なし。 
 (b) FC6.7 UAT リリース５の日程更新 
 (c) FC7.2 請求書内訳レポート書式の更新 
 (d) FC6.2 データ初期化作業の予行演習ドライランの
実施日を 2 月 6 日から 2 月 9 日に変更 
(e) FC3.10/11 取引報告当事者に関する部分の変
更に伴う使用事例の更新 

---

## Page 6

 
 
目次 
改訂履歴 .............................................................................................................................................................. 3 
1. 概要 .................................................................................................................................................................... 8 
背景 ..................................................................................................................................................................... 8 
仕様変更範囲 ...................................................................................................................................................... 8 
本プロジェクト対象外 .............................................................................................................................................. 9 
参考文書 ............................................................................................................................................................10 
用語の定義 .........................................................................................................................................................10 
2. 仕様変更 ........................................................................................................................................................... 12 
FC 1: 接続環境: メッセージ・チャネル、ルーティング、及びデータ提出の方法 ..............................................................12 
FC 2: データ取り込み メッセージタイプと提出フォーマット ..........................................................................................14 
FC 2.1: データ取り込みメッセージタイプと提出フォーマット .......................................................................................14 
FC 2.2: 特殊文字 ............................................................................................................................................14 
FC 2.3: メッセージヘッダー書式 ...........................................................................................................................15 
FC 3: データ取り込み - 提出されたデータの処理 ....................................................................................................17 
FC.3.1: データ取り込みに関する検証 ..................................................................................................................17 
FC 3.2: メッセージの処理と順序付け ..................................................................................................................19 
FC 3.3: 取引識別子 ........................................................................................................................................20 
FC 3.4: 取引の独自性 .....................................................................................................................................20 
FC 3.5: 担保情報の提出 ..................................................................................................................................21 
FC 3.6: 時価情報の提出 ..................................................................................................................................23 
FC 3.7: 取引当事者（Reporting Counterparty）と 報告義務者 （Entity Responsible for Reporting） 23 
FC 3.8: アクションタイプとイベントタイプの検証.......................................................................................................25 
FC 3.9: 検証を緩和する取引情報の種類 ...........................................................................................................33 
FC 3.10: 取引相手の変更 ...............................................................................................................................34 
FC 3.11: 取引報告当事者 TP1 の変更 ............................................................................................................35 
FC 3.12: JFSA 報告用 XML ユーセージガイドライン ............................................................................................35 
FC 3.13: 新たな集約型 O-Code の導入 ..........................................................................................................36 
FC 3.14: Other Payment 項目 .....................................................................................................................37 

---

## Page 7

 
 
FC 3.15: スケジュール項目 ................................................................................................................................47 
FC 3.16: イベントタイムスタンプとレポーティングタイムスタンプ ..................................................................................52 
FC 4: 応答メッセージ ...........................................................................................................................................58 
FC 4.1 応答メッセージ様式 ................................................................................................................................58 
FC 4.2 応答メッセージの書式および チャネル ........................................................................................................63 
FC 4.3 MQ 応答は Replyto キューに返信 ..........................................................................................................64 
FC 5: レポート ....................................................................................................................................................64 
FC 5.1: レポートの種類 .....................................................................................................................................64 
FC 5.2: 時価情報をトレード・ステート・レポート（TSR）へ反映 ............................................................................70 
FC 5.3: セルフサービスレポート管理機能...............................................................................................................71 
FC 5.4: レポートのファイル名フォーマット .................................................................................................................71 
FC 6: 制度改正実施にむけての特別な作業について ..............................................................................................73 
FC 6.1: 制度改正実施に向けての [[DTCC]] によるアクションタイプの初期化作業 ........................................................74 
FC 6.2: データ統合の予行演習計画 ..................................................................................................................75 
FC 6.3: 取引の独自性ロジックの変更に伴う重複ポジションの削除 .........................................................................77 
FC 6.４: 内部取引（Self Trades）の除外 .....................................................................................................77 
FC 6.5: 制度改正実施後の取引情報の更新 .....................................................................................................78 
FC 6.6: 移行期間の報告 ..................................................................................................................................78 
FC 6.7: 制度改正導入までのスケジュール ...........................................................................................................78 
FC 7: 請求額について .........................................................................................................................................79 
FC 7.1:  請求ロジック階層 ................................................................................................................................79 
FC 7.2:  請求金額内訳レポート ........................................................................................................................79 
 

---

## Page 8

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 8  
 
1. 概要 
背景 
本プロジェクトでは、金融庁が実施する制度改正（施行日は 2024 年 4 月 1 日）に対して、GTR が適切に、確実に対応
するために仕様等を変更することを目的とする。制度改正に伴う変更は、5 つの報告対象アセットクラス（クレジット、金利、株
式、コモディティ、FX）全てに適用され、時価情報報告と担保情報報告が新たに導入される。なお、暗号資産に関連する取
引だけがコモディティのアセットクラスに分類され報告の対象となる可能性がある。その他の伝統的なコモディティ取引については、
引き続き金融庁への報告対象外である。本制度改正実施日に報告が必要となる項目は、CDE98 項目、ESMA20 項目、
CFTC19 項目からなる計 137 項目である。デルタと UPI については、2024 年 4 月 1 日の新制度施行時には任意項目と
され、報告が必須となる時期は未定であり、金融庁の公表を待っている状況である。そのため本制度改正により、最終的に報
告が必須となる項目は合計 139 項目である。報告主体となる利用者には 2024 年 4 月 1 日から ISO XML 20022 準拠
の形式により、取引情報蓄積機関に取引情報を提出する義務が課せられている。現存する既存取引の情報更新の移行期
限は制度改正実施日から 180 日後の 2024 年 9 月 27 日に設定されている。制度改正実施日当日に、現存する既存取
引（オープンポジション）を再提出するために必要な最低限の項目が定められており、その後、第 2 段階として、新たな報告要
件に従って、残りのデータ項目を補完し、すべての現存する既存取引の情報更新を完了する必要がある。金融庁への直接報
告から、DDRJ へ報告先を移行する金融機関等にも同様の対応が必要となる。取引情報更新作業を効率的に行うために
も、2024 年 4 月 1 日時点で、新報告要件を完全に満たす形で現存する既存取引を一気に再提出することを推奨する。既
に DDRJ と契約のある利用者も新報告要件を満たす形で既存取引分の取引情報の再提出が必要である。なお、誤解を避
けるため 2024 年 4 月 1 日以降に新規取引として報告する取引情報については、新報告要件で求められる全ての必須項
目を入力し、提出する必要があることを明記する。 
仕様変更範囲 
本プロジェクトの対象範囲は、以下の変更部分となる。 
項目 説明 
制度改正実施日 
二段階アプローチ 
第一段階：2024 年 4 月 1 日 - 既存取引については最小限の必須項目提出。(JFSA メッセージ・
スペシフィケーション参照) 新規取引については新報告要件における全項目の提出が必要。提出ファイ
ル形式は ISO XML のみ。この日以降は全ての取引情報の検証ルールは、新規・既存取引分を問わ
ず、同一のものになる。 
第二段階：2024 年 9 月 27 日 - 残りのデータ項目を更新して再提出する締め切り日。 
UPI 
2024 年 4 月 1 日の時点では UPI 項目の報告は任意とする。2023 年 9 月 1 日付けパブコメに
て、報告が必須となる正式な導入時期を 2025 年 4 月 7 日と提言。 

---

## Page 9

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 9  
 
LEI 
LEI による報告は、取引当事者（RCP）及び報告義務者（ERR）に義務付けられる予定である。こ
れは GLEIF データベースを用いて有効値かどうか検証する。また該当する場合、報告が必要な清算機
関（CCP）の項目にも LEI の記載が必須であり、同様な検証を行う。詳細はメッセージ・スペシフィケー
ションに記載。 
UTI 
取引情報には UTI が義務付けられる。取引リンク・ロジックは、多くの場合が UTI+RCP＋OCP に基づ
くが、アクションタイプによっては UTI +取引当事者 1 のみに基づく。USI と Transaction [[ID]] 項目は
廃止され、取引リンク・ロジックから削除する。 
ISO XML 
TR への取引情報提出は、ISO XML フォオーマットのみに限定される。 
ISO XML スキーマは、同一ファイルによる複数法域への報告をサポートしない。 
[[DTCC]] XML は使用不可。 
JFSA 報告用 XML ユーセージガイドラインを発行する予定。 
FPML 
FpML は ISO XML の適用により廃止される。金融庁向け報告 FpML のサポートを終了。 
FpML を引き続き受領する法域との間で行われる取引報告については、別途取引情報の提出が必
要。 
CSV 
CSV の提出は、ISO XML の義務化に伴い廃止される。金融庁向け報告 CSV のサポート終了。 
Harmonized と [[OTC]] Legacy の両方のテンプレートも使用不可。 
CSV を引き続き受領する法域との間で行われる取引報告については、別途取引情報の提出が必要。 
取引リンクロジック 
取引リンクロジックは、多くの場合が UTI+RCP＋OCP に基づくが、アクションタイプによっては UTI +取
引当事者 1 のみに基づく。 
データ統合 現行の GTR から移行されるデータはない。データの初期化の詳細についてはセクション 6 に記述。 
メッセージ・スペシフィケーシ
ョン 
既存の項目についても新報告要件下では、データの取り込む方法に変更がある。 
メッセージ・スペシフィケーションは新報告要件を網羅する内容である。 
メッセージタイプ 
アクションタイプのルールに従い、Trade State, Valuations and [[collateral]] Valuation 
message がサポート対象。 
レポートの種類 
DDRJ から金融庁への報告は XML 形式。GTR から利用者に対しては、CSV 形式により各種レポート
を提供する予定。現在のところ、利用者へは原則一律に各種レポートを CSV 様式で提供予定。XML
様式がどうしても必要な場合への対応は、別途検討中。 
Action Type / Event 
Type の組み合わせルール 
Action Type/Event Type ルールが新たに適用される。 
本プロジェクト対象外 
本プロジェクトでは下記は対象外: 
• UPI (商品分類識別子)報告の完全導入。UPI 及び Delta 項目の導入実施時期は 2025 年 4 月 7 日予定。 
• 料金体系の見直しは制度改正実施後行う予定。 

---

## Page 10

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 10  
 
参考文書  
以下の文書も参照のこと。 
1. JFSA メッセージ・スペシフィケーションなど、本プロジェクトに関連する文書は、GTR ラーニングセンターにある JFSA Re-
Write コーナーの Upcoming Changes セクションにて公開予定。 
2. JFSA 報告用 XML ユーセージガイドライン (ISO20022) およびその他の公表された文書 
用語の定義 
略語・用語 定義・説明 
ACK GTR によりデータを受領した旨を示す応答メッセージ 
Channel メッセージを転送するために 2 つのエンド・ポイントやのキュー・マネージャー間を単方向でつなぐ通信回路 
CSV カンマ区切り（Comma Separated Values）GTR へのデータ提出タイプの一種 
[[DTCC]] ディー・ティー・シー・シー（The Depository Trust and Clearing Corporation） 
FpML XML ベースの金融商品用マークアップ言語（Financial Product Markup Language）、GTR への
データ提出タイプの一種 
GTR グローバル・トレード・レポジトリー（Global Trade Repository） 
JFSA 金融庁（Financial Services Agency of Japan) 
LEI 取引主体識別子（Legal Entity Identifier） 
MQ メッセージキュー（Message Queue） – アプリケーション間でメッセージの受け渡しをする際にメッセージ
をいったん預かるミドルウェア 
Message 
Specification 
GTR へ取引情報を提出する際の、各データ項目における有効値等を示すメッセージ仕様書、 [[DTCC]] ラ
ーニングセンターで閲覧可能 
NACK GTR によりデータが受領できなかった旨を示す応答メッセージ 
O-Code 口座毎のデータの切り分け及びアクセス権限を管理するためのコード 
OCP 取引相手（主に Trade Party2 と記載される） 
RCP 取引当事者 
SDO 顧客属性を管理する口座管理システム 
SDR 米国 [[CFTC]] により認可を受けた取引情報蓄積機関（Swap Data Repository） 
sFTP セキュア・ファイル転送プロトコル（Secure File Transfer Protocol） 

---

## Page 11

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 11  
 
略語・用語 定義・説明 
Trade State GTR で受領し適切に処理された最新の状態を示す取引情報 
TSR Trade State Report.  デリバティブ取引のオープンポジション（現存取引）を示すレポート (直近に提
出された時価情報も一緒に掲載)。 日次に作成。 
UAT GTR システム・テスト環境(“User Acceptance Testing”) 
UPI 商品分類識別子(Unique Product Identifier) 
USI 取引番号識別子（Unique Swap Identifier） 
UTI 取引番号識別子（Unique Trade Identifier） 
XML 本文書では ISO 20022 準拠の XML フォーマットを示す 

---

## Page 12

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 12  
 
2. 仕様変更 
FC 1: 接続環境: メッセージ・チャネル、ルーティング、及びデータ提
出の方法 
GTR への接続手段及びデータ提出フォーマットに変更なし。GTR は引き続き、ウェブポータル、MQ、sFTP という現行の接続
手段とプロトコールにより、データの送受信を運用。 
ISO XML メッセージは、Service Destination/ Reporting Obligation 項目を許容せずサポートしていないため、ルーティ
ングは以下の 3 つのポイントで決定され、各法域は個別のインバウンドプロダクト [[ID]]／キューを持つことになる。 
(i) ポータル/GUI で提供される Web アップロード機能は、ユーザが画面上で選択した法域への直接アップロードにのみ対応す
る。 
(ii) JFSA 報告専用 sFTP プロダクト [[ID]] により、GTR が取引情報を送信する法域を決定することになる。これらのプロダクト 
[[ID]] は、今回の JFSA の制度改正のために新たに設定されるため、sFTP を利用する金融機関は [[DTCC]] コネクティビティチーム
へ設定についての問い合わせを行う必要がある。 
(iii) JFSA 報告専用 MQ プロダクト [[ID]] によって、GTR が取引情報を送信する法域を決定する。キューの詳細は下記の表に
記載。 
RDS MQ Input Queues 
[[Asset]] 
Class/Product 
RDS 
Sub-
Services 
Queue 
Manager [[DTCC]] Input Queue Name Description 
Commodity JFSA MU1R, 
MP1R GTR.JFSA_COMMODITY.A01 [[DTCC]] input queue 
for JFSA (Re-Write) 
Credits JFSA MU1R, 
MP1R GTR.JFSA_CREDITS.A01 [[DTCC]] input queue 
for JFSA (Re-Write) 
[[Equity]] JFSA 
MU1R, 
MU2R, 
MP2R 
GTR.JFSA_EQUITY.A01 [[DTCC]] input queue 
for JFSA (Re-Write) 
FX JFSA 
MU1R, 
MP5R-
MP9R 
GTR.JFSA_FX.A01 [[DTCC]] input queue 
for JFSA (Re-Write) 
Rates JFSA MU1R, 
MP1R GTR.JFSA_RATES.A01 [[DTCC]] input queue 
for JFSA (Re-Write) 
[[Margin]] Activity 
Submission JFSA MU1R, 
MP1R GTR.JFSA_MARGIN.A01 [[DTCC]] input queue 
for JFSA (Re-Write) 
 
現在の機能についての詳しい説明は、ラーニングセンターの Connectivity セクションを参照のこと。ラーニングセンターの 
Connectivity に関する文書はこちら を参照のこと。制度改正の概要に関する要件は、コネクティビティの要件詳細について
は、ラーニングセンターの JFSA Rewrite and EMIR Refit sFTP Connectivity Starter Pack に記載されている。 
  

---

## Page 13

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 13  
 
 
金融庁報告制度改正に対応する接続環境やオンボーディングの詳細、各種レポートのプロダクト [[ID]] に関する詳細はラーニング
センターに掲載されている。sFTP 接続の際に使用するプロダクト [[ID]] は下記の表を参照のこと。青字は本番環境、UAT 環境
のプロダクト [[ID]] は 298 で始まる。（本番環境用の 250 の部分を 298 に入れ替える） 
Schema Description Format Collate
ral 
Commo
dity 
Cre
dit 
Equi
ty 
Rat
es 
F
X 
auth.030.001.03_JFSAUG_DAT
TAR_1.0.0  
JFSA Trade Activity Submission 
XML 
ISO20022X
ML   60978 
auth.108.001.01_JFSAUG_DAT
MDA_1.0.0  
JFSA [[Margin]] Activity Submission 
XML 
ISO20022X
ML 60979   
auth.031.001.01_JFSAUG_FDR
ES_1.0.0 
JFSA GTR Batch ACK/NACK 
Report XML 
ISO20022X
ML 2503233 
auth.030.001.03_JFSAUG_DAT
TAR_1.0.0  JFSA Trade Activity Report XML ISO20022X
ML   2503234 
auth.107.001.01_JFSAUG_DAT
TSR_1.0.0 JFSA Trade State Report XML ISO20022X
ML   2503235 
auth.108.001.01_JFSAUG_DAT
MDA_1.0.0 JFSA [[Margin]] Activity Report XML ISO20022X
ML 
25032
36   
auth.109.001.01_JFSAUG_DAT
MDS_1.0.0  JFSA [[Margin]] State Report XML ISO20022X
ML 
25032
37   
auth.030.001.03_JFSAUG_DAT
TAR_1.0.0  JFSA Trade Activity Report CSV CSV 
equivalent   2503238 
auth.107.001.01_JFSAUG_DAT
TSR_1.0.0 JFSA Trade State Report CSV CSV 
equivalent   2503239 
auth.108.001.01_JFSAUG_DAT
MDA_1.0.0 JFSA [[Margin]] Activity Report CSV CSV 
equivalent 
25032
40   
auth.109.001.01_JFSAUG_DAT
MDS_1.0.0  JFSA [[Margin]] State Report CSV CSV 
equivalent 
25032
41   
N/A JFSA [[collateral]] Submission 
Report CSV CSV only 25032
42   
N/A JFSA Daily Submission Report 
CSV CSV only   2503243 
N/A  JFSA [[EOD]] Allege Report CSV  CSV only  2503248  
N/A  JFSA Intraday Allege Report 
CSV  CSV only  2503249  
auth.030.001.03_JFSAUG_DAT
TAR_1.0.0  
JFSA Regulator Trade Activity 
Report XML 
ISO20022X
ML   2503244 
auth.107.001.01_JFSAUG_DAT
TSR_1.0.0 
JFSA Regulator Trade State 
Report XML 
ISO20022X
ML   2503245 
auth.108.001.01_JFSAUG_DAT
MDA_1.0.0 
JFSA Regulator [[Margin]] Activity 
Report XML 
ISO20022X
ML 
25032
46   
auth.109.001.01_JFSAUG_DAT
MDS_1.0.0  
JFSA Regulator [[Margin]] State 
Report XML 
ISO20022X
ML 
25032
47   
 

---

## Page 14

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 14  
 
FC 2: データ取り込み メッセージタイプと提出フォーマット 
FC 2.1: データ取り込みメッセージタイプと提出フォーマット 
メッセージタイプとそれに仕様する XML メッセージの種類は下記の表の通り。 アセットクラスごとのレガシーCSV メッセージファイル
は、制度改正後は許容されずサポートされないことに注意。 
メッセージタイプ 使用する XML メッセージの種類 
Transaction 
(Trade State)  
XML - auth.030.001.03_JFSAUG_DATTAR_1.0.0  
Valuation  XML - auth.030.001.03_JFSAUG_DATTAR_1.0.0  
[[collateral]]/[[Margin]]  XML - auth.108.001.01_JFSAUG_DATMDA_1.0.0  
 
現行のレガシーCSV テンプレートや FpML ファイルは受領不可となる。 
[[DTCC]] メッセージ・スペシフィケーションは各項目の詳細な説明や検証ルールおよび XML の x-path 情報が記載される。 
JFSA 報告用 XML ユーセージガイドラインは各項目の XML スキーマや桁数などユーザーがデータ提出の際に必要な要件が記
載される。 
[[DTCC]] は、ポータルからの Web アップロード、MQ および sFTP による取引情報提出をサポートする。Web アップロードや
sFTP による提出では、１つの XML ファイル内に複数の取引の内容を含めることができる。MQ による提出では、メッセージごと
に 1 つの取引の内容を作成することが必要である。メッセージのサンプルフォーマットはこちらに掲載済み。 
FC 2.2: 特殊文字 
GTR へのデータ送信の際は、UTF-8 の文字設定にすること。 
一般に、ISO XML スキーマではすべての文字が英数字であることを想定しています。メッセージ仕様に明示的に記載されてい
ない限り、各項目への入力は原則英数字だけが許容される。GTR は、この原則に基づいて各項目の要件と許容値等が説明
されているメッセージ・スペシフィケーションおよび JFSA 報告用 XML ユーセージガイドラインに従って検証を実施する。 
  

---

## Page 15

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 15  
 
FC 2.3: メッセージヘッダー書式 
ファイル送信の際は、所定のヘッダー形式に従う必要があり、そうでない場合は、ファイル全体またはメッセージが受領不可とな
る。ラーニング センターで公開されているサンプルには、必要となるタグが表示されている。下記の表にヘッダー部分の要素
（Element）、使い方の定義と Xpath およびサンプルとなる値を列記しているので参照のこと。報告権限のない法人に対す
る取引情報報告を防ぐために、下記の検証ルールを設定することとする。  
(a) sFTP 送信の場合、sFTP ファイル名と AppHdr アプリケーションヘッダー内の o-code を検証し、差異がある場
合は、受領不可とする。 
(b) ウェブポータル経由で取引情報ファイルをアップロードする際、ポータルのドロップダウンメニューで選択されている o-
code と AppHdr タグ内の o-code が異なる場合は、GTR はこれを受領不可とする。 
(c) MQ を含む全ての送信モードにおいて、Submitting Agent のタグと AppHdr 内の o-code を検証し、報告
権限があるか否かを確認する。 
その他の検証ルール 
(a) CreationDate の日付は、GTR がファイルを受領する日の翌日以降にはなってはならない。（同日もしくはそれ
以前であることが必要） 
(b) CreationDate の日付は、翌日以降の値（未来日付け）の場合、受領不可となる。 
 
エレメント名 e   使い方定義  Xpath   
データタイ
プ   
条件  スキーマバージョン   サンプルの値   
Hdr  
アプリケーションヘッダ
ーの内容を含める  
//element(*,Business
DataHeaderV01)/Hdr  
strict   必須  
head.003.001.01.
xsd  
“Hdr” の画像参照  
Pyld  
メッセージのボディ部
分を含める。 Pyld 
は、<Document> 
タグを内包し、取引
情報が auth.030 
または、auth.108
ベースかを特定する  
//element(*,Business
DataHeaderV01)/Pyld
  
N/A  必須  
head.003.001.01.
xsd  
“Pyld”の画像参照  
From   
BusinessApplicati
on A（送信者）の
[[ID]]. 報告者の O-
code を入力する。  
AppHdr/Fr/OrgId/[[ID]]/
OrgId/Othr/[[ID]]  
Max35T
ext  
必須  head.001.001.02  6ABC  
To  
BusinessApplicati
on B（受領者）の
[[ID]]。本邦報告法域
の取引情報蓄積機
AppHdr/To/OrgId/[[ID]]/
OrgId/Othr/[[ID]]  
Max35T
ext  
必須  head.001.001.02  DDRJ  

---

## Page 16

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 16  
 
関である DDRJ を入
力する。  
BusinessMessag
eIdentifier  
Business 
Message. A （送
信者）特有の [[ID]] を
入力。提出ファイルを
特定するための値を
入力する。 
AppHdr/BizMsgIdr  
Max35T
ext  
必須  head.001.001.02  ABC123456789  
MessageDefinitio
nIdentifier  
適用するメッセージの
定義    
AppHdr/MsgDefIdr  
Max35T
ext 英数
字文字列
(0-9a-
zA-Z),ア
ンダースコ
ア(_),ハイ
フン(-),ドッ
ト(.) 
必須   head.001.001.02  
auth.030.001.03_J
FSA_DATTAR_1.0.
0  
CreationDate  
Date and Time of 
the creation of 
the 
BusinessApplicati
onHeader（ヘッダ
ー）および
Business 
Message（取引情
報、時価、担保情
報）
(Payload/Trade/
[[Margin]] Data)の作
成日時を入力。  
AppHdr/CreDt  
ISODate
Time  
必須  head.001.001.02  
2001-12-
17T09:30:47Z  
  
“Hdr”  
  

---

## Page 17

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 17  
 
  
  
“Pyld”  
  
 
 
メッセージヘッダー内の”From”タグに付記されている o-code が、提出される取引レコードの“SubmitgAgt”タグに対して適切
かどうかの検証を行う。この検証により、提出されたデータファイルが有効なもので、且つ許可されていないある取引当事者のため
に誤って第三者として報告してしまうことを防止することができる。つまり、メッセージヘッダーの情報提出者の詳細と合致している
かの検証を行う。  
FC 3: データ取り込み - 提出されたデータの処理 
FC.3.1: データ取り込みに関する検証 


---

## Page 18

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 18  
 
金融庁への報告対象取引の定義には制度改正後も変更がないため、GTR が利用者から提出された取引情報を取り込む際
に適用する基本的な検証作業は、現行通り下記の手順で行う。 
• メッセージファイルが正しい書式となっておりデータ処理が適切にできるかどうかを検証するファイルレベルのスキーマ検証
（Schema Validation）によって、GTR が受領可能なフォーマットか否かの判断をする。更に、提出されたファイル
をメッセージファイルレベルで検証し、1 ファイル内に複数の取引レコードがある場合は各取引の詳細を検証する。
CRPT というファイルレベルでの受領不可の例としては、ファイルのヘッダー部分に誤りがあるか情報が不足している 場合
である。ファイルレベルでの検証で受領不可となった場合は、取引レベルの検証までは行わない。受領不可となるシナリ
オを下記に掲載する。 
(a) BizData ヘッダーが含まれていない若しくは形式が正しくない。受領不可となるヘッダー部分の要件は FC2.3 を
参照のこと。 
(b) MQ ファイルに複数の取引情報が含まれている。(/Rpt Blocks) 
(c) sFTP 送信によるファイルに 10 万件より多い取引情報が含まれている(/Rpt Blocks)  
エラーコードはメッセージファイルレベルで出力される。 
メッセージレベルのステータス 
  
コード名 名称 定義 
ACPT Accepted メッセージファイルが受領された 
CRPT CorruptedFile 
メッセージファイルが破損していた（したがって受領されていな
い） 
 
取引レコードレベル（取引レベル）で受領不可となるその他の例として、オプショナル項目に対して、XML タグ内の値
を空白（ブランク）で送信してきた場合は、スキーマ検証ではじかれ受領不可となる。検証ルールを通過するために
は、当該項目に適切な値を入れて送信するか、XML タグ自体を全部削除して報告する必要がある。これらは各取引
レコードレベルで検証される。 
詳細レベルのステータス 
  
コード名 名称 定義 
ACPT Accepted 取引記録が受領された 
RJCT Rejected 取引記録は受領不可 
 
• データ送信者権限検証（Permission Validation）によって、取引情報が適切な権限を有する提出者からの送
信か否かを検証する 
• コア・プロセッシング （Core Validations） によって、メッセージ・スペシフィケーションと Usage Guideline に定義さ
れている主要な項目（取引のエコノミクスを表す項目等）の書式の適正性を検証し、GTR で受領できるか否かを検
証する。例えばデータタイプ Num (31,13)は小数点の前に 18 桁の数字、小数点の後に 13 桁の数字を許容する

---

## Page 19

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 19  
 
が、トータルでは 18 桁までにする必要があるという意味である。これは、CDE および ISO XML における(18,13)と同
じことを意味している。仮に提出された値が、'11111111111111.1100000000000’の場合、トータル 27 桁に
なるので、受領不可となる。もし、最後のゼロの値を削除して、'11111111111111.11'を提出した場合は受領さ
れる。 
• メッセージ・スペシフィケーションと Usage Guideline に定義されている GTR 法域毎検証（Jurisdictional 
Regulatory Validation）によって、上記コア・プロセッシングに加えて、金融庁報告用特有の検証を行う。 
 
一般的な検証プロセスは、以下のとおりである。 
Authorization 
(Permission)
Jurisdictional 
Validation
Schema 
Validation
Control 
Processing 
(Core Validation)
Store
NACK
ACK
1
2
3
4
5
 
現行の検証プロセスの詳細は [[DTCC]] ラーニングセンターに掲載されている。 
各項目やメッセージタイプごとの検証ルールの詳細については、メッセージ・スペシフィケーションを参照のこと。  
FC 3.2: メッセージの処理と順序付け 
メッセージの処理と順序付けの方法については現行の仕様から変更はない。すなわち、 同一のチャネル(MQ、SFTP や Web 
アップロード)を利用して提出された取引情報については、提出された順序によりデータ処理される。しかし、ユーザーが異なるチャ
ネルやファイルを利用して、同一の取引に関して複数回連続して送信してきた場合、データ処理の順序についてのロジックは機
能しないこととなる。複数のチャネルを利用して、ほぼ同一時刻に GTR に送信するような事は避け、GTR から受領確認の返信
電文を確認してから次のデータを送信することを推奨する。 
アクションタイプによる順序付けルール（FC3.8 項参照）の実装に伴い、アクションタイプに基づいて、いつ、何をメッセージとして
送信するかを検討・考慮することが特に重要である。 
システム負荷を分散する機能により、MQ 経由の応答メッセージは、送信されたものとは異なる順序で返されることがあることに
注意が必要。しかし、これはメッセージが順番通りに処理されなかったことを意味するものではない。 

---

## Page 20

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 20  
 
FC 3.3: 取引識別子 
取引識別子（UTI）は、制度改正施行日以降に金融庁へ報告するすべての新規取引（アクションタイプ「NEWT」を使
用）に対しての必須項目。グローバル UTI フォーマットの要件（[A-Z0-9]{18}[0-9]{2}[A-Z0-9]{0,32}）は、仮
UTI が付与された新規取引や、UTI 付与者となる取引当事者によって作成された UTI を共有して使う新規取引にも適用さ
れる。しかし、既存取引分に限っては、Proprietary [[ID]] タグの使用によって、制度改正後の取引識別子の提出が可能とな
る。 
Proprietary [[ID]] タグの利用に関する検証ルールはメッセージ・スペシフィケーションに定義されている。 
既存利用者に対して [[DTCC]] が行う現行環境から新制度用環境へのポジションの移行（Data Initialization）では、制度
改正実施日以前に提出された現存する取引分の USI Value 項目の値を、Proprietary [[ID]] タグに移行する。（USI 
Prefix 項目の値は移行されない）この対象となる利用者は、既存取引の情報を報告制度改正後に Upgrade する際に、
UnqTxId を使って報告するのか、引き続き Prtry/[[ID]] tag を使って報告を行うのか選ぶことができる。ただし、各タグに求められ
ているフォーマットの要件を満たしているかどうかの確認が必要である。 
FC 3.4: 取引の独自性 
現行の仕様では、取引の独自性は下記のとおり判定されている。 
• 金融庁報告においては、取引識別子 USI (USI [[ID]] prefix + USI [[ID]] value) + 取引当事者 1（[[ID]] Type＋
[[ID]]）+ 取引当事者 2 ([[ID]] Type + [[ID]]) の組み合わせで取引の独自性を判断している。以下、
「USI+TP1+TP2」と言う。 
制度改正に伴い、GTR における取引の独自性判定は下記のとおりに変更する。 
• 金融庁報告においては、UTI（または Proprietary [[ID]]）＋取引当事者 1 の組み合わせによって取引の独自性を
判断する。以下、「UTI + RCP」と言う。 
この取引の独自性判定の変更により、同一の USI+TP1 の組み合わせに複数の異なる取引当事者 2（「TP2」）が存在
す、いわゆる「重複」取引（現行の独自性判定では、TP2 も判定要素としているため許容されている）を削除する必要があ
る。現行のポジションレポートを確認し、このような重複取引がある場合は、制度改正実施前に当該取引情報を削除（ EXIT
の提出）する必要がある。なお、該当する重複取引がある利用者には DDRJ のオペレーションチームより個別に連絡を取って
いる。この重複取引の削除作業を利用者が行わない場合は、GTR は直近で更新された取引情報のみを選択し、それ以外の
同一の USI+TP1 を持つ他の重複取引を削除するので注意すること。 

---

## Page 21

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 21  
 
この取引の独自性判定変更によって、取引相手の変更を提出する場合、現行の方法から変更する必要が出てくることとなり
る。詳細については、FC3.10 を参照のこと。 
FC 3.5: 担保情報の提出 
制度改正により、担保情報の提出も報告必須要件として加えられた。 
提出要件 
• 担保情報の送信には auth.108.001.01_JFSAUG_DATMDA_1.0.0 xml スキーマを利用し要件を満たす必
要ががある。スキーマ要件を満たさない場合、このメッセージは受領不可となる。例えば、アクションタイプ MARU を送
信し、Fixed Rate や Expiration Date などの取引のエコノミクスを示す項目を含めた場合、メッセージは受領不可
となる。 
• 担保情報は XML フォーマットで、O-code "0xxx "を指定して提出する必要がある。（検証ルールの詳細はメッセー
ジ・スペシフィケーションに記載）。メッセージのサンプルはラーニングセンターに掲載されている。 
• これらのメッセージは、Web アップロード、SFTP、MQ 経由で送信することができる。 
• 担保情報は、送信時のアクションタイプ Action Type の値が "MARU "であることで認識される。 
• データ送信者権限検証は、他のすべてのメッセージタイプと同様に機能する。 
• 検証ルールは、メッセージ・スペシフィケーションに記載されている。 
取引レベルまたはポートフォリオレベルの担保情報 
• 担保情報を送信する際は、担保情報が取引レベルなのかもしくはポートフォリオレベルなのかを選択する。  
• 取引レベルの担保情報の場合 
o 取引レベルの担保メッセージには UTI が必須であり、提出する担保情報が対象とする取引（UTI + RCP 
+ OCP が一致しなければならない）がある場合にのみ受理される。 その対象取引のステータスは
「Open」、「Terminated」、または「Expired」である必要がある。 
o 「誤提出」 (アクションタイプ EROR) または「転出」 (アクションタイプ PRTO) として報告された取引に対して
の取引レベルの担保情報は受領不可となる (NACK となる)。 
o  UTI を入力できるように、担保ポートフォリオ インジケータは「false」であること。 
o 当初証拠金担保ポートフォリオ コードまたは変動証拠金担保ポートフォリオ コードのいずれかを、2024 年 4 
月 1 日以降、auth.030 メッセージと auth.108 メッセージの両方で送信する必要がある。 [当初証拠
金担保ポートフォリオ コード] が取引に適用されない場合は、 「該当なし」を表す値 [NOAP] を送信する。  
• ポートフォリオレベルの担保情報の場合 

---

## Page 22

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 22  
 
o 2 種類のポートフォリオコードが定義されている（Initial [[Margin]] Portfolio Code と Variation [[Margin]] 
Portfolio Code）。 [[collateral]] Portfolio Indicator が「true」の場合、各担保メッセージには少なくと
もどちらかの入力が必要。 
o ポートフォリオレベルの担保情報には、指定された Initial [[Margin]] Portfolio Code および/または
Variation [[Margin]] Portfolio Code を含む 1 つまたは複数の対象取引が存在するかの検証を行う。 
o 金融庁はポートフォリオレベルによる担保情報報告の場合、Initial [[Margin]] Portfolio Code もしくは 
Variation [[Margin]] [[collateral]] Portfolio Code のいずれかの報告を必須としているため、GTR がデータ
を取り込む際の検証ルールで対象となるベース取引が最低でも 1 件は存在するかどうか参照するのは、
MARU のメッセージに含まれる二つのポートフォリオコードの結合値（大文字、小文字を区別する）に対応
する取引が存在するかである。 
 
金融庁への担保情報報告用に、利用者ごとに「0」から始まる新たな O コードが新たに設定される予定（アセットクラスに合わ
ないため、既存の顧客 O コードは使用できない）。  
担保情報は、 Trade State Report には統合されず、日次の [[Margin]] Submission Report、 [[Margin]] Activity 
Report、 [[Margin]] State Report に反映される予定。 担保情報に関するレポートの詳細については、本文書のレポートセク
ション（FC 5 レポート）を参照のこと。 
  

---

## Page 23

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 23  
 
FC 3.6: 時価情報の提出 
制度改正により、取引の時価情報の提出も報告必須要件として加えられた。 
取引の時価情報は、アクションタイプ "VALU" で示される Value message を使って GTR に提出する必要がある。 
時価情報は、提出された時価情報が対象とする取引（UTI + 取引当事者 1 + 取引当事者 2 + 法域が一致する必要
がある）が存在する場合にのみ受領される。対象取引のない時価情報は受領不可（NACK）となる。 
すでに現存していない取引（満期または解約済み）に対して提出された時価情報は、受け付ける。この場合、時価情報の提
出はデイリーアクティビティーレポートでアクティビティーとして報告されるが、監督当局と取引参加者の双方の Trade State 
Report には掲載されない。 
メッセージ・スペシフィケーションに基づき、「誤提出」（アクションタイプ EROR）または 「転出」（アクションタイプ PRTO）とされ
た取引についての時価情報は受領不可(NACK)となる。 
FC 3.7: 取引当事者（Reporting Counterparty）と 報告義務者 
（Entity Responsible for Reporting） 
報告義務者 (ERR)は、今回の制度改正により新たに導入された項目で、「報告義務を負う金融機関等の識別子」と定義さ
れる。概ね、取引当事者（RCP）= 報告義務者（ERR）であるが、金融庁向け の報告における例外として、信託勘定分
（ファンド）の報告がある。この場合では、信託銀行（受託者） = ERR、ファンド = RCP となる。金融庁発表のガイドライン
に基づく信託勘定の報告に関する検証ルールの条件は以下の通り。 
(a) ファンドの金融庁報告を行う金融機関（信託銀行等）がサービスの役割として ”Trust Bank”(信託銀行)のみを選択
している場合、取引当事者１（RCP），取引当事者２（OCP）のいずれになっていても受領不可となる。つまり、口座管
理システムの SDO で “Trust Bank”として設定されている金融機関は取引当事者になることはできない。 
 


---

## Page 24

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 24  
 
(b)報告義務者（ERR）と 取引当事者（RCP）は、取引情報提出時に検証される GLIEF のデータベース上で有効な 
LEI を保持している必要がある。取引情報提出主体（Report Submitting Entity）と 報告責任者（ERR）は共に金
融庁報告のために GTR の顧客属性管理システムである SDO に登録されており、有効なアカウントでなければならない。データ
取り込み時に、RSE <-> ERR の間に提出権限許可が適切に設定されているかどうかを確認する検証ルールが実装される予
定である。RSE と ERR が異なる場合、Manage Services で提出権限許可を設定する必要があるが、RSE = ERR の場
合、設定は不要である。想定されるシナリオを説明するために、いくつかのユースケースを以下に記載する。  
ケー
ス 
役割 
権限
許可
設定 
コメント 
Case 
1 
信託銀行 A（取引情報収集契約
締結済）= 報告義務者（ERR）
且つ取引情報提出主体
（RSE）。 
ファンド A = CP1 取引当事者
(RCP)。 
無 
ほとんどがこのケースに該当。取引情報報告制度上、ファンド A が
取引当事者の項目にその LEI を付記するが GTR 上、口座開設
を要しない。これは受託者である信託銀行がファンド A の取引にお
いても法的に取引当事者となるため、自社報告（ self-
reporting）と見なされ権限許可設定は不要。  
Case 
2 
信託銀行 B（取引情報収集契約
締結済）= 取引情報提出主体
（RSE）。 
信託銀行 A（取引情報収集契約
締結済）= 報告義務者
（ERR ）。 
ファンド A = CP1 取引当事者
(RCP)。 
有 
信託銀行 B は、第三者として報告義務者（ERR）である信託
銀行 A のために取引情報提出主体となるので、報告権限許可
設定が必要。 
信託銀行 A はマネージサービスにおいて権限許可設定のリクエス
トを承認する必要がある。 
（ｃ）第三者のサービスプロバイダーが取引当事者（CP1 及び CP2）として報告することはできない。いかなるアクションタイ
プで報告しても受領不可となる。 
  

---

## Page 25

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 25  
 
FC 3.8: アクションタイプとイベントタイプの検証 
制度改正実施日以降、GTR に提出する取引情報には、適切な "Action Type "と "Event Type "の値が必要である。 
これらの値は、「ステートレス」検証（すなわち、メッセージの内容のみに基づいて実行できる検証）と「ステートフル」検証（すな
わち、当該取引に関する以前の取引情報の内容を参照することによってのみ実行できる検証）の両方の検証を通過しなけれ
ばならない。 
ステートレス“Stateless” 検証 
この検証によって、"Action Type "と "Event Type " 項目の有効な組み合わせを特定する。メッセージ・スペシフィケーション
には "Action type & Event type "というタブがあり、すべてのメッセージにおいて有効な組み合わせの詳細が記載されてい
る。 これらの組み合わせは、メッセージの内容のみに基づいて検証することとなるため、シミュレーターを使用してテストすることがで
きる。 
ステートフル“Stateful” 検証 
この検証では、アクションタイプの許容される順序を制御する。 個々の新たに GTR で受領する取引情報は、以下の図に示す
通り、アクションタイプが許容される順序となっているか確認する。 この検証は、個別取引ごと（取引の独自性 3.4 項参照）、
且つ、法域ごとに行われる。メッセージ・スペシフィケーションには常に最新版を掲載する。 
主なポイントは以下の通りである。なお、金融庁は、一貫性を保持するために ESMA 方式を採用する。 
• 新規取引に関する最初の取引情報送信は、NEWT である必要がある。 
• 取引が満期を迎えた場合は、アクションタイプの送信は不要。 GTR 内のエンド・オブ・デイのプロセスでは、満期日当
日にトレードステートレポート（TSR）から満期の取引が削除される（現行の仕様と同様）。下の図では、この処理
により、取引は「Outstanding」から「Terminated」の状態に論理的に移行する。TERM で報告された情報はベー
スとなる取引情報と UTI＋RCP＋OCP（取引情報識別子と取引当事者１と２）の組み合わせが一致していれば
受領される。 
• 満期または既に解約した取引に対しては、 MODI、CORR、VALU、MARU の値によって、過去の報告の内容（取
引情報、時価情報、担保情報）を修正することができる。 提出する場合、関連する日付が正確であることを確認す
る必要がある。満期または解約済みの取引情報の修正（MODI）、訂正（CORR）の場合は、UTI+RCP（取
引識別子と取引当事者１）の組み合わせで取引と紐づける。 
• そのため、REVI を送信する前に取引相手である OCP の情報を変えることは可能になってしまうが、まずは REVI で
満期もしくは解約済みとなった時点で取引情報を提出し、GTR による受領を確認してから、MODI や CORR で
OCP を変更することが必要である。 
• TERM、EROR、PRTO の値が提出されると、当該取引は提出日当日のトレード・ステート・レポート (TSR)には表
示されなくなる。 取引が解約またはエラーとして報告した場合でも、TSR に再び表示されるのを望むのであれば、

---

## Page 26

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 26  
 
REVI の値（満期日が明日以降）を送信する必要がある。TERM、EROR、PRTO に対して、既存ポジションの
UTI＋RCP+OCP の組み合わせに該当するものがあるか検証する。 
• REVI を提出する際には、削除される前と同一の UTI+RCP+OCP（取引識別子＋取引当事者１，２）の組み
合わせであることが必要。GTR で UTI+RCP+OCP の既存の組み合わせをチェックする。  REVI が提出された日より
も先の満期日の場合はステータスが Terminated または Errored から、 “Outstanding” になり、過去の満期日
の場合は REVI を提出してもステータスは “Terminated” のままとなる。 REVI によって早期解約日の修正、訂正
はおこなうことは可能。  
• REVI を提出して GTR で受領された後に、MODI や CORR を提出して、OCP（取引当事者２）を含むその他の
項目情報を変更することが可能となる。  
• VALU と MARU を提出する際には紐づける取引情報は UTI+RCP+OCP（取引識別子と取引当時者１，２）
の組み合わせである。  
• 担保情報の更新をする際の紐づけのロジックは、その対象取引に対してどのように担保の計算をしているかによって異な
る。  
a. ポートフォリオレベルでなく、取引レベルで担保を計算している場合は、UTI+RCP+OCP（取引識別子と取
引当事者１，２）の組み合わせで判断する。参照する取引が明示されない場合には MARU を提出しても受領不
可となる。  
b. ポートフォリオレベルで担保を計算している場合は、当初証拠金 IM ポートフォリオコードと変動証拠金 VM
ポートフォリオコードが必要であり、紐づけには各ポートフォリオコード＋RCP+OCP（取引当事者１，２）の組み合
わせで判断する。MARU が受領されるためには、すくなくとも 1 つは既存の UTI が含まれるポートフォリオである必要
がある。  
紐づけは実際にトレードステートレポート（TSR）と担保の評価額を実際につなぐものではなく、マージンステートレポートと
TSR を突合作業する際に用いることができる。 
• 金融庁報告特有の制度だが、前年度の為替と金利のデリバティブ取引の平均残高の合算が 3000 億円の閾値を
超えている場合は翌年度の 7 月から取引報告が必要となると定められている。毎年の平均残高の計算で、閾値を下回
り、取引報告が免除される場合は金融庁および DDRJ に対して書面の提出が必要となる。報告が不要になった金融機
関は GTR からポジションを削除する作業が必須となる。作業が完了しない場合は、そのまま DDRJ から口座管理手数料
およびポジションに対する手数料、双方の課金が継続されることに注意。報告免除を知らせるための書面は日本語で金融
庁と DDRJ に提出することになっており、ポジションを GTR から削除する際には、 Action type=PRTO (Transfer 
out) と Event type =PTNG (Transfer)の組み合わせで取引情報削除の作業を行う。その後の年度の計算で、再び
閾値を超えて、報告義務が発生した場合は、DDRJ に報告再開の連絡を行い、残高として報告する取引の UTI（前に
報告した時と同一の値でなくても受領する）、 Action Type=NEWT と適切と思われる Event Type 項目の組み合
わせを使って再報告を行う。理由としては、GTR では通常の新規取引の報告と閾値を超えたことによる報告再開の判別を
することが不可能であるため。  
 

---

## Page 27

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 27  
 
 
１．＊満期日が明日以降（今日より先の日付） 
２．＊＊満期日が本日を含む過去の日付 
３．Revive により復元される取引のステータスは満期日によって異なる 
４．満期日当日には報告は不要。満期日の日付が誤っている場合は、アクションタイプ REVIVE で Outstanding のステー
タスに戻すことが可能。 
５．MODI や CORR は満期日が明日以降の場合は未来の日付を入力して報告可能。しかし解約後の取引について
MODI や CORR は受領不可。いったん REVI を送信してポジションを復元して Outstanding ステータスにしてから修正するこ
と。 
６．REVI は満期日を未来日付で提出可能。例）満期日が明日以降の場合、Matured（Non-Outstanding）のステ
ータスから Outstanding に翌日更新される。 
７．全ての MARU（担保情報報告）報告には取引レベル・ポートフォリオレベルともに、紐づけるベース取引が必要。ベース
取引が無い場合はリジェクト（受領不可）となる。 
８．移管（Transferred Out）ステータスの情報については、NEWT（イベントタイプはいずれも可）で転入（Transfer 
In）できる。 
９．解約（Terminated）ステータスの情報について、過去の満期日で REVI を送信してもステータスは Terminated のま
ま。 
１０．取引情報が受領された後に [[EOD]] で実施する満期日の処理によってステータスは変更されることがある。 
 


---

## Page 28

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 28  
 
 
下記のケースシナリオ例を参照のこと 
 
シナリオ  Sub#  
アクショ
ンタイプ 
イベント
タイプ 
UTI  RCP  OCP  
担保ポートフォリオ   
(Initial/Variation)
  
検証ルール  
想定される
結果  
コメント  
UC1  
1  NEWT  TRAD  123  Bank 
A  
Bank 
B  
NA  UTI+RCP  ACK     
2  MODI  TRAD  123  Bank 
A  
Bank 
B  
NA  UTI+RCP  ACK  UTI と RCP の組み合
わせで検証するので、
この UTI の報告は受
領される。 
UC2  
1  NEWT  TRAD  123  Bank 
A  
Bank 
B  
NA  UTI+RCP  ACK     
2  MODI  TRAD  123  Bank 
A  
Bank 
C  
NA  UTI+RCP  ACK  UTI と RCP の組み合
わせで検証するので、
取引相手である OCP
が変更となっていても、
この UTI の報告は受
領される。  
UC3  
1  NEWT  TRAD  123  Bank 
A  
Bank 
B  
NA  UTI+RCP  ACK     
2  MODI  TRAD  123  Bank 
B  
Bank 
A  
NA  UTI+RCP  NACK  UTI と RCP の組み合
わせで検証するとベー
スとなる取引が存在し
ないので受領不可とな
る。  
UC4  
1  NEWT  TRAD  123  Bank 
A  
Bank 
B  
NA  UTI+RCP ACK  
 
2  TERM  ETRM  123  Bank 
A  
Bank 
B  
NA  UTI+RCP+O
CP  
ACK  UTI と RCP と OCP
の組み合わせで検証
するので、この UTI の
情報は受領される。  
3  REVI*  NA  123  Bank 
A  
Bank 
B  
NA  UTI+RCP+O
CP  
ACK  UTI と RCP と OCP
の組み合わせで検証
するので、この UTI の
情報は受領される。  
UC5  
1  NEWT  TRAD  123  Bank 
A  
Bank 
B  
NA  UTI+RCP  ACK     
2  TERM  ETRM  123  Bank 
A  
Bank 
B  
NA  UTI+RCP+O
CP  
ACK     
3  REVI*  NA  123  Bank 
A  
Bank 
C  
NA  UTI+RCP+O
CP  
NACK  UTI と RCP と OCP
の組み合わせで検証
するので、この UTI の

---

## Page 29

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 29  
 
情報は受領不可とな
る。  
UC6  
1  NEWT  TRAD  123  Bank 
A  
Bank 
B  
NA  UTI+RCP  ACK     
2  TERM  ETRM  123  Bank 
A  
Bank 
B  
NA  UTI+RCP+O
CP  
ACK     
3  REVI*  NA  123  Bank 
B  
Bank 
A  
NA  UTI+RCP+O
CP  
NACK  ベースとなる取引が存
在しないので受領不
可となる。  
  
金融庁はアクションタイプについて 2022 年 8 月に発行された下記の CDE 市中協議文書の定義を採用している。  
 
 
アクションタイプ  有効値  報告する内容  
New  NEWT  The creation of the first transaction resulting in the 
generation of a new UTI.  
Modify  MODI  A modification of the terms of a previously reported 
transaction due to a newly negotiated modification 
(amendment) or a filling in of previously missing 
information (e.g., post price transaction). It does not 
include correction of a previously reported transaction.  
Correct  CORR  A correction of erroneous data of a previously reported 
transaction.  
Terminate  TERM  A termination of an existing transaction.  
Error  EROR  A cancellation of a wrongly submitted entire transaction in 
case it never came into existence or was not subject to the 
reporting requirements under the applicable law of a given 
jurisdiction, or a cancellation of a duplicate report.  
Revive  REVI  An action that reinstates a reported transaction that was 
reported with action type “Error” or terminated by mistake 
or expired due to an incorrectly reported Expiration date.  
Valuation  VALU  An update of a valuation of a transaction. There will be no 
corresponding Event type.  
[[collateral]] or 
[[Margin]] 
update  
MARU  An update to [[collateral]] [[Margin]] data. There will be no 
corresponding Event type.  
Transfer out  PRTO  A transfer of a transaction from one trade repository to 
another trade repository (change of trade repository).  
 

---

## Page 30

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 30  
 
Action type 値 許容値 報告する内容 
New NEWT 新しい取引情報を報告するときのアクション。新規 UTI 付与による最初の取引情報報告に
適用 
Modify MODI 以前に提出した取引の状態を変更（クレジットイベントなど）、取引相手と新たに合意した
変更、又は以前に不足していた情報を追記する場合等の理由により、以前に提出した取引
情報を変更するアクション。これには、以前の取引自体の訂正は含まれない。 
Correct CORR 以前に提出した取引が誤っていた場合にデータを訂正するアクション 
Terminate TERM 新しいイベント(コンプレッション、ノベーションなど)によりのために既存の取引を終了するアクショ
ン。（ただし、契約上の満期日に終了する取引には適用しない。） 
Error EROR 取引が存在しなかったにもかかわらず、誤って取引情報が報告された場合、又は報告対象で
はなかったが誤って報告された場合に、誤って提出された取引情報を取り消すアクション。重
複データの取り消しを行う際にも適用。 
Revive REVI エラーとして報告された、又は誤って終了した取引情報を復元するアクション。 
Valuation VALU 時価情報の報告用アクション・対応するイベントタイプはなし。 
[[collateral]] or 
[[Margin]] update 
MARU 担保情報の報告用アクション。対応するイベントタイプはなし。 
Transfer out PRTO 取引情報蓄積機関の間で取引情報を移管する場合のアクション (ＴＲの変更) 
 
Event type Allowable 
value 
Details to be reported 
Trade TRAD A creation or modification of a transaction. 

---

## Page 31

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 31  
 
[[Novation]] NOVA A [[Novation]] legally moves partial or all of the financial risks of a swap 
from a transferor to a transferee and has the effect of 
terminating/modifying the original transaction and creating a new 
transaction to identify the exposure between the 
transferor/transferee and remaining party. 
Compression COMP Compressions and risk reduction exercises generally have the effect 
of terminating or modifying (i.e., reducing the notional value) a set of 
existing transactions and of creating a set of new transaction(s). 
These processes result in largely the same exposure of market risk 
that existed prior to the event for the counterparty. 
Early 
Termination 
ETRM Termination of an existing swap transaction prior to scheduled 
termination or maturity date. 
Clearing CLRG Central clearing is a process where a [[Derivatives]] clearing organization 
interposes itself between counterparties to contracts, becoming the 
[[Buyer]] to every [[Seller]] and the [[Seller]] to every [[Buyer]]. It has the effect of 
terminating an existing transaction between the [[Buyer]] and the [[Seller]] 
and thereby ensuring the performance of open contracts. 
Clearing & 
Allocation 
CLAL A simultaneous clearing and allocation event in a [[Derivatives]] clearing 
organization 
Exercise EXER The process by which a counterparty fully or partially exercises their 
rights specified in the contract of an [[Option]] or a swaption. 
Allocation ALOC The process by which an agent, having facilitated a single swap 
transaction on behalf of several clients, allocates a portion of the 
executed swap to the clients 

---

## Page 32

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 32  
 
Credit Event CREV An event or trigger that results in the termination or modification of 
the state of a previously submitted credit derivative transaction. 
Applies only to credit [[Derivatives]]. 
Corporate 
Event 
CORP A corporate action on [[Equity]] underlying that impacts the transactions 
on that [[Equity]]. 
Transfer PTNG The process by which a swap is transferred to another SDR that has 
the effect of the closing of the swap transaction at one SDR or 
opening of the same swap transaction using the same UTI/USI in a 
different SDR (new). 
Upgrade UPDT An upgrade of an outstanding transaction performed in order to 
ensure its conformity with the amended reporting requirements. 
 
イベントタイプ 許容値 報告する内容 
Trade TRAD 取引の作成又は変更。 
[[Novation]] NOVA ノベーションとは、取引にかかる債権債務の一部又は全部を譲渡や移転することで取引相手を
変更することを意味する。実質的には、該当するとりを終了もしくは修正し、引き続き取引当
事者となるものと譲渡や移転を受けたものとの間に新しい取引の締結を生む効果を持つ。 
Compression COMP コンプレッションとは、一般に複数もしくは単数の取引当事者が概ね同種のリスクを包含する複
数の取引を、合意の上同時に解約することにより鳥肥残高（想定元本金額、件数）の圧
縮、削減を図ることを意味する。その結果、一連の新規取引が創出されることになる。 
Early 
Termination 
ETRM 当初契約された終了日又は満期日より前に、既存のスワップ取引を終了すること。 

---

## Page 33

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 33  
 
Clearing CLRG 清算とは、清算機関が両取引当事者から取引にかかる債務を引き受けることにより、それぞれ
の取引当事者の新たな取引当事者になることをいう。その結果、相対取引で成立していた取
引は終了となり、新たに一方の取引当事者対清算機関、他方の取引当事者対清算機関の
2 つの取引が私立することなる。 
Clearing & 
Allocation 
CLAL デリバティブ清算機関が行う同時清算・割当行為。 
Exercise EXER オプション又はスワップション取引における、権利保有者により一部もしくは全部の取引について
権利行使が行われることをいう。 
Allocation ALOC 執行されたブロック取引を適切な複数のサブアカウントに割り当てるプロセス。 
Credit Event CREV クレジットイベントの発生により、以前に報告していた取引情報を修正もしくは終了する場合に
適用。クレジット・デリバティブ特有のイベント。 
Corporate 
Event 
CORP 原資産である株式に発生したコーポレートアクションが、デリバティブ取引にも影響を与える場合
に適用。 
Transfer PTNG 取引情報が別の TR に移管される場合、元の TR で取引を終了し、新たな TR で同じ UTI
を使用し新規に報告を開始する場合に適用。 
Upgrade UPDT 改訂もしくは新たに設定された報告要件を満たすために取引情報を更新する場合に適用。 
 
制度改正実施時にオープンポジションとして現存している取引について、[[DTCC]] は直前の週末にそれらの取引の情報を初期化
し、制度改正実施後に報告される後続するアクションタイプに対して検証ルールに従い受領できるようにする。このロジックについ
ては、本書第 6 章にてさらに詳しく説明する。 
FC 3.9: 検証を緩和する取引情報の種類  
制度改正後、一部の取引情報においては（アクションタイプ=TERM、EROR、PRTO）、引き続き検証を緩和する。 これらの
アクションタイプは、アクションタイプ=NEWT または MODI の提出の場合と同じ検証用スキーマを使用するが、いくつかの項目に
ついては、同じ検証作業を行わない。詳細はメッセージ・スペシフィケーションに記載されている。 

---

## Page 34

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 34  
 
FC 3.10: 取引相手の変更 
現行金融庁向け報告の GTR では、USI+RCP1+RCP2 の組み合わせで取引の独自性を判断している。取引の相手方
（RCP2）を変更するためには、一旦、当該取引情報を削除してから、再度報告を行う必要がある。この再報告の際には、も
ともと使用していた USI の値 を再利用することが可能となっている。 
• 金融庁は、今後、誤って報告された 取引相手（RCP2） を修正するために、EROR に続いて NEWT（新たな取
引識別子 UTI を含む）を提出することを認めるが、報告された UTI が唯一であるかどうかの確認は行わない。 
• 取引の独自性ロジックの変更により、Action Type が MODI または CORR のいずれであっても、NEWT と異なる 
RCP2 の提出が可能になる。 
下記の例を参照のこと。 
ケースシ
ナリオ 1 
                
報告の
順番# 
アクション
タイプ 
イベント
タイプ 
UTI 
Submitt
ed For 
Party 1 
(RCP) 
Part
y 2 
(OCP
) 
受領可
否結果 
コメント 
1 NEWT TRAD 123 Bank A Bank A 
Bank 
B 
ACK   
2 NEWT TRAD 123 Bank B Bank B 
Bank 
A 
ACK 
GTR は、同一の UTI を複数の異な
る RCP が使用しても、受領する 
3 MODI TRAD 123 Bank A Bank A 
Bank 
C 
ACK 
同じ UTI+RCP で取引相手 OCP
の修正報告が可能 
4 NEWT TRAD 123 Bank B Bank B 
Bank 
A 
NACK 
2 番で既に UTI+RCP の組み合わ
せが使用されており、2 番と 4 番は同
じ内容なのでアクションタイプ NEWT
は受領不可となる。 
5 NEWT TRAD 123 Bank D Bank D Bank 
A 
NACK GTR は、同一の UTI を複数の異な
る RCP が使用しても、受領する 
 
ケース
シナリ
オ 2 
                
報告の
順番 
アクショ
ンタイプ 
イベント
タイプ 
UTI 
Submitted 
For 
Party 
1 
(RCP) 
Party 
2 
(OCP) 
受領可
否結果 
コメント 
1 NEWT TRAD 123 Bank A Bank A Bank B ACK   

---

## Page 35

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 35  
 
2 TERM NOVA 123 Bank A Bank A Bank B ACK   
3 TERM NOVA 123 Bank A Bank A Bank B NACK 
既に取引が存在しないため、解約は
できない。 
4 NEWT TRAD 123 Bank A Bank A Bank B NACK 
UTI テクニカル・ガイダンスでは、以
前に使用したトランザクションが既に
オープンポジションでない場合でも 
UTI を再使用することはできないとし
ているが、UTI を再利用しているかど
うかの検証は行わない。 
UTI テクニカルガイダンスで UTI の
再利用はできないとされているので、
JFSA 報告でも検証をかけることにな
った。 
 
FC 3.11: 取引報告当事者 TP1 の変更 
現行及び制度改正後においても、取引当事者（Trade Party1） を変更するためには、一旦取引を削除し、再度報告を
行う必要がある。この再報告の際には、もともと使用していた取引識別子（UTI）を再利用することが認められている。  
ケースシ
ナリオ 3 
                
報告の
順番 
アクション
タイプ 
イベント
タイプ 
UTI 
Subm
itted 
For 
Part
y 1 
(RCP
) 
Party 
2 
(OCP) 
受領可
否結果 
コメント 
1 NEWT TRAD 123 
Bank 
A 
Bank 
A 
Bank 
B 
ACK   
2 
TERM/E
ROR 
- 123 
Bank 
A 
Bank 
A 
Bank 
B 
ACK   
3 NEWT TRAD 123 
Bank 
C 
Bank 
C 
Bank 
B 
ACK 
UTI テクニカル・ガイダンスでは、以前に使
用したトランザクションが既にオープンポジシ
ョンでない場合でも UTI を再使用すること
はできないとしているが、UTI を再利用して
いるかどうかの検証は行わない予定。(後日
詳細発表) 
UTI テクニカルガイダンスでは UTI の再利
用はできないとされているので、JFSA 報告
でこのルールを適用。しかしこのケースでは
UTI+RCP の組み合わせが 1－2 とはこと
なるので受領する。 
FC 3.12: JFSA 報告用 XML ユーセージガイドライン 

---

## Page 36

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 36  
 
金融庁報告では 4 つのメッセージタイプのうち、リアルタイム報告を除く 3 つのメッセージタイプを使用する。 
(i) トランザクション（取引）報告 – auth.030.001.03_JFSAUG_DATTAR_1.0.0 
(ii) 時価情報報告 – auth.030.001.03_JFSAUG_DATTAR_1.0.0 
(iii) 担保情報報告 – auth.108.001.01_JFSAUG_DATMDA_1.0.0 
 
トランザクション（取引）報告と時価情報報告は同じデータ取り込みスキーマを共有するが、ユーセージガイドライン (以下 UG)
は、提出される項目ごとの定義を金融庁報告に沿う内容に厳格化した定義を示すものである。例えば、
auth.030.001.03.xsd のベースラインスキーマでは、時価情報報告において取引のエコノミクスを示す項目を提出することが
可能だが、UG ではこれを厳格化し、時価評価関連の項目のみを含むべきであるとする。UG は、ベースラインスキーマを特定法
域への報告用に厳格化したものである。 
 
UG は SWIFT 社の MyStandards ポータルを通じて登録される。[[DTCC]] は金融庁との合意に基づき、UG の発行と保守を
行う。一方で、[[DTCC]] は MyStandards を利用しなくても、利用者が UG を閲覧・ダウンロードできるように XSD、PDF および
/または Excel の様式で配布する予定。ただし、この UG は MyStandards ポータルで非公開として設定され、[[DTCC]] はこの
UG の閲覧および利用希望者を MyStandards にて承認する必要がある。 
 
ユーセージガイドラインでは以下を網羅する。 
  
1. ISO ベースライン・スキーマが任意としているアクションタイプによる検証を必須とする。 
2. ISO ベースライン・スキーマより厳格な数値設定。 
3. ISO ベースライン・スキーマより厳密な書式設定 
4. アクションタイプ別に分類された 金融庁報告に適用されない項目が利用者から提出された場合、ユーセージガイ
ドラインに 基づき無効なスキーマとして受領不可とする。 
 
利用者向けに、サンプルメッセージもラーニングセンターに掲載されている。 
FC 3.13: 新たな集約型 O-Code の導入 
制度改正に伴い、利用者はすべてのアセットクラスを 8ABC に統合するか、既存のアセットクラス別の（つまり、2 = CO、3 = 
クレジットなど）を継続するかを選択できる。8ABC は、提出された全てのデータを集約した O-code となり、既存のアセットクラ
ス別の 2 ～ 6 で始まる O コードで提出される内容を網羅する。これは必須ではなく、利用者が採用するかどうかの選択が可
能である。集約型の 8ABC を利用することで、アセットクラスにとらわれず全ての取引情報のレポートを一元化して取得できるこ
とになる。0ABC は担保情報レポート用に存続する。この機能は今回の制度改正の対象ではなく、利用者の利便性を向上す
るための追加機能であるため、他の制度改正対象の機能提供より優先順位を下げざるをえず、2024 年第 1 四半期後半以
降に UAT 環境においての導入となる見込み。よって 2024 年 4 月 1 日の制度改正実施当初から利用することはできない。 
 

---

## Page 37

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 37  
 
FC 3.14: Other Payment 項目 
 
金融庁報告制度改正後の報告では、Other Payment 項目に関連して下記に掲載する 6 つのデータ項目の情報を参照す
る。  
1. Other payment amount  
2. Other payment type  
3. Other payment currency  
4. Other payment date  
5. Other payment payer  
6. Other payment receiver  
  
これらの項目は複数の値の入力が可能であり、各項目内の値に矛盾がないかどうかの検証を行う。例）複数の値が入力され
ている場合、Other payment amount, Other payment type, Other payment currency, Other payment 
date, Other payment payer および Other payment receiver 項目に入力されている値の数が一致していることが必
要。値の数が合致しない場合は、受領不可となる。 
詳細についてはメッセージ・スペシフィケーションに記載のビジネスルール欄を参照のこと。  
  
CSV ファイルの場合は、以下の Other payment type 項目として提出された値を独自性を判断するための鍵として使用し、
[[EOD]] の Trade State Report（TSR）に反映する。  
Other Payment 項目で独自性を判断する鍵となる項目: 
a. Other payment type 
b. Other payment date  
c. Other payment payer 
d. Other payment receiver 
 
Other Payment 項目の独自性判断材料に基づいて以下の処理を行う： 
 
(a) 独自性判断の鍵が同じ条件の場合は、最新の Event Timestamp の値を使って最新の情報が保存される。 
(b) 独自性判断の鍵となる条件に変更がある場合、新たに提出された項目の値は集積されて、各項目ごとに Trade State 
Report に表示される。例えば、NEWT として Payment Type=UFRO の報告後に、アクションタイプ MODI で PEXH が提
出された場合、Other Payment 項目の独自性を判断する鍵の 4 つのうちの 1 つが変更されたことになる。そのため PEXH
で提出された詳細内容は NEWT で報告された内容に追加し、TSR に反映される。。（追加された情報はセミコロンで区分さ
れて表示される。）NEWT の内容に上書きしないことに注意。 
(c) アクションタイプ = CORR は以前提出された Payment 情報の詳細を訂正するため、もしくは other payment 
amount = 0 を使って以前報告すべきではなかった支払い項目の組み合わせの金額を取り消すために使用できる。  
 
下記の Other Payments 関連の表の例を参照のこと。(内容が更新されているので注意)  

---

## Page 38

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 38  
 
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
1 NEWT UFRO LEI123 LEI456 GBP 100 
2023-
02-20 
UFRO LEI123 LEI456 GBP 100 
2023-02-
20 
新規取引として 
Other Payment 
項目を提出した内容
がレポートに表示され
る。 
2 MODI UFRO LEI123 LEI456 USD 100 
2023-
02-20 
UFRO LEI123 LEI456 USD 100 
2023-02-
20 
 Other Payment 
項目の独自性判断
の鍵である[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] に変更が
ないので、[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver]の組み合
わせは同じ。最新の
情報を表示する。 

---

## Page 39

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 39  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
3 MODI UFRO LEI123 LEI456 GBP 100 
2023-
03-20 
UFRO 
UFRO 
LEI123 
LEI123 
LEI456 
LEI456 
USD 
GBP 
100 
100 
2023-02-
20 
2023-03-
20 
Other Payment 
項目の独自性判断
の鍵である[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] が変更さ
れた。[Other 
payment date] が
更新された[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver]の組み合
わせが異なるのでレポ
ート上に追加された。 
4 MODI UFRO LEI123 LEI456 USD 100 
2023-
03-20 
UFRO; 
URFO 
LEI123; 
LEI123 
LEI456; 
LEI456 
USD; 
USD 
100; 
100 
2023-02-
20; 
2023-03-
20 
Other Payment 
項目の独自性判断
の鍵である[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] の組み合
わせは既に存在する
ので、最新の情報に
更新する。 

---

## Page 40

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 40  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
5 MODI UFRO LEI123 LEI456 USD 300 
2023-
03-20 
UFRO; 
URFO 
LEI123; 
LEI123 
LEI456; 
LEI456 
USD; 
USD 
100; 
300 
2023-02-
20; 
2023-03-
20 
前回提出された組み
合わせのうち 1 つの
内容が変更になって
いる。[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] の値は同
じだが、[Other 
payment 
amount] の内容は
更新されている。 
[Other Payment 
Type] & [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver]の組み合
わせは同じなので、変
更箇所の最新の値が
表示される。 

---

## Page 41

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 41  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
6 MODI PEXH LEI123 LEI456 USD 500 
2023-
04-20 
UFRO; 
URFO; 
PEXH 
LEI123; 
LEI123; 
LEI123 
LEI456; 
LEI456; 
LEI456 
USD; 
USD; 
USD 
100; 
300; 
500 
2023-02-
20; 
2023-03-
20; 
2023-04-
20 
Other Payment 
項目の独自性判断
の鍵である[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] に変更が
ある。[Other 
payment Type] 
が更新されている。 
[Other Payment 
Type] & [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] の組み合
わせが異なるので、新
たに今回提出された
内容が追加されてレ
ポートに表示される。 

---

## Page 42

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 42  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
7 MODI 
PEXH; 
PEXH 
LEI123;LEI45
6 
LEI456; 
LEI123 
USD; 
GBP 
500; 
160 
2023-
04-20; 
2023-
05-20 
UFRO; 
URFO; 
PEXH; 
PEXH 
LEI123; 
LEI123; 
LEI123; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123 
USD; 
USD; 
USD; 
GBP 
100; 
300; 
500; 
160 
2023-02-
20; 
2023-03-
20; 
2023-04-
20; 
2023-05-
20 
[Other Payment 
Type] & [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] の組み合
わせが異なる。
[Other payment 
date] が追加で提
出されている。 
[Other Payment 
Type] & [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] の組み合
わせが異なるので、今
回提出された内容が
新たに追加されてレ
ポートに表示される。 

---

## Page 43

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 43  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
8 MODI 
PEXH; 
PEXH 
LEI123; 
LEI456 
LEI456; 
LEI123 
USD;GBP 400;320 
2023-
04-20; 
2023-
05-20 
UFRO; 
URFO; 
PEXH; 
PEXH 
LEI123; 
LEI123; 
LEI123; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123 
USD; 
USD; 
USD; 
GBP 
100; 
300; 
400; 
320 
2023-02-
20; 
2023-03-
20; 
2023-04-
20; 
2023-05-
20 
前回提出分の組み
合わせのうち 1 つに
変更があり。[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] の値は同
じだが、[Other 
payment 
amount]の値が更
新されている。 
[Other Payment 
Type] & [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver]の組み合
わせが同じなので、変
更箇所の最新の値が
レポートに表示され
る。 

---

## Page 44

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 44  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
9 MODI UWIN LEI456 LEI123 USD 100 
2023-
04-18 
UFRO; 
URFO; 
PEXH; 
PEXH; 
UWIN 
LEI123; 
LEI123; 
LEI123; 
LEI456; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123; 
LEI123 
USD; 
USD; 
USD; 
GBP; 
USD 
100; 
300; 
400; 
320; 
100 
2023-02-
20; 
2023-03-
20; 
2023-04-
20; 
2023-05-
20; 
2023-04-
18 
[Other Payment 
Type]の値が
'UWIN'で提出され
ている。 
[Other Payment 
Type] & [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver]の組み合
わせが異なるので、 
今回提出された内容
が追加されてレポート
に表示される。 
*注釈 'UWIN'は、
過去に提出した内容
の訂正に使われる。 
[Other Payment 
Type] ='UWIN' 
は、この情報の提出
が行われた 2023 年
4 月 18 日時点で取
引自体が全額解約
されたことを示す。. 

---

## Page 45

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 45  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
1
0 
MODI UFRO LEI456 LEI123 USD 300 
2023-
03-20 
UFRO; 
URFO; 
PEXH; 
PEXH; 
UWIN; 
UFRO 
LEI123; 
LEI123; 
LEI123; 
LEI456; 
LEI456; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123; 
LEI123; 
LEI123 
USD; 
USD; 
USD; 
GBP; 
USD; 
USD 
100; 
300; 
400; 
320; 
100; 
300 
2023-02-
20; 
2023-03-
20; 
2023-04-
20; 
2023-05-
20; 
2023-04-
18; 
2023-03-
20 
Other Payment 
項目の独自性判断
の鍵である[Other 
Payment Type] 
& [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver] の内容に
変更がある。Other 
payment payer] 
& [Other 
payment 
receiver]が更新さ
れている。 
[Other Payment 
Type] & [Other 
payment date] & 
[Other payment 
payer] & [Other 
payment 
receiver]の組み合
わせが異なるので、今
回提出された内容が
追加されてレポートに
表示される。 

---

## Page 46

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 46  
 
順
番
: 
GTR への XML 提出ファイルの値 CSV レポートで表示される値 
コメント Actio
n 
Type 
Other 
paymen
t type* 
Other 
payment 
payer* 
Other 
payment 
receiver* 
Other 
payment 
currency 
Other 
paymen
t 
amount 
Other 
paymen
t date* 
Other 
paymen
t type 
Other 
payment 
payer 
Other 
payment 
receiver 
Other 
payment 
currency 
Other 
payment 
amount 
Other 
payment 
date 
1
1 
CORR UFRO LEI456 LEI123 USD 0 
2023-
03-20 
UFRO; 
URFO; 
PEXH; 
PEXH; 
UWIN; 
UFRO 
LEI123; 
LEI123; 
LEI123; 
LEI456; 
LEI456; 
LEI456 
LEI456; 
LEI456; 
LEI456; 
LEI123; 
LEI123; 
LEI123 
USD; 
USD; 
USD; 
GBP; 
USD; 
USD 
100; 
300; 
400; 
320; 
100; 
0 
2023-02-
20; 
2023-03-
20; 
2023-04-
20; 
2023-05-
20; 
2023-04-
18; 
2023-03-
20 
Action Type 
=CORR を使って過
去の 3 月 20 日時
点の payment 内
容は報告すべきでは
なかったた
め、、’UFRO’部分の
other payment 
amount をゼロ '0'
として提出している。 
*Other Payment 項目の独自性を判断する鍵となる組み合わせは Other Payment Type, Other payment date, Other payment payer, Other 
payment receiver である。 
 

---

## Page 47

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 47  
 
FC 3.15: スケジュール項目 
金融庁報告制度改正においてスケジュールを示す６項目は下記のとおり。  
  
1. Price schedule  
2. Strike price schedule  
3. Notional amount schedule - Leg 1  
4. Notional amount schedule - Leg 2  
5. Notional quantity schedule - Leg 1  
6. Notional quantity schedule - Leg 2  
  
これらのスケジュール項目にはそれぞれ 3 つ関連する項目が存在する。すなわち、Effective Date と End Date および、2
つの項目の示す期間の値である。  
CSV で提供するレポートの観点からは、XML ファイルで提出されたスケジュールの値をプライマリー値として適用し、関連する金
融庁向け報告項目を更新する。下記の表でそれら使用される項目を示している。  
 
スケジュール項目  金融庁向け報告項目  適用するスケジュールの値  CSV ファイルのレポートに表示するロジック  
Price schedule  
Price  
報告された値もしくは適用するスケ
ジュール項目から生成した値  
1.[複数のプライススケジュールー調整前プライススケジュ
ール契約効力発生日と調整前契約終了日の間に適用
されるプライス群] が入力されていたら、プライススケジュ
ールから効力発生日と終了日の期間中に設定された値
を報告する。 
2. 終了日がない場合は、price in the schedule 項
目の契約効力発生日の値を報告し続ける。 
3. 継続的に異なるスケジュール日がない場合は、次のス
ケジュールの効力発生日までの Price 項目の値を報告
する。(値が空白 blank の場合は、blank を報告) 
プライススケジュール -契約効力発生日（調整
前）と 契約終了日（調整前）間に適用される
プライス  
スケジュールの値  
Schedule 項目: 提出された値を表示  
プライススケジュール -契約効力発生日（調整
前）  
スケジュールの効力発生日  
プライススケジュール -契約終了日（調整前）  スケジュールの契約終了日  
Strike price 
schedule  
行使価格  
報告された値もしくは適用するスケ
ジュール項目から生成した値  
1.[行使価格スケジュールー契約効力発生日（調整
前）と契約終了日（調整前）間に適用される行使価
格］が入力されていたら、スケジュールの契約効力発生
日の行使価格の値を報告する。 
2. 終了日がない場合は、行使価格の契約効力発生
日の値を報告し続ける。 
3. 継続的に異なるスケジュール日がない場合は、次のス
ケジュールまで行使価格項目の値を報告する。 
行使価格スケジュール- 契約効力発生日（調
整前）と契約終了日（調整前）間に適用され
る行使価格  
スケジュールの値  Schedule 項目: 提出された値を表示  

---

## Page 48

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 48  
 
行使価格スケジュール -契約効力発生日（調
整前）  
スケジュールの効力発生日  
行使価格スケジュール -契約終了日（調整
前）  
スケジュールの契約終了日  
Notional 
amount 
schedule - Leg 
1  
leg 1 の想定元本  
報告された値もしくは適用するスケ
ジュール項目から生成した値  
1. [想定元本スケジュール - leg 1 の想定元本スケジ
ュールの契約効力発生日の想定元本] が入力されてい
たら、効力発生日から終了日までの Leg1 スケジュール
の現在の想定元本を報告する。 
2. 終了日がない場合は、効力発生日以降のLeg1 の
想定元本の値の報告を継続する。 
3. 値の異なるスケジュール群の日付がない場合は、
Notional amount of leg 1 項目の値を次のスケジュ
ールの効力発生日まで報告する。  
想定元本スケジュール – 契約効力発生日（調
整前）の Leg1 想定元本  
スケジュールの値  
Schedule 項目: 提出された値を表示  
想定元本スケジュール – 契約効力発生日の
（調整前）Leg1 
スケジュールの効力発生日   
想定元本スケジュール – 契約終了日の（調整
前）Leg1  
スケジュールの契約終了日  
Notional 
amount 
schedule - Leg 
2  
Leg 2 の想定元本  
報告された値もしくは適用するスケ
ジュール項目から生成した値  
1. [想定元本スケジュール - leg 2 の想定元本スケジ
ュールの契約効力発生日の想定元本] が入力されてい
たら、効力発生日から終了日までの Leg2 スケジュール
の現在の想定元本を報告する。 
2. 終了日がない場合は、効力発生日以降のLeg２の
想定元本の値の報告を継続する。 
3. 異なるスケジュール群の日付がない場合は、
Notional amount of leg ２項目の値を次のスケジュ
ールの効力発生日まで報告する。 
 (値が空白 blank の場合は、blank を報告) 
想定元本スケジュール – 契約効力発生日（調
整前）の Leg２想定元本  
スケジュールの値  
Schedule 項目: 提出された値を表示.  
想定元本スケジュール – 契約効力発生日（調
整前）Leg2 
スケジュールの効力発生日   
想定元本スケジュール – 契約終了日（調整
前）Leg2  
スケジュールの契約終了日  
Notional 
quantity 
schedule - Leg 
1  
CDE-想定元本の総量 Leg 1  
報告された値もしくは適用するスケ
ジュール項目から生成した値  
1. [想定元本の総量 leg 1-スケジュールの効力発生
日に設定された leg1 の想定元本の総量スケジュール ] 
が入力されていたら、指示されている効力発生日から終
了日の現在の期間の想定元本の総量を報告する。  
2. 期間の終了日が指定されていない場合は、効力発
生日以降の想定元本の総量 leg 1-の値の報告を継
続する。 
3. 異なるスケジュールの日付がない場合は、次のスケジ
ュール期間の効力発生日まで想定元本の総量 leg 1
の値を報告する。(値が空白 blank の場合は、blank
を報告)  
想定元本総量スケジュール 契約効力発生日
（調整前）の想定元本の総量 Leg1  
スケジュールの値  Schedule 項目: 提出された値を表示  

---

## Page 49

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 49  
 
想定元本総量スケジュール 契約効力発生日
（調整前）Leg1  
スケジュールの効力発生日   
想定元本総量スケジュール 契約終了日（調
整前）Leg1  
スケジュールの契約終了日  
Notional 
quantity 
schedule - Leg 
2  
CDE-想定元本の総量 leg 2  
報告された値もしくは適用するスケ
ジュール項目から生成した値  
1. [想定元本の総量 leg 2-スケジュールの効力発生
日に設定された leg2 の想定元本の総量スケジュール ] 
が入力されていたら、指示されている効力発生日から終
了日の現在の期間の想定元本の総量を報告する。  
2. 期間の終了日が指定されていない場合は、効力発
生日以降の想定元本の総量 leg 2-の値の報告を継
続する。 
3. 異なるスケジュールの日付がない場合は、次のスケジ
ュール期間の効力発生日まで想定元本の総量 leg 2
の値を報告する。(値が空白 blank の場合は、blank
を報告)   
想定元本総量スケジュール 契約効力発生日
（調整前）の想定元本の総量 Leg2  
スケジュールの値  
Schedule 項目: 提出された値を表示  想定元本総量スケジュール 契約効力発生日
（調整前） Leg2  
スケジュールの効力発生日   
想定元本総量スケジュール 契約終了日（調
整前） Leg2  
スケジュールの契約終了日  
 
スケジュール項目には複数の値を入力することができ、各項目間の値に論理的矛盾がないかどうかの検証を行う。下記のルール
に沿わない場合は受領不可となる。  
1. 提出された各項目のスケジュールの数と効力発生日に整合性がない場合は、受領不可となる。 
例）[プライススケジュール群 - 契約効力発生日（調整前）と 契約終了日（調整前）間に適用されるプライス] 
の数と[プライススケジュール群 - 契約発効日（調整前）]の数が一致しない  
2. 各スケジュールの契約終了日はオプショナル扱いだが、値が入力されている場合は、値の数と契約効力発生
日、契約終了日の数が一致しない場合は、受領不可とする。  
3. 契約効力発生日の報告は時系列的に正しい順番で提出する必要がある。  
4. 契約効力発生日は前回のペイメントスケジュールの終了日よりも前の日付になることはできない。  
5. 契約終了日の報告は時系列的に正しい順番で提出する必要がある。  
 
下記に、値が受領される場合と受領不可になる場合の例を挙げているので参照のこと。  
Case 1  
  
XML ブロ
ック  
項目  値  想定される応答結果  
1  Unadjusted effective date of the price  2023-09-01  
受領される  
Unadjusted end date of the price  2023-09-30  
Price in effect between the unadjusted effective and end 
date  9000  
2  Unadjusted effective date of the price  2023-10-01  
Unadjusted end date of the price  2023-10-31  

---

## Page 50

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 50  
 
Price in effect between the unadjusted effective and end 
date  8000  
3  Unadjusted effective date of the price  2023-11-01  
Unadjusted end date of the price  2023-11-30  
Price in effect between the unadjusted effective and end 
date  7000  
  
 Case 2          
XML ブロ
ック  
項目  値  想定される応答結果  
1  Unadjusted effective date of the price  2023-11-01  
受領不可 – XML ブロックが時系列順に並ん
でいないため。  
Unadjusted end date of the price  2023-11-30  
Price in effect between the unadjusted effective and end 
date  9000  
2  Unadjusted effective date of the price  2023-09-01  
Unadjusted end date of the price  2023-09-30  
Price in effect between the unadjusted effective and end 
date  8000  
3  Unadjusted effective date of the price  2023-10-01  
Unadjusted end date of the price  2023-10-31  
Price in effect between the unadjusted effective and end 
date  7000  
   
Case 3           
XML ブロ
ック  
項目  値  想定される応答結果  
1  Unadjusted effective date of the price  2023-09-01  
受領不可 – Block 2 の発効日が'Block 1'
の終了日と重なっているため。  
Unadjusted end date of the price  2023-09-30  
Price in effect between the unadjusted effective and end 
date  9000  
2  Unadjusted effective date of the price  2023-09-30  
Unadjusted end date of the price  2023-10-31  
Price in effect between the unadjusted effective and end 
date  8000  
3  Unadjusted effective date of the price  2023-11-01  
Unadjusted end date of the price  2023-11-30  
Price in effect between the unadjusted effective and end 
date  7000  
 
 Case 4     
XML ブロッ
ク  
項目  値  想定される応答結果  
1  Unadjusted effective date of the price  2023-09-01  
受領される – 終了日はブランクでも可  
Unadjusted end date of the price  Blank  
Price in effect between the unadjusted effective and end 
date  9000  

---

## Page 51

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 51  
 
2  Unadjusted effective date of the price  2023-10-01  
Unadjusted end date of the price  Blank  
Price in effect between the unadjusted effective and end 
date  8000  
3  Unadjusted effective date of the price  2023-11-01  
Unadjusted end date of the price  Blank  
Price in effect between the unadjusted effective and end 
date  7000  
   
Case 5         
XML ブロッ
ク  
項目  値  想定される応答結果  
1  Unadjusted effective date of the price  2023-11-01  
受領不可 - XML ブロックが時系列順に並ん
でいないため。 
Unadjusted end date of the price  Blank  
Price in effect between the unadjusted effective and end 
date  9000  
2  Unadjusted effective date of the price  2023-09-01  
Unadjusted end date of the price  Blank  
Price in effect between the unadjusted effective and end 
date  8000  
3  Unadjusted effective date of the price  2023-10-01  
Unadjusted end date of the price  Blank  
Price in effect between the unadjusted effective and end 
date  7000  
 
例えばレポート日付が 2023-10-16 の場合、TSR の CSV ファイルレポートは Case1 と Case4 下記の値で作成される。 
取引識別
子 UTI 
報告当
事者
RCP 
取引相手
OCP 
価格 
Price in effect 
between the 
unadjusted effective 
date and end date  
(Price schedule) 
Unadjusted 
effective date of 
the price (Price 
schedule) 
Unadjusted end date of 
the price  
(Price schedule) 
UTI1 LEI1 LEI2 8000 9000;8000;7000 
2023-09-01;2023-
10-01; 
2023-11-01 
2023-09-30;2023-10-31; 
2023-11-30 
 
注釈: XML スキーマ構成上、関連する“notation”や “currency” タグはスケジュール XML ブロックの中に含める必要があ
る。しかしながら、これらの値は別途報告が必要な notation や currency 項目の値から抽出することはない。 
たとえば、Price Notation 項目とスケジュール項目ブロック内の Price Notation タグに値を入れて報告する場合には、Price 
Notation 項目で報告された値のみを表示する。スケジュール項目ブロック内の値は表示されない。 

---

## Page 52

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 52  
 
このルールは以下に挙げる、その他のスケジュール項目のブロックにも全て適用される。 Price schedule, Strike price 
schedule, Notional amount schedule - Leg 1, Notional amount schedule - Leg 2, Notional quantity 
schedule - Leg 1 and Notional quantity schedule - Leg 2. 
FC 3.16: イベントタイムスタンプとレポーティングタイムスタンプ 
金融庁向け報告の制度改正ではタイムスタンプ項目における時系列の合理性に対する検証を導入する。具体的には、全ての
取引情報提出ファイルにおいて、日付け・時間が早い順（同時も可）が以下の通りとなる必要がある。 
Execution Timestamp ≦ Event Timestamp ≦ Reporting Timestamp ≦ Message Received 
Timestamp ≦ Message Processed Timestamp 
最初の 3 つの項目については、ユーザーが提出すべき値であるが、Message Received Timestamp と Message 
Processed Timestamp は GTR が付記する値である。 
FC5.1 に記載のとおり Trade State Report に反映するポジションを決定するために、タイムスタンプ項目を使って上記のウォ
ーターフォールの順位通りに判断する。

---

## Page 53

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 53  
 
ポジションが TSR に正しく反映されているかどうかの決定にはタイムスタンプ項目を基準にする。データの取り込みの際のルールと使用事例は以下を参照のこと。  
Data 
Element 
Name 
データ項目名 
Description of Data 
Element 
データ項目の定義 
Business Rules when 
[Action Type] = 
NEWT, MODI, CORR, 
REVI 
4/1/2024 以降 
Business Rules when 
[Action Type] = 
PRTO, EROR 
4/1/2024 以降 
Business Rules when 
[Action Type] = TERM 
4/1/2024 以降 
[[collateral]] 
Business Rules 
[Action Type] = 
MARU 
4/1/2024 以降 
Valuation Business 
Rules 
[Action Type] = 
VALU 
4/1/2024 以降 
Reporting 
timestamp 
報告タイムスタ
ンプ 
取引情報蓄積機関への報
告の提出日時 
(a)報告タイムスタンプは執行
タイムスタンプと同時か遅い時
間でなければならない。(b)報
告タイムスタンプは TR による
Message Received 
timestamp と同時か早い時
間でなければならない。
(c)Message Received 
timestamp は、Reporting 
Timestamp から 2 日以内
でなければならない。 
(a)報告タイムスタンプは執行
タイムスタンプと同時か遅い時
間でなければならない。(b)報
告タイムスタンプは TR による
Message Received 
timestamp と同時か早い時
間でなければならない。 
(c)Message Received 
timestamp は、Reporting 
Timestamp から 2 日以内
でなければならない。 
(a)報告タイムスタンプは執行
タイムスタンプと同時か遅い時
間でなければならない。(b)報
告タイムスタンプは TR による
Message Received 
timestamp と同時か早い時
間でなければならない。 
(c)Message Received 
timestamp は、Reporting 
Timestamp から 2 日以内
でなければならない。 
(a)報告タイムスタンプは
TR による Message 
Received 
timestamp と同時か
早い時間でなければなら
ない。 
(b)Message 
Received 
timestamp は、
Reporting 
Timestamp から 2 日
以内でなければならな
い。 
(a)報告タイムスタンプは
TR による Message 
Received timestamp と
同時か早い時間でなけれ
ばならない。 
(b)Message Received 
timestamp は、
Reporting Timestamp
から 2 日以内でなければな
らない。 
(c)報告タイムスタンプは
Valuation timestamp
と同時か遅い時間でなけれ
ばならない。 

---

## Page 54

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 54  
 
Event 
timestamp 
イベントタイム
スタンプ 
報告主体の取引当事者又
はサービスプロバイダーによっ
て決定されたイベントの発生
日時。清算取引の場合、元
取引がデリバティブ清算機関
により債務引受が行われ、清
算機関のシステムによって記
録された日時をこのデータ項
目に記載する。 
(a)アクションタイプが NEWT, 
MODI, CORR の場合、イベ
ントタイムスタンプは執行タイム
スタンプと同時か遅い時間で
なければならない。 
(b)アクションタイプが
NEWT,MODI,CORR の場
合、イベントタイムスタンプは報
告タイムスタンプと同時か早い
時間でなければならない。 
(c)アクションタイプが REVI の
場合、イベントタイムスタンプは
報告タイムスタンプと同時でな
ければならない。 
(d)アクションタイプが NEWT, 
MODI, CORR の場合、イベ
ントタイムスタンプの値は
[Expiration date] および 
[Early termination date] 
と同じか早い時間でなければ
ならない。 
(a)イベントタイムスタンプは執
行タイムスタンプと同時か遅い
時間でなければならない。 
(b)イベントタイムスタンプの日
付は報告タイムスタンプと同じ
でなければならない。 
(c)イベントタイムスタンプの日
付は、[Expiration Date]お
よび[Early termination 
date]と同じか早い日付でな
ければならない。 
(a)イベントタイムスタンプは執
行タイムスタンプと同時か遅い
時間でなければならない。 
(b)イベントタイムスタンプは報
告タイムスタンプと同時か早い
時間でなければならない。 
(c)イベントタイムスタンプの日
付は[Expiration Date]と
同じか早い日付でなければな
らない。 
(d)イベントタイムスタンプの日
付は [Early termination 
date] と同じでなければなら
ない。 
(a)イベントタイムスタンプ
の日付は報告タイムスタ
ンプと同時か早い日付で
なければならない。 
[N/A] 
 
 
 
 
 
 

---

## Page 55

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 55  
 
TRADE STATE REPORT におけるタイムスタンプ使用事例 
 
最新のイベントタイムスタンプよりも過去の取引情報についての内容を変更するため等にこれらを提出した場合では、当該 UTI 取引の TSR 上の最新
情報を示す記録は上書きされない。 取引情報蓄積機関としては過去データの修正内容から最新の状態を示すTSR で何を修正すべきかの判断は行わ
ない。 つまり過去のイベントに関する訂正等の提出は最新のイベントタイムスタンプの内容に影響を与えることはないので、ユーザー自身が、必要に応じ
て、現時点での最新情報が TSR に適切に示されているかを確認する必要があることに注意。 
  


---

## Page 56

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 56  
 
VALUATION TIMESTAMP における使用事例 
 
時価情報は Valuation Timestamp 項目の情報に基づいて TSR に統合される。最新情報と判断する順位として、Reporting Timestamp, Message Received 
Timestamp の順となる。そのため過去日付の時価情報を提出しても、直近の時価情報を上書きすることはしない。 時価情報を TSR に統合する際は、時価情報関連の
項目のみを反映させる。金融庁報告における時価情報関連の項目は以下のとおり。  Valuation amount, Valuation currency, Valuation timestamp, 
Valuation method および Delta である。TSR に掲載する Reporting Timestamp と Valuation Timestamp 以外のタイムスタンプ項目の内容はその対象となる
取引情報の提出内容から適用されるので、VALU で提出したファイルのタイムスタンプの内容は統合されない。(つまり 時価情報の報告ファイルから統合されるタイムスタンプ
関連の項目は、Valuation Timestamp と Reporting Timestamp のみであり、その他は対象外。) 
 
 
 
 


---

## Page 57

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 57  
 
 
[[Margin]] EVENT TIMESTAMP における使用事例 
 
マージンステートレポート（MSR)はイベントタイムスタンプに基づいて、最新の状態を掲載する。最新情報を判断する際の順位として Reporting Timestamp、Message 
Received Timestamp、Message Processed Timestamp の順となる。レポート作成時のオープンポジションに対して、取引レベル・ポートフォリオレベルの担保に関わら
ず適用するルールである。 


---

## Page 58

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 58  
 
FC 4: 応答メッセージ 
FC 4.1 応答メッセージ様式 
応答メッセージ様式が、現行の FpML や CSV から、GTR への提出ファイル形式に合わせて ISO20022 準拠の XML に変更
される。応答ファイルのフォーマットは zip で圧縮された形式となり、zip ファイルの中に xml ファイルが格納される。具体的なファ
イル名は下記を参照のこと。 
レポートの種類 フォーマット 現状のファイル名 
JFSA GTR Batch 
ACK/NACK 
Report XML 
ISO20022XML 
SFTP File Name:（圧縮ファイル名 2 種類） 
sFTP_BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_YYYY-MM-
DD.HH_MM_SS.zip または、 
sFTP_BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_YYYY-MM-
DD.HH_MM_SS.gz 
 
 sFTP File Name within the zip file: （圧縮ファイル内のファイル名） 
sFTP_BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_2023-10-
20.01_10_06.xml   
  
Portal:（ポータルの場合の圧縮ファイル名） 
BizMsgIdr_JFSA_ACKNACK_Report_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.zip 
 
Portal File Name within the compressed file:（ポータルの圧縮ファイル内のファイル名）  
WEB-US-BatchInfoID.xml （ポータルでアップロードした場合）または 
SFP-US-BatchInfoID.xml （sFTP 経由で提出した場合） 
注釈：ユーザーは圧縮方式を gz または zip のどちらか選択が可能。GZIP(.gz)は UNIX ベースのシステ
ム、WINZIP(.zip)は Windows ベースのシステム 
 
(a) BizMsgIdr は利用者が付記する 35 文字の識別子であり、XML の提出ファイルのヘッダー部分を示す。このストリングは
原則、特殊文字を受け付けない。受け付けることができるのは英数字文字列(0-9a-zA-Z)および アンダースコア (_), ハイフ
ン (-) ドット (.)の３特殊文字だけである。 
(b) BatchInfoID は、GTR が生成する [[ID]] であり、ファイルを区別する際の識別子となる。 
(c) 6XXX は、利用者が取引情報を提出する際に使用する各社に固有に付与されている O-code を示す 
(d) YYYY-MM-DD.HH_MM_SS は、応答ファイルが生成された UTC ベースの日時を示すタイムスタンプを示す。 
** 注）: 現行の応答ファイル（BDR）のファイル名は本番稼働後までは当面そのままで継続させることになる。しかし、システ
ム的な制限のため、BizMsgIdr の文字数が 35 文字を超えると GTR システムの受け入れ上限の 96 文字を超えてしまい、フ
ァイル名が切り捨てられ応答ファイルが作成できなくなってしまうことに注意。今後行われるファイル名の変更作業を完了するまで
の期間は BizMsgIdr の文字数は 25 文字以内にすること。  

---

## Page 59

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 59  
 
BizMsgIdr の文字制限 35 文字を可能にするための変更作業後のファイル名は以下のとおりになる予定:  
 
レポートの種類 フォーマット 変更作業後のファイル名 
JFSA GTR 
Batch 
ACK/NACK 
Report XML  
ISO20022XML  
SFTP File Name:  
sFTP_BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip or 
sFTP_BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.gz  
sFTP File Name within the compressed file:  
sFTP_BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_2023-10-20.01_10_06.xml   
Portal:  
BizMsgIdr_JFSA_BDR_BatchInfoID_6XXX_YYYY-MM-DD.HH_MM_SS.xml.zip  
  
Portal File Name within the compressed file:  
WEB-US-BatchInfoID.xml or SFP-US-BatchInfoID.xml  
  
Note: Clients may configure the compression method to .gz or .zip. GZIP (.gz) is for UNIX 
based systems and WINZIP (.ZIP) is for Windows based systems.  
 
4 月 1 日の改正制度施行後に、ファイル名を変更するのは 2024 年第 3 四半期末を予定。（9 月 28 日の検証ルールを
厳格化するタイミングと同時期に実施する予定）“JFSA_ACKNACK_Report” の名称を “BDR”に短縮し、sFTP ファイル
名の.zip および.gz の前に.xml の拡張子が挿入される。  
  
ISO 20022 準拠の XML ファイルテンプレートでは応答メッセージ (ACK /NACK) の検証が 2 段階レベルで行われる。  
  
1. メッセージ / ファイル形式レベル   
2. 提出内容レベル   
  
下記の応答メッセージの XML メッセージスキーマ (auth.031.001.01)に 2 段階レベルの ACK / NACK の検証が記載され
ている。   
  
•青いセクションの<MsgSts>タグ内に、メッセージ/ ファイルレベルの検証をかける要素が表示されている。提出されたメッセージ
/ファイルごとに受領可否の ACK / NACK の応答を返す。 <MsgSts>の値は ACK/NACK のいずれかの値となる。   
o <Sts>CRPT</Sts> = CRPT (Corrupt) は、メッセージ/ファイル自体がリジェクトされ受領不可となったことを示す。
[[DTCC]] 側でファイルを開いてないので、ポジション情報の内容は見ていない。   
o <Sts>ACPT</Sts> = ACPT (ACK) は、メッセージ/ファイル自体は正しく読み込むことができ GTR で受領したことを示
す。   
  
• 赤いセクションの<RcrdSts>タグ内に、提出ファイルの内容レベルでの検証をかけるエレメントが表示されている。提出ファイル
内に 100 件の取引情報が含まれている場合は 100 件の 受領可否 ACK / NACK 応答が含まれる。 <MsgSts>タグ内は
下記の 2 つの値のいずれかが表示される。   
o <Sts>RJCT</Sts> = RJCT (NACK)は、取引情報は受領不可となったことを意味する。   
o <Sts>ACPT</Sts> = ACPT (ACK) は取引情報は受領されたことを意味する。   

---

## Page 60

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 60  
 
 
ビジネスメッセージヘッダーID (BizMsgIdr タグ 下記に表示) は各ファイルのアプリケーションヘッダーもしくはGTR に対し
て送信するメッセージに含める必要がある。その際には、ビジネスアプリケーションヘッダー(BAH)のバージョン 01 もしくは 02 を
使うことが求められる。 


---

## Page 61

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 61  
 
 
GTR から生成される受領可否 ACK / NACK の応答メッセージ (auth.031.001.01) は、利用者から提出されたファイル/
メッセージと同じ BizMsgIdr を使用する。下図の赤で囲んだ MsgRptIdr タグを参照のこと。  
 


---

## Page 62

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 62  
 
各提出ファイルに対する受領可否を示す ACK / NACK 応答メッセージはテクニカルレコード [[ID]]（Technical Record [[ID]]）
を基にして識別する。 各提出ファイル/メッセージの取引記録には下記でハイライトしたとおり XML メッセージのボディにテクニカル
レコード [[ID]] (TRI)を含めることができる仕様になっている。この識別子に独自性を持たせることで、応答メッセージを受領した際
に、どの取引情報についての検証結果の応答なのか突合することができる。このテクニカルレコード [[ID]] は必須項目となるの
で、取引情報提出の際には、取引記録に対して必ず独自の値を付与して突合ができるようにすること 。なおこの項目には
UTI と同じ値を使うことが可能である。その場合の欠点は、同一ファイル内に同一 UTI の取引記録を複数含めた場合に識別
ができなくなることである。  
このテクニカルレコード [[ID]] (TRI) は受領可否(ACK/NACK)を示す応答ファイル上では auth.031.001.01 スキーマを使って
Original Record [[ID]] (ORI) として表示される。 
 


---

## Page 63

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 63  
 
 
 
 
XML での応答メッセージのレイアウトを示すサンプルファイルは、ラーニングセンターに掲載される予定。 
応答メッセージサンプル (TBD) 
FC 4.2 応答メッセージの書式および チャネル  
制度改正実施に応じて、応答メッセージの様式やチャネルが以下の通り変更される予定。 


---

## Page 64

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 64  
 
 
送信チャネル 
送信 
フォーマット 
応答 
フォーマット 
応答 
ファイル 
応答電文受信者 
応答チャネル 
MQ 
ISO XML 
message 
ISO XML 
ISO XML 
message 
Data Submitter 
MQ 
Web Upload 
(a)sFTP 使用無し 
(b)sFTP 使用あり 
ISO XML files ISO XML ISO XML files Data Submitter 
(a)ポータル 
(b)ポータルおよび
sFTP 
SFTP ISO XML files ISO XML ISO XML files Data Submitter sFTP およびポータル 
FC 4.3 MQ 応答は Replyto キューに返信 
利用者の利便性向上のために、新たに ACK/NACK の応答メッセージを GTR がどこに返信するかを指定することができる機能
を搭載することになった。利用者からの要望にに応える形ですでに北米報告では実装されている。  
この機能は利用者が Reply To キューマネージャーを利用してどこに応答メッセージを受領したいか指定することができ、MQ メッ
セージのヘッダーにキューの名称の詳細を入力することによって、指示した場所に応答メッセージが返る仕組みである。  
 
FC 5: レポート 
日次に作成する各種レポートは、[[DTCC]] ポータルを通じて提供され、閲覧・ダウンロード可能となる。ポータルサイトの機能の詳
細は、ラーニングセンターで確認できる。現行提供している各種のレポート（ROR を含む）はすべて廃止し、制度改正実施後
は以下の新しいレポートを提供する。レポートを作成するための時間内に取引情報の提出がない場合には、レポートは作成され
ない。ブランクレポートは提供されないことに注意。 
FC 5.1: レポートの種類 
以下のレポートが日次で作成される。レポートのレイアウトや詳細はラーニングセンターに掲載されている。 
種類 内容 
JFSA [[EOD]] 
Trade State 
Report 
(TSR)  
• トレード・ステート・レポート（TSR）には取引相手（OCP）が送信した取引情報（アレッジ記録）は掲載し
ない。  

---

## Page 65

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 65  
 
種類 内容 
• TSR には、独自性のある取引のみが表示される。取引の独自性は、UTI + RCP1 により判定される。例え
ば、ポジション 1 が UTI + RCP1 + OCP1 で、 ポジション 2 が UTI + RCP2 と OCP1 である場合、それ
らはそれぞれが独自性のあるポジションと見なされる。また、RCP と ERR が同一であるポジションの場合、RCP と
ERR の両方が TSR にアクセスできるが、当該ポジションは TSR に 1 件だけ表示される。 
• TSR を作成する際、適切なアクションタイプ（EXIT）の報告によって早期解約となったポジション、もしくは満期
日到来となったポジションはその日の TSR から除外される。 
• TSR にはポジションの最新情報を表示するが、時価情報と担保情報のメッセージは含まない。しかし時価情報
の報告後、その内容はポジションデータに統合される。TSR には、各取引情報のイベントタイムスタンプ (event 
timestamp) に基づいた、最新のポジションの情報が表示される。例えば、過去のイベントタイムスタンプを使っ
て過去の報告内容の訂正を提出した場合、直近のイベントタイムスタンプのポジション情報を上書きすることはな
い。 
• TSR は、毎週火曜日から土曜日の日本時間午前 0 時以降に日次で作成される。 
• TSR はポータル上で 12 か月間閲覧・ダウンロードが可能 
• TSR にアクセスができるのは、取引当事者（RCP）および報告責義務者（ERR）に限定される。 
• TSR には、GTR で受領されたメッセージのみを含み、受領不可となった分は掲載されない。 
• TSR の各ポジションは、提出された情報のみを含むものとする。利用者が任意項目の値を提出してこなかった場
合、TSR の当該項目は空欄となる。 
• 取引当事者（RCP）と報告義務者（ERR）のみが TSR にアクセス可能なため、金融庁報告ではすべての
項目についてマスキングは行わない。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる。 
• TSR は、アセットクラスごと、法域ごとに作成される。 
• アクションタイプ TERM または EROR で提出された取引、またはアクションタイプ PRTO で提出された取引は満
期日が将来の日付であっても TSR には掲載されない。 
JFSA [[EOD]] 
Trade Activity 
Report (TAR) 
• トレード・アクティビティ・レポート（TAR）は、GTR で受領されたメッセージのみを含み、受領不可となった分は
掲載されない。 
• TAR は、日次で作成され日々のカットオフ時刻（日本時間 23:59:59）の間に提出された取引情報が掲載
される。例えば、日本時間水曜日の朝に作成される TAR には、日本時間火曜日 00:00:00 から火曜日 
23:59:59 までの間に送信された取引メッセージが含まれる。TAR が複数日分を含む唯一の例外は、火曜日
の朝に生成されるもので、土曜日の 00:00:00 JST から月曜日の 23:59:59 JST の間に送信された取引
メッセージが含まれる。タイムスタンプ（刻印時刻）としては、利用者が送信した時刻である送信タイムスタンプと

---

## Page 66

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 66  
 
種類 内容 
する。したがって、同一の取引識別子を持つ取引メッセージを、複数回正常に送信し GTR に受領された場合、
この取引は TAR 上複数回表示される。 
• TAR には、提出された情報のみを含むものとする。利用者が任意項目の値を提出してこなかった場合、TAR の
当該項目は空欄となる。 
• TAR には取引メッセージまたは時価情報のみを含み、別に作成されるレポートに記載されることになる担保情報
は掲載されない。 
• TAR には取引相手（TP2）が送信した取引情報（アレッジ記録）は掲載しない。  
• TAR は、毎週火曜日から土曜日の日本時間午前 0 時以降に日次で作成される。 
• TAR はポータル上で 12 か月間閲覧・ダウンロードが可能。 
• TAR にアクセスができるのは、取引当事者（RCP）および報告義務者（ERR）に限定される。 
• TAR ではすべての項目に対してマスキングは行わない。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる。 
• TAR は、アセットクラスごと、法域ごとに作成される。 
JFSA [[EOD]] 
Submission 
Report 
• サブミッション・レポートには、受領可否に関わらず、取引情報提出主体（RSE）が提出したの全ての提出情報
が含まれる。すなわち、送信された取引メッセージにそれぞれ受領済もしくは受領不可を表示する。 
• 取引情報の提出期限時刻は月曜日から金曜日の日本時間 23:59:59 である。つまり、GTR での受領タイム
スタンプが日本時間 23:59:59 であれば、GTR での処理が翌日になったとしても、それらの取引情報は日のレ
ポートに掲載される。 
• サブミッション・レポートには、取引メッセージと時価情報が含まれるが、担保情報は含まれない。担保情報は、別
のレポートに反映される。 
• サブミッション・レポートは CSV フォーマットでのみ作成される。 
• サブミッション・レポートは毎週火曜日から土曜日の日本時間午前 0 時以降に日次で作成される。 
• レポートは 12 か月間閲覧・ダウンロードが可能。 
• サブミッションレポートにアクセスができるのは、取引情報提出主体（RSE）取引当事者（RCP）および報告
義務者（ERR）に限定される。取引情報提出主体（RSE）は、受領可否にかかわらず、提出したすべての
内容を見ることができるが、自身が提出していない取引情報の内容を見ることはできない。 
• 取引当事者（RCP）と報告義務者（ERR）が異なる場合は、自身を取引当事者 RCP または ERR、取引
相手を OCP として、自身の側の取引情報の受領可否の確認が可能。取引当事者(RCP)と報告義務者
（ERR）は、受領可否に関わらず、自身が提出したすべての提出内容を見ることができる。 

---

## Page 67

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 67  
 
種類 内容 
• サブミッション・レポートではすべての項目に対してマスキングは行わない。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる 
• レポートは、アセットクラスごと、法域ごとに作成される。 
JFSA [[EOD]] 
[[Margin]] State 
Report 
• マージン・ステート・レポートは毎週火曜日から土曜日の日本時間午前 0 時以降に日次で作成される。 
• レポートはポータル上で 12 か月間閲覧・ダウンロードが可能。 
• マージン・ステート・レポート（MSR）は取引レベルかポートフォリオレベルか問わずイベントタイムスタンプの情報に基
づきレポート作成時のオープンポジションについての最新の担保情報が反映される。 
• 取引レベルの担保情報の場合:  
(a) デリバティブ取引のポジション (RCP-OCP-UTI) が 2024 年 5 月 15 日当日に早期解約された場合、5 月
15 日付の MSR には当該ポジションは掲載されるが、5 月 16 日のレポートには掲載されない。 
(b) デリバティブ取引のポジション (RCP-OCP-UTI) が 2024 年 5 月 15 日に満期を迎えた場合、5 月 15 日
付の MSR には当該ポジションは掲載されるが、5 月 16 日のレポートには掲載されない。 
• ポートフォリオレベルの担保情報の場合:  
(a) IM/VM ポートフォリオコードの連結値を参照し、ポートフォリオの中にあるデリバティブ取引ポジションが 2024
年 5 月 15 日時点で 1 件(RCP-OCP-UTI) でもアウトスタンディングポジションとして存在している場合（そ
のポートフォリオに満期日(Expiration Date)が 2024 年 5 月 15 日のポジションが存在する場合も含まれ
る）、5 月 15 日付の MSR には当該担保ポートフォリオは掲載されるが、5 月 16 日のレポートには掲載さ
れない。この例は、2024 年 5 月 15 日より後の日付で紐づいている IM/VM 担保ポートフォリオが存在して
いない想定である。 
(b) IM/VM ポートフォリオコードの連結値を参照し、ポートフォリオの中にあるデリバティブ取引ポジションが 2024
年 5 月 15 日時点で(RCP-OCP-UTI) アウトスタンディングポジションとして全く存在していない場合
（2024 年 5 月 15 日に早期解約のポジションが存在する場合も含む）5 月 16 日付の MSR には当該
担保ポートフォリオ情報は掲載されない。 
• レポートにアクセスできるのは、 取引当事者（RCP）及び報告義務者（ERR)に限定される。 
• 本レポートは GTR で受領された担保情報のみを含み、受領不可となった分は表示されない。 
• レポート上の各ポジションは、提出された情報のみを含むものとする。利用者が任意項目の値を提出してこなかっ
た場合、レポート上当該項目は空欄となる。 
• マージン・ステート・レポートではすべての項目に対してマスキングは行わず、取引当事者（RCP）と報告義務者
（ERR）のみがアクセス可能。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる 

---

## Page 68

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 68  
 
種類 内容 
JFSA [[EOD]] 
[[Margin]] 
Activity 
Report 
• 担保情報アクティビティレポートは、GTR で受領された「MARU」アクションタイプのメッセージのみを含み、受領不
可の担保情報は含まれない。 
• レポートには、日次で作成され日々のカットオフ時刻（日本時間 23:59:59）までに提出された担保情報が
掲載される。例えば、日本時間水曜日の朝に作成される TAR には、日本時間火曜日 00:00:00 から火曜
日 23:59:59 までの間に送信された取引メッセージが含まれる。TAR が複数日分を含む唯一の例外は、火
曜日の朝に生成されるもので、土曜日の 00:00:00 JST から月曜日の 23:59:59 JST の間に送信された
取引メッセージが含まれる。タイムスタンプ（刻印時刻）としては、利用者が送信した時刻である送信タイムスタ
ンプとする。したがって、同一の取引識別子を持つ取引メッセージを、複数回正常に送信し GTR に受領された
場合、この取引は TAR 上複数回表示される。 
• レポート上の各ポジションは、提出された情報のみを含むものとする。利用者が任意項目の値を提出してこなかっ
た場合、レポート上当該項目は空欄となる。 
• レポートは担保情報メッセージの内容のみを表示する。 
• 取引相手（TP2）が送信した取引情報（アレッジ記録）は掲載しない。 
• レポートは毎週火曜日から土曜日の日本時間午前 0 時以降に日次で作成される。 
• レポートはポータル上で 12 か月間閲覧・ダウンロードが可能。 
• レポートにアクセスできるのは取引当事者（RCP） と報告義務者（ERR）に限定される。 
• レポートにおけるすべての項目に対してマスキングは行わない。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる。 
JFSA [[EOD]] 
[[Margin]] 
Submission 
Report 
• レポートには GTR での受領可否に関わらず、取引情報提出主体（RSE）が提出したすべての取引情報報告
分が含まれる。すなわち送信された担保情報メッセージにそれぞれ受領済もしくは受領不可を表示する。 
• 担保情報の提出期限時刻も月曜日から金曜日の日本時間 23:59:59 である。つまり、GTR での受領タイム
スタンプが日本時間 23:59:59 であれば、GTR での処理が翌日になったとしても、それらの担保情報は日のレ
ポートに掲載される。 
• レポートには、アクションタイプ MARU で提出された担保メッセージ内容のみが含む。 
• レポートは、CSV フォーマットでのみ作成される。 
• レポートは、毎週火曜日から土曜日の日本時間午前 0 時以降に日次で作成される。 
• レポートはポータル上で 12 か月間閲覧。 

---

## Page 69

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 69  
 
種類 内容 
• サブミッションレポートにアクセスができるのは、取引情報提出主体（RSE）取引当事者（RCP）および報告
義務者（ERR）に限定される。取引情報提出主体（RSE）は、受領可否にかかわらず、提出したすべての
内容を見ることができるが、自身が提出していない取引情報の内容を見ることはできない。 
• 取引当事者（RCP）と報告義務者（ERR）が異なる場合は、自身を取引当事者 RCP または ERR、取引
相手を OCP として、自身の側の取引情報の受領可否の確認が可能。取引当事者(RCP)と報告義務者
（ERR）は、受領可否に関わらず、自身が提出したすべての提出内容を見ることができる。 
• レポートにおけるすべての項目に対してマスキングは行わない。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる。 
JFSA [[EOD]] 
Allege Trade 
State Report 
• エンドオブデイ([[EOD]])トレード・アレッジ・レポートは取引相手が提出した取引情報を反映したレポートであり、
CSV 形式で提供する。 
• このレポートは TSR を基に作成され、[[EOD]] ベースでの取引相手側が提出した取引情報をまとめたものである。 
• 取引相手が GTR 利用者である場合にのみ、このレポートで取引相手が提出した内容を確認することができる。 
• 独自性が確認された取引情報のみがアレッジレポート掲載の対象となる。取引の独自性判断の定義は UTI＋
OCP の組み合わせである。 
• レポート作成日に、当該ポジションが適切なアクションタイプの提出や早期解約の事由で削除された場合や、満
期日を迎えた場合は、アレッジレポートには掲載されない。 
• レポートは最新のポジションを反映するが、取引相手が提出した時価や担保情報は掲載されない。 
• レポートは毎週火曜日から土曜日の日本時間午前 0 時以降に日次で作成される。 
• レポートはポータル上で 12 か月間閲覧・ダウンロードが可能。 
• レポートにアクセスできるのは GTR を利用している取引相手（OCP）のみである。 
• レポートは GTR で受領されたメッセージのみを含み、受領不可となった分は掲載されない。 
• 各ポジションは、提出された情報のみを含むものとする。利用者が任意項目の値を提出してこなかった場合、
TSR の当該項目は空欄となる。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる予定。 
• レポートは、アセットクラスごと、法域ごとに作成される。 
JFSA Intraday 
Allege Activity 
Report  
• この新しいレポートは取引当事者同士が日中に取引情報の内容を共有することを容易にするために考案され
た。 
• レポートは監督当局からの規制もしくは指導によるものではない。GTR が自主的に作成するレポートである。 
• レポートは日中のウインドウ時間内に提出され GTR が受領した取引情報のみ掲載する。受領不可となったメッ
セージは含まない。 
• レポートはある特定日において、アクションタイプ NEWT, EROR, REVI で提出され、CP2 として自社を指定し
てきているメッセージで、GTR で受領されたメッセージファイルの内容だけを掲載する。（受領不可となった分は含
まれない。） 
• レポートは CSV のみで提供される。 

---

## Page 70

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 70  
 
種類 内容 
• レポートは日本時間の午前 10 時、18 時、午前０時の 3 回に分けて、月曜日から金曜日まで作成される。イ
ントラデイ・アレッジ・アクティビティレポートはレポート作成時点までに受領された報告内容を網羅して作成する。 
午前 10 時作成のレポートは午前 0 時から午前 9 時 59 分 59 秒までに受領された報告内容を反映。 
午後 6 時作成のレポートは午前 0 時から 17 時 59 分 59 秒までに受領された報告内容を反映する。 
• レポートはポータル上で制度改正発効日以降、ポータルで 12 か月間閲覧・ダウンロードが可能。 
• レポートにアクセスできるのは GTR を利用している取引相手（OCP）のみである。 
• 各ポジションは、提出された情報のみを含むものとする。利用者が任意項目の値を提出してこなかった場合、
TSR の当該項目は空欄となる。 
• レポートの確定版フォーマットはメッセージ・スペシフィケーションで確認できる。 
• レポートは、アセットクラスごとに作成され、[[DTCC]] の設定している O-code ごとに分類される。 
• レポートの詳細についてはラーニングセンターに掲載している。 
 
これらの新しいレポートを SFTP 接続で送信することを希望する場合、新しいプロダクト [[ID]] の設定を [[DTCC]] グループのコネクテ
ィビティチームに依頼して設定する必要がある。(GTRConnectivity@[[DTCC]].com)。接続完了には若干時間がかかる場合が
あるため、早めに連絡することを推奨する。 
FC 5.2: 時価情報をトレード・ステート・レポート（TSR）へ反映 
1) TSR への時価情報の統合：TSR に時価情報を反映させる際、時価情報に関連する項目のみを更新する必要が
ある。金融庁報告における時価情報関連の項目は、報告タイムスタンプ、時価評価額、評価通貨、評価タイムスタン
プ、 評価方法および Delta である。 
2) 時価情報関連の項目を TSR 上のポジションに連結させる際は、Valuation Timestamp の情報を適用する。 
3) TSR に表示するその他のタイムスタンプに関する項目は、引き続き取引情報メッセージの提出に関するものを適用す
る。（すなわち、時価情報メッセージの値で上書きすることはない）。 
4) 「最新」の時価評価額を統合するために使用するタイムスタンプ：TSR への統合に使用する時価情報は、最新の
評価タイムスタンプを適用する。 
5) 時価情報を TSR に統合するためには、その対象となる取引について、UTI（取引識別子）＋RCP（取引当事
者）＋OCP（取引相手）の組み合わせが一致 していなければならない。 

---

## Page 71

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 71  
 
FC 5.3: セルフサービスレポート管理機能 
金融庁およびその他の法域では利用者レポートのフォーマットについての規制はないため、GTR 利用者が取得するレポートのフ
ォーマットは XML、CSV もしくは両方欲しいという要望があると理解している。しかしながら、FC5.1 に記載のとおり、利用者レポ
ートのフォーマットは CSV に限定されることに注意。 
マネージサービス画面の中に新たなメニュータイルとしてレポートマネジメント機能が追加される。当該タイルを選択して、レポート
サービスの追加やカスタマイズが可能になる。初期設定で全てのレポートが CSV 形式になっている。レポートマネジメント機能は
種類ごとに集約されている。例えば Trade State Report について全般の設定が可能だが、アセットクラスごとに更に細分化し
た設定はできない。 
この機能は、利用者側でのシステム対応・開発等などは不要であり、一度設定すればその後は継続的に閲覧が可能となる。カ
スタマイズ作業を行えば、その後は選択したフォーマットでレポートが作成されることになる。ユーザーは選択した形式でのレポート
取得を停止することも可能である。現在の計画としては、UAT 環境と本番環境稼働前にこの機能の提供を開始する予定。そ
のため、事前に利用者側でマネージサービス機能の画面の設定をカスタマイズしておくことが可能になる。詳細については、ラーニ
ングセンターの Report Management Section を参照のこと。 
FC 5.4: レポートのファイル名フォーマット  
レポートの種類  フォーマット  ファイル名  
JFSA Trade 
Activity Report 
XML  
ISO20022XML  
sFTP  
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml  
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml  
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml  
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml  
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml  
  
Portal  
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml  
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml  
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml  
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml  
JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml  
JFSA Trade 
State Report 
XML  
ISO20022XML  
sFTP  
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml 
sFTP_JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml  
Portal  
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml  
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_5XXX.xml  
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_4XXX.xml  
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_3XXX.xml  
JFSA_EOD_Trade_State_Report_02503235-YYYY-MM-DD.HH_MM_SS_001001_2XXX.xml  
JFSA [[Margin]] 
Activity Report 
XML  
ISO20022XML  
sFTP  
sFTP_JFSA_EOD_Margin_Activity_Report_02503236-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml  
  
Portal  
JFSA_EOD_Margin_Activity_Report_02503236-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml  

---

## Page 72

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 72  
 
JFSA [[Margin]] 
State Report 
XML  
ISO20022XML  
sFTP  
sFTP_JFSA_EOD_Margin_State_Report_02503237-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml  
  
Portal  
JFSA_EOD_Margin_State_Report_02503237-YYYY-MM-DD.HH_MM_SS_001001_0XXX.xml  
JFSA Trade 
Activity Report 
CSV  
CSV equivalent  
sFTP  
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
  
Portal  
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
JFSA Trade 
State Report 
CSV  
CSV equivalent  
sFTP  
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
sFTP_JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
  
Portal  
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
JFSA_EOD_Trade_State_Report_02503239-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
JFSA [[Margin]] 
Activity Report 
CSV  
CSV equivalent  
sFTP  
sFTP_JFSA_EOD_Margin_Activity_Report_02503240-YYYY-MM-DD.HH_MM_SS_0XXX.csv  
  
Portal  
JFSA_EOD_Margin_Activity_Report_02503240-YYYY-MM-DD.HH_MM_SS_0XXX.csv  
JFSA [[Margin]] 
State Report 
CSV  
CSV equivalent  
sFTP  
sFTP_JFSA_EOD_Margin_State_Report_02503241-YYYY-MM-DD.HH_MM_SS_0XXX.csv  
  
Portal  
JFSA_EOD_Margin_State_Report_02503241-YYYY-MM-DD.HH_MM_SS_0XXX.csv  
JFSA [[Margin]] 
Submission 
Report CSV  
CSV only  
sFTP  
sFTP_JFSA_EOD_Margin_Submission_Report_02503242-YYYY-MM-DD.HH_MM_SS_0XXX.csv  
  
Portal  
JFSA_EOD_Margin_Submission_Report_02503242-YYYY-MM-DD.HH_MM_SS_0XXX.csv  
JFSA Trade 
Submission 
Report CSV  
CSV only  
sFTP  
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
sFTP_JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
  
Portal  
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
JFSA_EOD_Submission_Report_02503243-YYYY-MM-DD.HH_MM_SS_2XXX.csv  

---

## Page 73

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 73  
 
JFSA [[EOD]] 
Allege Report  CSV only  
sFTP  
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
sFTP_JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
  
  
Portal  
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
JFSA_EOD_Allege_Trade_State_Report_02503248-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
  
JFSA Intraday 
Allege Report  CSV only  
sFTP  
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
sFTP_JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
  
Portal  
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_6XXX.csv  
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_5XXX.csv  
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_4XXX.csv  
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_3XXX.csv  
JFSA_Intraday_Allege_Report_02503249-YYYY-MM-DD.HH_MM_SS_2XXX.csv  
  
 
レポート書式についての注釈:  
(a) XML フォーマットのレポートは、同日レポートに５０万件以上の取引レコードが含まれる場合は分割される。レポ
ートのファイル名の最初の 3 桁でファイル数の総計を判別し、次の 3 桁で何番目のファイルかを示す。(例 
005001 は、5 つに分割されたファイルの 1 つ目のファイルという意味).     
(b)  レポートのタイムスタンプは DD.HH_MM_SS で表示され、時間帯は UTC ベース。 
(c) 上記の表のファイル名は圧縮ファイル内に格納されている実際のファイル名である。sFTP 経由で配信されるレポー
トは以下のいずれかの圧縮タイプを選択できる。UNIX ベースの GZIP(.gz)か Windows ベースの
WINZIP(.zip) 例えば、zip ファイル内に格納されているファイル名は下記の通りになる。 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-YYYY-MM-DD.HH_MM_SS_6XXX.csv 又は 
sFTP_JFSA_EOD_Trade_Activity_Report_02503234-YYYY-MM-DD.HH_MM_SS_001001_6XXX.xml 
 
一方、zip ファイル名は下記の通りになる。 
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-2023-10-27.17_34_31_2CHR.csv.gz 又は  
sFTP_JFSA_EOD_Trade_Activity_Report_02503238-2023-10-27.17_34_31_2CHR.csv.zip  
  
FC 6: 制度改正実施にむけての特別な作業について 

---

## Page 74

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 74  
 
金融機関等は、制度改正実施後、メッセージ・スペシフィケーションで定義された新しい報告要件を満たす内容に従って既存取
引分の内容を更新し再送信することが求められている。 このセクションでは、そのプロセスおよびその他関連するプロセスを説明す
る。 
これらの作業は、テスト環境(UAT)および本番環境の両方で適用されることに留意すること。 
FC 6.1: 制度改正実施に向けての [[DTCC]] によるアクションタイプの初期化
作業  
アクションタイプの許容される順序を検証する新しい機能では、GTR がすべての取引に対して、アクションタイプ順序図に従ったス
テータス（「オープン」、「解約」、「誤提出」、「満期」、「転出」）を保持し、このステータスを使用してその後送信されてくるメッセ
ージのアクションタイプと比較し、許容される順序の観点から問題がないかの検証を行う。制度改正実施に向けて、 GTR では各
取引におけるアクションタイプの情報を初期化し、制度改正実施後のメッセージ送信に対しての順序検証を行う必要がある。 こ
の初期化は、取引および法域（UTI + RCP）ごとに行われる。 アクションタイプルールの詳細については、FC3.8 項に詳細を
記しているのでそれを参照のこと。 
 
制度改正実施時に、GTR では以下の通り、アクションタイプの初期化作業を実施する。 
 
• 施行前営業日の 2024 年 3 月 29 日 23 時 59 分（日本時間）、GTR に現存するすべての有効ポジションを初期
化の対象とする。つまり 2024 年 3 月 29 日以前に削除・解約されておらず、満期日が 2024 年 3 月 29 日より先の
取引すべてを「オープン」ステータスとして初期化される。これにより、「ステートフル」検証が可能になり、これらの取引に対し
て新規取引を示すアクションタイプ NEWT の提出を防ぐとともに、これらのオープンポジションに対して送信されるこ後続のア
クションタイプを許容することができることになる。ただし、金融庁への直接報告から GTR に取引情報報告先を移行する利
用者は、移行する既存取引分の情報について、アクションタイプ NEWT とイベントタイプ PTNG を使用して最初の報告
（移管）を行う必要がある。既存の GTR 利用者は、現存する全てのオープンポジションについて、2024 年 4 月 1 日
以降に GTR にそれらのポジションを構築するために、金融庁が提示した最低限の報告項目を MODI-UPDT のアクション
タイプ/イベントタイプもしくは CORR のアクションタイプで更新する必要がある。その後、VALU や MARU で時価や担保報
告を行うことができるようになる。 
• しかしながら、金融庁に直接報告された取引情報については、GTR は一切情報を保持していないため、GTR に対して新
たに既存ポジションの取引情報を再提出する必要がある。その場合は、アクションタイプ“NEWT”とイベントタイプ“PTNG”
を使って直接報告をしていた既存ポジションの取引情報を GTR に移管すること。 

---

## Page 75

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 75  
 
• 満期日が 2024 年 3 月 30 日から先の日付を持つすべてのポジションの USI Value の値は、新しいデータベースの
Proprietary [[ID]] タグに移行される。この際、USI Prefix フィールドは移行されない。2024 年 4 月 1 日以降、初期化さ
れたポジションについて報告する場合、Proprietary [[ID]] タグを継続して使用、もしくは Global UTI フォーマットの書式要
件([A-Z0-9]{18}[0-9]{2}[A-Z0-9]{0,32}))を満たす値であるならば、Global UTI タグを使って報告が可能。 
• 2024 年 3 月 29 日 23:59（日本時間）以前に「満期や削除（dead）」となった取引、あるいは新しい GTR システ
ムに移行されないその他のすべての過去の取引には、アクションタイプを初期化するデータが存在しないため、これら過去の
取引情報について修正等の報告を行う必要がある場合は、アクションタイプ「NEWT」で改めて当該取引情報の提出が必
要となる。これらの修正報告は制度改正前の過去の取引情報が対象となるが、制度改正後のあらゆる送信については、
新報告要件の検証ルールに準拠する必要があることに注意すること。 
• 取引データの初期化とは別に、GTR では以下の項目の情報を把握し保存する、すなわち USI Value（USI Prefix 無
し）、取引当事者 1、並びに満期日。これは、変更、解約、時価情報など、後に送信されるであろう取引情報の内容を
検証するためにこれらの情報を保存する必要があるためである。したがって、2024 年 3 月 30 日以降、新報告要件で取
引情報の再提出ができていない限り、アクティブなポジションとして TSR には表示されることはない。一方、時価情報メッセ
ージの送信とその対象となる取引への統合については、取引情報の更新（MODI）が再提出されていない場合、GTR は
時価情報メッセージを受領不可とする。しかし本来は、時価情報メッセージの送信前に、新報告要件に沿って且つ検証ル
ールに基づき、対象となる取引の修正報告を完了しておくことが望まれる。これは、2013 年に金融庁報告が開始して以
来現在に至るまで、GTR では極めて複雑なレガシーデータセットを保有しており、それらを移行することが現実的に不可能
であることに起因する。 
• 制度改正実施時に移行の対象とされるべきオープンポジションの情報を、前述の基本項目（USI Value の値を初期化し
た値, RCP, OCP および RSE を含む）と合わせて csv ファイルとして作成し、2024 年 2 月頃に利用者に提供する予定
である。 
FC 6.2: データ統合の予行演習計画 
• 2023 年９月 28 日 23:59（日本時間）までに既存ユーザーである金融機関等は現行の UAT（テスト）環境にポ
ジションを構築しておくことを推奨する。これによって、UAT 環境でデータ統合作業がどのように行われるかを確認することが
できる。UAT 環境や本番環境で複雑なデータ統合作業を行うことは想定していないが、取引情報の初期化の作業後に
MODI を使って制度改正後の要件に沿った取引情報を報告するための予行演習を行うことができるようになる。そのた
め、新制度用 UAT 環境のシステム更新作業を開始する 2023 年９月 28 日までに現行の UAT 環境に提出されてい
るポジションで満期が到来しておらず、FC6.3 および FC6.5 で説明している初期化作業の除外対象とならない取引情
報は、データ統合作業の対象となる。まだテストを行う準備ができていない場合でも、まずは既存ポジションがどのように引

---

## Page 76

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 76  
 
き継がれていくかの確認ができる状態にしておけば、準備が整ったときに必要なテストが行えるように、現行の UAT 環境に
ポジション構築を行っておくことを推奨する。 
• 2023 年９月 29 日から 2023 年 10 月 8 日までの UAT 環境のシステム更新期間中に、UAT 環境にあるポジション
のデータ統合（アクションタイプの初期化）作業を行う。作業完了後、[[DTCC]] は利用者に、アセットクラス別の USI 
Value の値を初期化した値, RCP および RSE とアセットクラス情報を含めた CSV のレポートを提供し、どのポジション情
報が制度改正後の UAT 環境に引き継がれたかどうか確認ができるようにする。これによって、ユーザー側で初期化された
ポジションデータを MODI-UPDT を使って新報告要件に必要な情報を更新する作業が可能になる。データ初期化の対
象となる取引は、まず MODI-UPDT の提出が受領されないと、その他のアクションタイプとイベントタイプの組み合わせで
内容を更新することはできない。新制度用 UAT 環境での TSR の提供は 11 月末の提供となるが、提出状況を確認す
る TAＲは 2023 年 10 月 9 日から利用できている。その後、TSR 提供開始によってポジション情報の内容を検証でき
るようになる。これらは、2024 年 4 月 1 日の本番環境での稼働開始の予行演習となる。 
• 2023 年 11 月末に UAT 環境を開始したが、本番環境のデータを使用したデータ統合の予行演習作業は 2024 年 2
月９日に行う予定。これは作業日時点でのポジション情報を使用して取引情報の初期化を行った場合の結果を還元す
るものであり、ユーザー側でどのポジションが制度改正後の GTR の本番環境に引き継がれるのか、または除外されるのか
を確認することができる。ただし、これは、単に本番環境データの模擬テスト結果に当たるため、MODI-UPDT の作業は
行えない。還元する内容のレポートは 10 月に UAT 環境で提供する CSV レポートの形式と同じである。 
 
 


---

## Page 77

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 77  
 
FC 6.3: 取引の独自性ロジックの変更に伴う重複ポジションの削除 
FC3.4 項に記載のとおり、取引の独自性判定の変更により、制度改正実施時には重複ポジションの削除が必要となる。対象
は、同一の取引識別子 USI + 取引当事者（Trade Party 1）の組み合わせに、複数の異なる取引相手（Trade 
Party 2）が存在する取引情報となる。これらに該当するポジションがある利用者は、ある UTI/USI に対してどの取引相手と
の情報を残すのか判断し、制度改正実施前に重複するポジションを適切に削除（EXIT）することを強く推奨する。 
 
仮に、制度改正実施前にこれらの重複するポジションを削除しない場合、[[DTCC]] は制度改正後にこれら重複するポジションを
Trade State Report に表示できない。 これは GTR が、提出されたメッセージの最新のタイムスタンプに基づき、最も直近に
更新された取引情報を、初期化の対象となるポジションとして認識するためである。GTR はこれらの取引について、自ら市場参
加者や監督当局に削除の EXIT 報告を行うことはない。したがって、あくまで利用者自身の責任により、重複するポジションの
削除を制度改正実施前に行うことが肝要である。 
 
制度改正実施時に複数の TP2 ポジションが存在する USI+TP1 の組み合わせ例： 
USI Trade 
Party 1 
Trade 
Party 2 
最終更新日 コメント 
USI1 LEIa LEIb 01/12/22 TP1 が削除報告を行わない場合、[[DTCC]] はこのポジション情報を報告対象から
除外する。 
USI1 LEIa LEIc 01/15/22 TP1 が削除報告を行わない場合、[[DTCC]] はこのポジション情報を報告対象から
除外する。 
USI1 LEIa LEId 01/27/22 TP1 が削除報告を行わない場合、[[DTCC]] はこのポジション情報を報告対象から
除外する。 
USI1 LEIa LEIe 03/21/22 [[DTCC]] は最新情報として送信されたこのポジション情報を報告対象とする。 
USI1 LEIa LEIf 01/15/22 TP1 が削除報告を行わない場合、[[DTCC]] はこのポジション情報を報告対象から
除外する。 
FC 6.４: 内部取引（Self Trades）の除外 

---

## Page 78

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 78  
 
内部取引の取引情報もアクションタイプの初期化作業で除外される。これらの内部取引の情報は現行のシステムではデータベ
ース上に存在しているが、ユーザーが閲覧するレポートには掲載していない。内部取引とは取引当事者１と２が同一の値であ
ると定義している。制度改正の本番稼働後はこのような内部取引はデータの取り込み時点で受領不可となる。    
FC 6.5: 制度改正実施後の取引情報の更新 
制度改正実施時のオープンポジションを制度施行後に更新しようとする場合、アクションタイプ=「MODI」、イベントタイプ=
「UPDT」という特定の取引情報メッセージを送信してから、後に起こりえるライフサイクルイベントの内容を正しく送信することによ
り、新しい内容に更新することが可能となる。 
 
FC 6.6: 移行期間の報告 
制度改正実施後、すべての取引情報は新しい報告要件を満たす必要がある。 提出内容とアクティビティを示すレポートには、
制度改正実施後に新報告要件で提出されたすべての取引情報が反映される。制度改正以前から現存するオープンポジション
については、制度改正後の検証ルールに基づき新報告要件を満たすように再報告しない限り、TSR には表示されない。制度
上、2024 年 4 月 1 日には、最低限の項目を更新し、180 日間の猶予期限締め切り 9 月 27 日までに残りの項目を更新
して再提出することになっているが、２度以上の再提出する労力を省き事務手続きを効率化するため、最低限の項目に限らず
すべての項目を新要件を満たす内容に更新して、4 月 1 日に再提出作業を一度に済ませることを強く推奨する。 
 
FC 6.7: 制度改正導入までのスケジュール 
制度改正実施直前の週末に行う作業に関する正確なスケジュールは、実施間近に別途発表予定。今後のスケジュール概要
は以下の通り。 

---

## Page 79

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 79  
 
 
 
 
FC 7: 請求額について 
FC 7.1:  請求ロジック階層  
DDRJ は 2024 年 4 月 1 日時点では料金体系の変更を行わないが、請求の対象となるのは、以下の順位である。 “Entity 
Responsible for Reporting”, “Counterparty 1 (reporting counterparty)”,“Submitter identifier”  階層の
最上位にある ERR 報告義務者は GTR の金融庁報告のための契約締結が必須である。全ポジションについての料金はこのロ
ジックに基づいて、対象となる法人に請求される。現行の料金体系は月末時点でのポジション残高に応じて計算されるが、今後
の料金改定の発表があるまで制度改正後もしばらくの間継続する。 
FC 7.2:  請求金額内訳レポート 
請求金額の内訳レポートは、課金対象のポジションがある全てのお客様に対して月次ベースで以下の項目を含む書式で提供
する。金融庁向け報告の制度改正に合わせて不要となった項目の削除、ERR（報告義務者）の追加、取引識別子を UTI
のみに変更し、金融庁報告においては課金対象とならない Execution Agent 項目は削除することとする。 
[[Asset]] Class  
UTI  
Submitted For Reporting Destination  
Billing Period (Month)  


---

## Page 80

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 80  
 
Entity Responsible for Reporting LEI  
Entity Responsible for Reporting [[DTCC]] 
Account  
Entity Responsible for Reporting [[DTCC]] 
Name  
Submitted For LEI  
Submitted For [[DTCC]] Account  
Submitted For Name  
Data Submitter LEI  
Data Submitter [[DTCC]] Account  
Data Submitter Name  
Party 1 LEI  
Party 1 Name  
Party 2 LEI  
Party 2 Name  
Billable [[DTCC]] Account  
Billable Corporate Parent Account  
Billing Exception Reason  
 

---

## Page 81

FUNCTIONAL CHANGE DOCUMENT: JFSA RULES REWRITE]  
 
Page | 81  
 
 
