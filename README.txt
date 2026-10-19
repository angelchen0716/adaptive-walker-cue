Adaptive Walker Cue v0.8 — Baseline Foot Displacement

快速測試：
1. Camera ON。
2. 雙腳不動，按 SET BASELINE。
3. 慢慢向前移左腳，記錄 LEFT/RIGHT CHANGE。
4. 回原位、重新 SET BASELINE，再測右腳。
5. 預設 Step threshold 18%、Pixel sensitivity 28，皆可調。

核心差異：
v0.7 = 相鄰 frame 比較。
v0.8 = 每一 frame 與固定 baseline 比較，所以慢速踏步也會累積出差異。

Walker 自動模式：
IMU Walker event → 350 ms → baseline → 第一腳辨識。
