Adaptive Walker Cue v0.9.2 — Front Walker View

這版配合新的實際助行器視角：
- 手機裝在前方橫桿中央。
- 後鏡頭朝使用者並略向下。
- 畫面保留左右小腿、腳踝、完整鞋子與少量地面。
- LEFT / RIGHT ROI 改成更高、更寬的長條區域，適合目前照片中的構圖。
- Walker 移動後等待時間加長到約 500 ms，再建立 baseline，降低助行器本身晃動造成的假訊號。
- 每一步之後重新 baseline。
- Vision threshold 預設仍 30%；dominance 改為 1.25x。
- 保留左右腳 calibration、IMU、Voice、Debug fallback。

第一次實機測試：
1. 手機先固定好，不要手持。
2. Camera ON。
3. 確認兩腳各自在 LEFT/RIGHT ZONE，鞋子不要跨過中央太多。
4. 完成左右腳 calibration。
5. Voice ON。
6. 先用 Debug WALKER → 真實移左腳/右腳測 Vision。
7. Vision 穩定後才啟用 IMU。
8. 最後測真實 Walker → 患側 → 健側。

若 LEFT/RIGHT 在固定後仍系統性顛倒，不要改支架，下一版直接加入 Mirror toggle。
