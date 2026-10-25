Adaptive Walker Cue v0.9.3 — Front Walker View + L/R Mapping

新增：
- Foot Mapping 選項
  1. Swapped（預設）：Screen Left = User Right；Screen Right = User Left
  2. Normal：Screen Left = User Left；Screen Right = User Right
- 針對「後鏡頭裝在助行器前方、朝向使用者」情境，預設採 Swapped。
- 畫面仍維持 LEFT ZONE / RIGHT ZONE，但判斷前會先套用 mapping。
- 左右不再靠硬編碼或記憶。

建議測試：
1. Camera ON
2. 雙腳靜止 → 建立 baseline
3. Foot Mapping 保持 Swapped
4. Debug WALKER
5. 只移動「使用者左腳」
   - 系統應判定 User LEFT
6. 重設
7. Debug WALKER
8. 只移動「使用者右腳」
   - 系統應判定 User RIGHT
9. 若剛好相反，改成 Normal 即可
10. 再測 Walker → 患側 → 健側

注意：
- 這裡的 LEFT/RIGHT 指使用者本人的左右，不是畫面左右。
- 若未來改用前鏡頭、鏡像顯示或不同安裝方向，不需重寫程式，只需切換 Foot Mapping。
