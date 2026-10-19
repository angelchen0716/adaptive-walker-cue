Adaptive Walker Cue v0.3 — Smartphone IMU Prototype

這一版新增：
1. DeviceMotion 手機 IMU 讀取。
2. iPhone Safari 的動作感測權限按鈕。
3. 即時顯示 movement intensity。
4. 當 IMU movement intensity 超過初始 threshold 時，自動產生「助行器前移」事件。
5. 保留 Debug 手動助行器按鈕，避免實機感測失敗時無法展示。
6. 保留 v0.2 語音與步序 state machine。

重要：
- v0.3 的 threshold 2.20 m/s² 只是「初始測試值」，不是驗證後的臨床門檻。
- 必須上 HTTPS（例如 GitHub Pages）後再用 iPhone Safari 測試 DeviceMotion。
- iPhone 上要點「啟用手機動作感測」並允許權限。
- 真正綁到助行器後，要記錄靜止、輕碰、正常前移的 movement intensity，再做 v0.4 threshold / debounce 校正。
- 若 IMU 尚未成功，仍可使用 Debug 按鈕測試完整流程。

建議測試順序：
A. 電腦：先確認原本按鈕和語音仍正常。
B. GitHub Pages HTTPS：iPhone Safari 開啟。
C. 點「啟用手機動作感測」。
D. 手持手機快速前移一下，觀察 movement intensity 和是否自動進入「等待患側腳」。
E. 再測錯誤流程：IMU偵測 → 健側腳 → 語音「請先移動患側腳」。
