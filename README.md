# ai-catchup GitHub Pages 配信台帳

公開先: `https://naji555.github.io/ai-catchup/`

このリポジトリは GitHub Pages の公開専用経路です。検索エンジン向けには、ルートの `robots.txt` で全パスを拒否し、各公開 HTML の `<head>` に `noindex,nofollow,noarchive` を指定します。これは検索抑制であり、URLを知る人へのアクセス制御ではありません。

## 公開物

| ファイル | 用途 | 公開日 | 元データ |
| --- | --- | --- | --- |
| `index.html` | AI進化キャッチアップ | 週次更新 | `NJ_Life_with_AI/scripts/ai/ai_catchup/web/index.html` |
| `setup.html` | 既存セットアップ配信（現在は空） | 2026-05-25 | 履歴管理のみ |
| `task14-nlm-500.html` | 既存 NotebookLM 500 調査レポート | 2026-05-26 | 履歴管理のみ |
| `diy-stair-viewer-7c91f2.html` | 2段ベッド階段 3Dビューア | 2026-07-12 | `NJ_Life_with_AI/projects/DIY/2段ベッド階段/階段3Dビューア.html` |
| `nvan-bed-viewer-a4e86d.html` | N-VANベッド 3Dビューア | 2026-07-12 | `NJ_Life_with_AI/projects/DIY/N-VANベッド/N-VANベッド3Dビューア.html` |
| `diy-stair-index-7c91f2.html` | 2段ベッド階段 現場閲覧入口（資料3本+ビューア2本へのリンク集） | 2026-07-12 | 新規作成（モバイル現場閲覧用） |
| `diy-stair-buy-7c91f2.html` | 購入部材リスト・切り出し割付（モバイル版） | 2026-07-12 | `NJ_Life_with_AI/projects/DIY/2段ベッド階段/購入部材リストと切り出し割付.md` |
| `diy-stair-cut-7c91f2.html` | 切断寸法表（モバイル版） | 2026-07-12 | `NJ_Life_with_AI/projects/DIY/2段ベッド階段/切断寸法表.md` |
| `diy-stair-build-7c91f2.html` | 組立手順書（モバイル版） | 2026-07-12 | `NJ_Life_with_AI/projects/DIY/2段ベッド階段/組立手順書.md` |

## noindex確認

```powershell
Invoke-WebRequest https://naji555.github.io/ai-catchup/robots.txt | Select-Object -ExpandProperty Content
(Invoke-WebRequest https://naji555.github.io/ai-catchup/diy-stair-viewer-7c91f2.html).Content | Select-String 'noindex,nofollow,noarchive'
(Invoke-WebRequest https://naji555.github.io/ai-catchup/nvan-bed-viewer-a4e86d.html).Content | Select-String 'noindex,nofollow,noarchive'
(Invoke-WebRequest https://naji555.github.io/ai-catchup/diy-stair-index-7c91f2.html).Content | Select-String 'noindex,nofollow,noarchive'
(Invoke-WebRequest https://naji555.github.io/ai-catchup/diy-stair-buy-7c91f2.html).Content | Select-String 'noindex,nofollow,noarchive'
(Invoke-WebRequest https://naji555.github.io/ai-catchup/diy-stair-cut-7c91f2.html).Content | Select-String 'noindex,nofollow,noarchive'
(Invoke-WebRequest https://naji555.github.io/ai-catchup/diy-stair-build-7c91f2.html).Content | Select-String 'noindex,nofollow,noarchive'
```

## rollback

公開commitを取り消す場合は、履歴を残してrevertします。

```powershell
git revert <公開commitのSHA>
git push origin main
```
