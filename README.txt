Adaptive Walker Cue v0.7 — Fast Foot Motion Tracking

Why v0.7:
v0.6 的 full-body pose model 在「walker 中央、鏡頭斜向後下方、只看到下肢」的第一人稱/局部人體視野下不穩。
v0.7 改成 task-specific ROI motion detection，不需要辨識完整人體。

原理：
Camera → LEFT/RIGHT ROI → frame difference → motion % → LEFT/RIGHT event
IMU → WALKER event
Sequence engine → Walker → affected → unaffected

建議手機位置：
- walker 前方上橫桿中央
- 後鏡頭朝使用者方向、斜向下
- 畫面應包含左右鞋、小腿下段，以及腳前後移動空間

測試：
1. 上傳 index.html 到 GitHub Pages root，網址加 ?v=7。
2. 啟用 Camera。
3. 靜止：記錄 LEFT/RIGHT MOTION 背景值。
4. 單獨動左腳：記錄 L/R motion。
5. 單獨動右腳：記錄 L/R motion。
6. 預設 motion threshold 12%、pixel sensitivity 28 只是起始值。
7. 再啟用 IMU，測 Walker → 左/右第一步。
8. Debug buttons 永久保留作 fallback。

限制：
- 目前左右 ROI 固定，實際 walker mounting 後可能需要調 ROI。
- 光影劇烈改變、walker 本身進入 ROI、相機持續震動都會造成 frame-difference false positive。
- v0.7 先專注辨識 Walker 後「第一個移動的腳」；完整第二步自動偵測可在校正穩定後加入。
- 不可宣稱臨床辨識準確度。
