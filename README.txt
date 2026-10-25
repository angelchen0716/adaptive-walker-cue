Adaptive Walker Cue v0.9.3.1 — Button Hotfix

修正：
- 修正 v0.9.3 Foot Mapping 函式殘留字元造成的 JavaScript syntax error。
- Camera / Calibration / IMU / Voice / Debug 按鈕事件可正常綁定。
- 保留 Swapped / Normal Foot Mapping。
- Swapped 預設：Screen Left = User Right；Screen Right = User Left。

建議測試：
1. 上傳此 index.html 覆蓋 GitHub Pages 根目錄舊檔。
2. 用 ?v=0931 開啟，避免 Safari cache。
3. 先按「啟用後鏡頭」；應跳出相機權限或直接開啟。
4. 再測「啟用／測試語音」。
5. Debug WALKER / LEFT / RIGHT 都應可按。
