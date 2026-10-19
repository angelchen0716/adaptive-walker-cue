Adaptive Walker Cue v0.8.2

新增：
- Left/Right calibration：不假設畫面 ROI 與實際左右腳 mapping。
- 預設 step threshold 30%。
- Dominance gate 1.35x。
- 必須連續 2 次分析確認才輸出 STEP。
- 兩側同時大幅變化或 dominance 不足時：不判定，不硬猜。

建議測試：
1. Camera ON。
2. 開始左右腳校正。
3. 依畫面指示先左腳、再右腳。
4. 校正完成後確認 Mapping。
5. SET TEST BASELINE。
6. 分別移左腳/右腳各 5 次，記錄是否仍有左右顛倒。
7. 若失敗，截圖當時 ROI A/B 數值與 Confidence。
