# Supabase 資料安全設定

本網站的 `anon / publishable key` 可以公開在前端，但資料表必須啟用 Row Level Security（RLS）。

## 正式上課前的建議

1. `mood_records` 允許匿名使用者新增紀錄。
2. 不要允許匿名使用者直接讀取個別座號、留言、AI 回應或求助內容。
3. 班級統計應改由只回傳各心情人數的資料庫函式提供。
4. 老師查看個別紀錄時，應使用 Supabase Auth 登入。
5. `service_role` 金鑰不得放在網頁或 GitHub。

目前學生頁面的「班級天氣」已只顯示匿名人數，但完整的資料保護仍需在 Supabase 後台設定 RLS。