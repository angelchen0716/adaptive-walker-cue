Adaptive Walker Cue v1.0 Finalist Demo

主流程已簡化：
1. 選擇患側（左 / 右）
2. 按「開始 Demo」
3. 系統自動啟用語音、Camera、IMU
4. 語音依序：
   - 請移動助行器
   - 請移動患側腳
   - 請移動健側腳
   - 完成
5. 走錯才插入糾正：
   - 請先移動患側腳
   - 請移動健側腳

攝影：
- 固定使用目前實機安裝方式：手機在助行器前方，後鏡頭朝向使用者。
- 因此固定 mapping：
  Screen Left = User Right
  Screen Right = User Left
- Demo 主畫面不再要求校正。
- Walker 移動後自動等待約 600 ms，再抓 foot baseline。
- 每一個腳步事件後自動重新 baseline。

現場備援：
- 工程模式保留 WALKER / USER LEFT / USER RIGHT 手動事件。
- 若 iPhone IMU 權限或現場光線影響感測，仍可展示完整 interaction logic。

重要：
- Step threshold、IMU threshold 仍屬 prototype calibration parameters。
- 決賽前請在「手機真正固定於助行器」的狀態下測試。
