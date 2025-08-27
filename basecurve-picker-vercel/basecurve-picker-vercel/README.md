# 基弧選擇器 — Vercel 部署包

這是可直接部署到 Vercel 的最小專案（純靜態）。

## 方法 A：從 GitHub 匯入（推薦）
1. 將本資料夾建立成一個 GitHub repo（或使用你現有的 repo）。
2. 到 Vercel Dashboard → **Add New… → Project** → **Import Git Repository**。
3. 選擇此 repo：
   - **Framework Preset**：Other
   - **Root Directory**：`/`（根目錄）
   - **Build Command**：空白（None）
   - **Output Directory**：空白（None）
4. 直接 **Deploy**。部署完成後會得到網址（例如 `https://<project>.vercel.app`）。

> 本專案不需要 Node build；Vercel 會直接當作靜態網站提供 `index.html`。

## 方法 B：拖拉上傳（無需 GitHub）
1. 到 Vercel Dashboard → **Add New… → Project** → 右上角 **Deploy**（Drag & Drop）。
2. 將此資料夾整包拖進去，按 **Deploy** 即可。

## 方法 C：Vercel CLI
```bash
npm i -g vercel
vercel --yes --prod
```
（第一次會詢問 Team / Project 名稱，後續再 `vercel --prod` 即可更新上線）

## 檔案說明
- `index.html`：單檔網頁（已可直接使用）
- `basecurve_mapping.json`：對應表（可選）
- `vercel.json`：可選設定（靜態站其實可不設）。