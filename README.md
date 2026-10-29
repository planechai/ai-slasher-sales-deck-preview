# AI Slasher 訓練營｜銷售互動 Deck（2026-10-30）

雙模式 HTML deck（對齊 Pulse Room：大屏 `/present` vs 觀眾手機 `/view`）。本包係**靜態預覽**——投票／提交只喺瀏覽器本機，冇 live room server。

## Preview URL
- GitHub Pages：https://planechai.github.io/ai-slasher-sales-deck-preview/
- 強制手機觀眾 UI：`?mode=view`
- 強制大屏投影 UI：`?mode=present`
- 唔帶參數：闊螢幕（>820px）用 present；窄螢幕自動 view

## 點用
1. 打開 `index.html`（雙擊或 `python3 -m http.server`）。
2. 鍵盤 `←` `→`／空白鍵／PageUp／PageDown 翻頁；底部／右下角掣亦可。
3. 手機 view 可用左右 swipe。
4. 右上／底欄細字可切換「大屏模式」／「手機模式」。
5. Live 現場：之後把 `slides.json` 接入 Pulse Room 式 room（overlays + audienceElements）。

## 雙模式 vs Pulse Room
| | Pulse Room | 本預覽 |
|--|--|--|
| 大屏 | `/present/{code}` 1920×1080 | `?mode=present` 同款 stage + scale-to-fit |
| 手機 | `/view/{code}` mobile-first | `?mode=view` full-bleed 直式卡，**唔係**縮細 16:9 |
| 同步 | room `currentSlide` | 本機各自翻頁（預覽） |
| 投票／Prompt | server + 審批 | 本機 tally／toast「已記錄（預覽；live 要審批）」 |

## 邊頁有互動（預覽可用）
| 頁 | id | 互動 |
|----|-----|------|
| 02 | join | 入場說明（觀眾指引；已移除 meta 備註） |
| 05 | poll-pain | 可點 A–D；本機 tally bar（標「預覽投票」）；手機直向全寬掣 |
| 12 | prompt-90d | 文字框 + 提交 → toast |
| 14 | checklist |「一鍵複製」clipboard（內容同 `slides.json` audienceElements） |
| 15 | cta | 大掣連結 startfree.io / YouTube @StartFree |
| 16 | thanks | Q&A 輸入 + 提交 toast；CTA 連結 |

## CTA
- 銷售頁：https://startfree.io/ →「立即加入訓練營」
- YouTube：https://www.youtube.com/@StartFree →「訂閱 StartFree」

## 品牌色
- Navy `#0B1F3A` · Gold `#D4A017` · Bright `#F5C84C`

## 檔案
- `index.html` — 16 頁；present + view 雙模式
- `slides.json` — visual + overlays + audienceElements（`modes` 註記）
- `README.md` — 本說明
