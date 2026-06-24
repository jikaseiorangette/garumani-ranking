# がるまに ドラマCD ランキング分析

DLsite がるまに（乙女向けドラマCD）の週間ランキングを毎日23:30頃に自動取得・分析するサイトです。

## サイト

https://jikaseiorangette.github.io/garumani-ranking/

## データソース

- ランキング: https://www.dlsite.com/girls-drama/ranking/week/=/sort/sale
- 新着: https://www.dlsite.com/girls-drama/fsr/=/order/release_d/work_category/drama

## 構成

```
garumani-ranking/
├── scraper.py              # スクレイパー本体
├── requirements.txt
├── .github/workflows/
│   └── scrape.yml          # 毎日23:30自動実行
├── data/                   # スクレイパーが生成するデータ
│   ├── latest.json         # 最新ランキング
│   ├── history.json        # ランキング履歴
│   ├── work_meta.json      # 作品メタデータ（発売日等）
│   ├── graph.json          # グラフデータ
│   └── meta.json           # 統計データ
└── docs/                   # GitHub Pages配信用
    ├── index.html          # サイト本体
    └── data/               # dataと同内容（GitHub Pages用）
```
