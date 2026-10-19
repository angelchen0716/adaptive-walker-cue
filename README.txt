Adaptive Walker Cue v0.9.1 Voice Hotfix

修正重點：
- 新增「🔊 啟用／測試語音」按鈕，讓 iPhone Safari 在使用者手勢中解鎖 Speech Synthesis。
- 點擊後應立即播放：「語音提示已啟用」。
- 主畫面新增 Voice ON/OFF 狀態。
- 走錯順序時才播放 cue；走對全程安靜。
- 語音錯誤會顯示在 Diagnostic。

測試：
1. 用 Safari 開啟頁面，確認手機非靜音且音量足夠。
2. 點「啟用／測試語音」。
3. 必須先聽到「語音提示已啟用」。
4. 再用 Debug WALKER → 健側腳，應聽到「請先移動患側腳」。
5. Debug WALKER → 患側 → 健側，應保持安靜並完成。
