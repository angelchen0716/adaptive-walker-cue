Adaptive Walker Cue v0.9 — Closed-loop Prototype

核心流程：
Walker IMU event
→ 350 ms settle
→ Vision baseline
→ 偵測第一腳
→ 若健側先走：語音「請先移動患側腳」並重新 baseline
→ 患側正確：重新 baseline
→ 偵測健側
→ 完成本輪
→ 約 1.6 秒後 reset

使用順序：
1. Camera ON
2. 左右腳校正
3. 選擇患側
4. IMU ON
5. 正式測試

建議先用 Debug WALKER 測 Vision 完整閉環，確認穩定後才用真實 IMU 觸發。

決賽 demo 保險：
Engineering Mode 內保留 WALKER / LEFT / RIGHT debug buttons。
若現場感測受環境影響，仍可示範 interaction logic。

注意：
- Vision threshold 30%、dominance 1.35x 為 PoC calibration parameters。
- IMU threshold 2.20 m/s² 需裝上 walker 後重新校正。
- 不代表臨床驗證或準確率。
