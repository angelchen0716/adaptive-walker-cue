Adaptive Walker Cue v0.8.1 HOTFIX

這版刻意簡化，只測：
Camera -> SET BASELINE -> LEFT/RIGHT displacement

修正重點：
- 重寫 Camera 啟動事件。
- 增加 getUserMedia 支援檢查。
- 增加 Safari Camera error diagnostic。
- 移除 IMU / sequence engine，避免其他 JavaScript 錯誤影響 Camera button。
- Baseline tracking 保留。

測試：
1. 上傳 index.html 到 GitHub repo 根目錄，取代舊版。
2. 等 Pages deployment 完成。
3. Safari 開 ?v=81。
4. 點「啟用後鏡頭」。
5. Diagnostic 應先顯示：
   Start button tapped. Requesting camera permission…
   接著成功時：
   Camera started successfully.
6. 雙腳站好 -> SET BASELINE -> 慢慢移左腳/右腳。
7. 記錄 LEFT CHANGE / RIGHT CHANGE。

若 Camera 失敗，直接把 Diagnostic 的 CAMERA ERROR 文字或截圖傳回來。
