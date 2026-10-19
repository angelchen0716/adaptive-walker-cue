Adaptive Walker Cue v0.6 — Vision Step Detection

新增：
- MediaPipe Pose 在瀏覽器內進行人體姿勢 landmark detection。
- 顯示左右 ankle / heel / foot-index landmarks。
- IMU 偵測 WALKER 後，建立雙腳 baseline。
- 追蹤左右腳 landmark 位移，嘗試自動產生 LEFT STEP / RIGHT STEP。
- 患側可選左/右。
- Foot movement threshold 可調。
- 保留 WALKER / LEFT / RIGHT Debug fallback。

GitHub：
1. 以新版 index.html 取代 repository 根目錄舊檔。
2. Commit changes，等待 Pages deployment。
3. iPhone Safari 使用 ?v=6 開啟。
4. 先啟用「鏡頭＋姿勢辨識」，第一次載入需要網路下載 MediaPipe 模型。
5. 確認畫面在腳踝/腳跟/足部出現 landmarks。
6. 再啟用 IMU。
7. Walker 前移後停穩，約 0.45 秒後建立 baseline，再移動一腳。
8. 觀察 LEFT MOVE / RIGHT MOVE 與是否自動觸發 STEP。

重要：
- v0.6 是實驗性 PoC，不可宣稱已有臨床準確度。
- 預設 foot threshold 0.035 是初始測試值，需要依實機角度校正。
- 若自動辨識不穩定，使用 Debug fallback 完整展示 sequence engine。
- MediaPipe 資源目前由 CDN 載入，因此第一次開啟需網路；決賽前可再做離線化版本。
