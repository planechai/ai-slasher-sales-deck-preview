# AI Slasher 訓練營｜銷售互動 Deck（2026-10-30）

## 點用
1. 用瀏覽器打開 `index.html`（本地雙擊或 `python3 -m http.server`）。
2. 鍵盤 `←` `→`（或空白鍵／PageUp／PageDown）翻頁；右下角按鈕亦可。
3. 大屏 1920×1080 stage，自動 scale-to-fit。
4. 之後要把現場投票／手機入場：將 `slides.json` 丟入 Pulse Room 式 room（本包未開 live server）。

## 邊頁有互動
| 頁 | id | 互動 |
|----|-----|------|
| 02 | join | overlay `join`（入場玩法位） |
| 05 | poll-pain | overlay `poll`：你而家最痛係？ |
| 12 | prompt-90d | overlay `prompt`：90 日最想改善 1 件事 |
| 14 | checklist | audienceElements `copy`：啟動 Checklist Prompt |
| 15 | cta | audienceElements `link`×2 + HTML 大掣 |
| 16 | thanks | overlay `prompt` Q&A + `link`×2 |

## CTA 去邊
- 銷售頁：https://startfree.io/ →「立即加入訓練營」
- YouTube：https://www.youtube.com/@StartFree →「訂閱 StartFree」

## 檔案
- `index.html` — 16 頁可投影 deck
- `slides.json` — visual + overlays + audienceElements
- `README.md` — 本說明
