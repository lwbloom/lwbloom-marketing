---
description: X巡回分析と見込み客発見（LinkedInは対象外・別サイクルで手動確認）
---

以下の作業を順番に行い、レポートとして出力してください。

**注記：LinkedInは自動化・スクレイピング対策により継続的な自動取得ができないため、日次のx-checkの確認項目からは外している。LinkedIn運用状況（週1〜2本の記事執筆の進捗など）は、のりあきさんが週次・月次など別サイクルで手動確認する運用とする。**

---

## 1. 自社Xアカウント分析

X: https://x.com/lwbloom にアクセスし、現在の投稿状況を確認すること。

分析観点：
- 直近の投稿頻度
- 5つの型（違和感/構造化/面接官目線/ケース/導線）のバランス
- エンゲージメントが高そうな投稿の特徴
- 不足している型の投稿案を3つ提案
　ルールは、下記「## X投稿の文体ルール（最重要）」に沿って作成する
　文字数は200文字前後
　前日と同じ内容は記載しないこと
　**投稿案の文面は、既存のX投稿（実際の直近投稿）を読み込み、そこから抽出した本人の実際の言い回し・語尾・トーンをベースに作成すること。**
　下記の文体ルールはあくまで一般的な指針であり、実際の投稿内容と食い違う場合は実際の投稿の口調を優先する。

### 投稿案作成前のトレンド確認（必須）

3つの投稿案を作る前に、X上で今どんな話題が動いているかを検索で確認し、実在するトレンド・議論に根ざした内容にすること。架空の場面や自分の想像だけで書かない。

最低限含める検索キーワード：
- 「転職エージェント 後悔」
- 「転職エージェント 話が違う」
- 「内定 入社したら 話が違う」

上記に加え、その時々でX上のトレンド（本日のニュース欄や話題のポスト）に50代の転職・キャリア・面接・管理職に関連するものがあれば、それも検索・確認して投稿案のネタ候補にする。

見つけたトレンド・議論は、個人の作り話にせず、「最近、X上でよく見かける話があります」のように実際に観測した流れとして扱い、そこから自分の経験・視点を重ねて書くこと（特定個人の投稿を無断で引用・要約しすぎない）。

**ケース投稿についての重要な制約：**
ケース投稿（Before/After型）は、のりあきさんが実際に行ったセッションの内容（匿名化可）に基づくものに限る。実在しない相談者（架空の「Kさん」「Mさん」等）を作り出して投稿案にすることは絶対にしない。ケース投稿の型が手薄でも、実際のエピソードが手元にない場合は無理に埋めず、他の4つの型（違和感/構造化/面接官目線/導線）から提案するか、のりあきさんに実際にあったセッションのエピソードを尋ねること。

### 投稿案へのX投稿ボタン付与（必須）

3つの投稿案それぞれに、ワンクリックでX投稿画面を開く「投稿ボタン」を付与すること。
これはX公式のWeb Intent機能（規約準拠・自動化検知の対象外）を用いる。

**手順：**
1. 各投稿案の本文（改行・記号を含む全文）をURLエンコードする
   （改行は %0A、スペースは %20 等。日本語・記号もすべてエンコードすること）
2. 次のURL形式を組み立てる：
   `https://x.com/intent/post?text=（エンコード済み本文）`
3. mdファイル内では、各投稿案の直後に以下のMarkdownリンクを記載する：
   `[𝕏 この内容で投稿する](組み立てたURL)`

**注意事項：**
- 本文が欠けないよう、エンコードは全文に対して漏れなく行うこと
- 導線投稿にCTAのURL（lwbloom.jp）が含まれる場合、そのURLも本文の一部としてエンコードに含めること
- エンコード後の投稿本文が実質140字（URL含む）を大きく超える場合は、本文を短縮して文字数警告を注記すること

---

## 2. 見込み客の発見

以下のキーワードでX上を検索し、Life & Work Bloomのターゲットになりうる投稿を探すこと。

検索キーワード：
- 「50代 転職 迷い」
- 「役職定年 不安」
- 「50代 面接 通らない」
- 「このままでいいのか 仕事 50代」
- 「早期退職 迷い 決断」
- 「50代 キャリア モヤモヤ」
- 「管理職 疲れた 50代」

発見した投稿を以下の形式で整理すること：

### 見込み客リスト
| 投稿者 | 悩みの分類（場面A〜E） | 概要 |
|---|---|---|

**投稿者列の必須ルール：**
- 投稿者名は必ず `[@ハンドル名](投稿URL)` の形式でMarkdownリンクとして埋め込むこと（プレーンテキストでハンドル名だけを書かない）
- リンク先は、その投稿者のプロフィールURLではなく、**該当する具体的な投稿（ステータス）へのパーマリンク**（例：`https://x.com/handle/status/1234567890`）にすること
- パーマリンクが確認できない投稿は掲載しない（プロフィールURLで代用しない）

場面の分類基準：
- 場面A：転職か現職か（選択迷い型）
- 場面B：役職定年・再雇用後の設計（構造変化型）
- 場面C：早期退職の意思決定（時限判断型）
- 場面D：管理職としての停滞・消耗（蓄積疲弊型）
- 場面E：面接に通らない50代（成果直結型）

---

## 3. 返信したい見込み客（リプライ候補）

見込み客リストの中から、のりあきさんがリプライすべき投稿をTOP5で選出すること。

選出基準：
- **投稿日が当日または前日のものに限定すること**（古い投稿へのリプライは不自然なため）
- のりあきさんの武器（面接官経験・管理職経験・同世代当事者性）が直接活きる
- リプライで「売り込み」にならず「この人は分かっている」と思ってもらえる
- フォロワー数やエンゲージメントが一定以上ある（リーチが見込める）
- 前日と同じ投稿は選出しない

**投稿日の確認方法：**
X投稿のURLに含まれるステータスID（数値）は時系列順になっている。
現在（2026年7月）の目安：ステータスIDが `2076000000000000000` 以上を当日・前日の投稿として扱う。
これより小さいIDの投稿は数週間〜数ヶ月前の投稿である可能性が高いため、リプライ候補から除外すること。

**検索ツールの制約への対応：**
Web検索ツールでは「今日・昨日」への絞り込みが技術的に困難な場合がある。
その場合は以下の方法で対応すること：
1. 検索クエリに投稿IDの目安を含めて絞り込みを試みる
2. それでも最新投稿が見つからない場合は「**当日・前日の投稿が確認できませんでした**」とレポートに明記し、候補を空欄にするかリプライ可能性の参考情報として古い投稿を注記付きで掲載する
3. 「候補が見つからなかった」は正直な報告であり、古い投稿を新しいかのように偽って掲載してはならない

以下の形式で出力すること：

### リプライ候補TOP5
各候補について：
- 投稿URL
- 悩みの分類（場面A〜E）
- なぜこの投稿にリプライすべきか（理由）
- リプライ案（2パターン：短文版・丁寧版）

リプライの方針：
- 絶対に売り込まない
- 共感 → 面接官目線 or 管理職経験からの一言 → 価値提供
- サービスURLは貼らない。信頼を積むだけ
- リプライの言葉遣いは丁寧語で「です」「ます」調にすること

---

## 4. 競合動向（簡易チェック）

以下の競合アカウントの直近の動きを簡潔に確認すること。

- @2G_coach（47歳キャリア再起動）
- @coach_coo（40-50代セカンドキャリアコーチ）
- @Katsuta_0511（ライフシフトラボ取締役）
- @ebi320118（ミドル・シニア転職支援）
- @asuiro_lab（50代人生再設計）

確認観点：
- 新しい施策やキャンペーンをやっていないか
- のりあきさんと差別化できているか
- 参考にすべき投稿があるか

---

## 5. GA4集客データ分析

まず以下のコマンドで仮想環境を有効化すること：

```bash
source ~/Library/Mobile\ Documents/com~apple~CloudDocs/projects/lwbloom/marketing/.venv/bin/activate
```

**注記：`.venv`はマシン固有（アーキテクチャ依存）である。`python3 -m pip --version`などで動作確認し、importエラーが出る場合は`rm -rf .venv && python3 -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt`でこのマシン用に作り直すこと。**

以下のPythonスクリプトを `$TMPDIR/ga4_fetch.py` として作成し実行すること。

```python
import json
import os
from datetime import datetime, timedelta
from google.analytics.data_v1beta import BetaAnalyticsDataClient
from google.analytics.data_v1beta.types import (
    RunReportRequest, Dimension, Metric, DateRange, OrderBy
)
from google.oauth2 import service_account

CREDENTIALS_PATH = os.path.expanduser(
    "~/Library/Mobile Documents/com~apple~CloudDocs/Documents/Life&Work Bloom/鍵/lwbloom-mcp-60b75c8ca130.json"
)
PROPERTY_ID = "536766233"

credentials = service_account.Credentials.from_service_account_file(
    CREDENTIALS_PATH,
    scopes=["https://www.googleapis.com/auth/analytics.readonly"]
)
client = BetaAnalyticsDataClient(credentials=credentials)

end_date = datetime.today().strftime("%Y-%m-%d")
start_date = (datetime.today() - timedelta(days=90)).strftime("%Y-%m-%d")
date_range = DateRange(start_date=start_date, end_date=end_date)

results = {}

# チャネル別集客データ
req1 = RunReportRequest(
    property=f"properties/{PROPERTY_ID}",
    dimensions=[Dimension(name="sessionDefaultChannelGroup")],
    metrics=[
        Metric(name="sessions"),
        Metric(name="totalUsers"),
        Metric(name="engagementRate"),
        Metric(name="conversions"),
    ],
    date_ranges=[date_range],
    order_bys=[OrderBy(metric=OrderBy.MetricOrderBy(metric_name="sessions"), desc=True)]
)
r1 = client.run_report(req1)
results["channel"] = [
    {
        "channel": row.dimension_values[0].value,
        "sessions": row.metric_values[0].value,
        "users": row.metric_values[1].value,
        "engagement_rate": f"{float(row.metric_values[2].value)*100:.1f}%",
        "conversions": row.metric_values[3].value,
    }
    for row in r1.rows
]

# 上位ページ別データ
req2 = RunReportRequest(
    property=f"properties/{PROPERTY_ID}",
    dimensions=[Dimension(name="pagePath"), Dimension(name="pageTitle")],
    metrics=[
        Metric(name="screenPageViews"),
        Metric(name="averageSessionDuration"),
        Metric(name="bounceRate"),
    ],
    date_ranges=[date_range],
    order_bys=[OrderBy(metric=OrderBy.MetricOrderBy(metric_name="screenPageViews"), desc=True)],
    limit=10
)
r2 = client.run_report(req2)
results["pages"] = [
    {
        "path": row.dimension_values[0].value,
        "title": row.dimension_values[1].value,
        "pageviews": row.metric_values[0].value,
        "avg_duration": f"{float(row.metric_values[1].value):.0f}秒",
        "bounce_rate": f"{float(row.metric_values[2].value)*100:.1f}%",
    }
    for row in r2.rows
]

# 流入元別データ
req3 = RunReportRequest(
    property=f"properties/{PROPERTY_ID}",
    dimensions=[Dimension(name="sessionSource"), Dimension(name="sessionMedium")],
    metrics=[
        Metric(name="sessions"),
        Metric(name="totalUsers"),
        Metric(name="engagementRate"),
    ],
    date_ranges=[date_range],
    order_bys=[OrderBy(metric=OrderBy.MetricOrderBy(metric_name="sessions"), desc=True)],
    limit=10
)
r3 = client.run_report(req3)
results["source_medium"] = [
    {
        "source": row.dimension_values[0].value,
        "medium": row.dimension_values[1].value,
        "sessions": row.metric_values[0].value,
        "users": row.metric_values[1].value,
        "engagement_rate": f"{float(row.metric_values[2].value)*100:.1f}%",
    }
    for row in r3.rows
]

with open(os.path.join(os.environ.get('TMPDIR', '/tmp'), 'ga4_data.json'), "w", encoding="utf-8") as f:
    json.dump(results, f, ensure_ascii=False, indent=2)

print("GA4データ取得完了")
print(json.dumps(results, ensure_ascii=False, indent=2))
```

スクリプト作成後、以下のコマンドで実行すること：

```bash
~/Library/Mobile\ Documents/com~apple~CloudDocs/projects/lwbloom/marketing/.venv/bin/python3 "$TMPDIR/ga4_fetch.py"
```

**接続エラーになる場合：** 環境にHTTPプロキシ（`HTTP_PROXY`/`HTTPS_PROXY`等）が実際に設定されていない限り、gRPCのプロキシ環境変数を追加してはならない。直接接続で到達できることを`curl -s -o /dev/null -w "%{http_code}" https://analyticsdata.googleapis.com/`等で確認してから実行すること。

取得したデータをもとに以下を分析し、レポートに含めること：

### GA4分析観点

**チャネル別分析：**
- 最も貢献しているチャネルと伸びしろのあるチャネル
- エンゲージメント率・コンバージョン率が低いチャネルの課題

**ページ分析：**
- 最も読まれているページと直帰率が高く要改善のページ
- Xからの流入と連動しているページはどれか

**集客改善施策：**
Life & Work Bloom（50代キャリア支援）に特化した施策を3つ提案すること。
各施策は以下の形式で記載：
- **施策名**
- **優先度**（高・中・低）
- **根拠**（どのデータから導いたか）
- **具体的アクション**
- **期待効果**

---

## X投稿の文体ルール（最重要）

あなたは「コンサルタント」でも「コーチ」でもない。
58歳、IT企業で管理職を20年やった人間として書く。

**投稿案を作成する前に、必ず実際の直近投稿（最低10〜15件）を確認し、そこで使われている語尾・敬語の有無・問いかけ方・締め方のパターンを抽出すること。以下のルールと実際の投稿の口調が食い違う場合は、実際の投稿を優先する。**

### 絶対に守ること
1. **正論を書くな。** 「〜が大切です」「〜すべきです」は禁止。
2. **教える立場で書くな。** 上から目線の構造化・整理は読者が最も嫌うもの。
3. **自分が見た具体的な場面から始めろ。** 「○年前」「あの会議で」「金曜の夜」など、時間と場所がある文章にする。
4. **感情は説明するな、描写しろ。** 「不安だった」ではなく「帰りの電車で降りる駅を一つ乗り過ごした」。
5. **オチをつけるな。** きれいにまとめない。投げっぱなしでいい。読者が「…俺もだ」と思えば勝ち。
6. **1投稿に1場面だけ。** 複数のメッセージを詰め込まない。
7. **CTA（導線）は5投稿に1回だけ。** それ以外は一切売り込まない。
8. **敬語を使うな。** 「です・ます」ではなく「〜だった」「〜だろう」の語り口調。

### 参考にすべきトーン
- 居酒屋で同世代の友人に話すような口調
- 日経の「私の履歴書」の独白パート
- 退職した先輩が後輩に本音で話すときの空気感

### NG例（AIっぽい・正論）
「管理職として孤独を感じていませんか？一人で抱え込まず、まず言語化することが大切です。」

### OK例（現場の言葉）
「部長になって3年目の冬、初めて辞表を書いた。出さなかったけど、書いたことで少し楽になった。あれは何だったんだろう。」

### 投稿のネタの出し方
以下の問いに答える形で場面を思い出し、そこから書く：
- 管理職時代、一番キツかった瞬間は？
- 面接官をしていて「この人、本当のことを言っていないな」と感じた場面は？
- 50代の同僚や部下が急に元気をなくした時、何が起きていた？
- 自分が「もう無理だ」と思った時、最初に何をした？

---

## 出力先

レポートを reports/ フォルダに以下のファイル名で保存すること：
`reports/x-check-YYYY-MM-DD.md`（当日の日付）

レポートには以下のセクションを全て含めること：
1. 自社Xアカウント分析
2. 見込み客リスト
3. リプライ候補TOP5
4. 競合動向
5. **GA4集客データ分析・施策提案**

作成したmdファイルをwebで視覚的に見やすくするファイルを作成すること。
出力するWebページは、`~/projects/lwbloom/marketing/reports/Master.html` のフォーマットに合わせること。

**HTML化における投稿ボタンの描画（必須）：**
セクション1の3つの投稿案それぞれについて、投稿本文（post-content）の直後に、
X投稿画面を開くボタンを配置すること。ボタンは以下のHTMLで生成する：

```html
<a href="https://x.com/intent/post?text=（エンコード済み本文）"
   target="_blank" rel="noopener"
   style="display:inline-block; margin-top:12px;
          background:linear-gradient(135deg,#0f3460,#533483);
          color:#fff; text-decoration:none; border-radius:8px;
          padding:10px 20px; font-size:0.88rem; font-weight:700;">
  𝕏 この内容で投稿する
</a>
```

href の text パラメータには、その投稿案の本文をURLエンコードした文字列を入れること。
エンコード処理を確実に行うため、HTML生成時は以下のいずれかを用いる：
- Pythonで生成する場合：`urllib.parse.quote(本文, safe='')`
- JavaScriptで生成する場合：`encodeURIComponent(本文)`

ボタンを押すと、本文が入力済みのX投稿画面が新規タブで開く。
