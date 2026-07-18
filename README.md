# Soul Eater — Episode 01｜《噬魂記》第一集

AI 輔助影視製作儲存庫，涵蓋故事拆解、角色與場景一致性、提示詞生成、影片批次製作、剪輯組裝與品質驗收。

## 專案狀態

- 儲存庫初始化：進行中
- 當前階段：Agent Pipeline Configuration
- 首批執行範圍：`SH001–SH030`
- 全集鏡頭規劃：`SH001–SH120`

## Agent Pipeline

1. **Director Agent**：讀取故事與 Shot Cards，控制鏡頭順序、節奏、戲劇意圖及敘事連續性。
2. **Character Agent**：依 Character Bible 維持角色外觀、服裝、年齡、道具與表演一致性。
3. **Environment Agent**：管理冰封新安市、九龍會、靈堂等場景的建築、氣候、光線與空間連續性。
4. **Prompt Agent**：為 Veo、Sora、Kling 產生結構化 Prompt Bundle。
5. **Video Agent**：執行生成任務，記錄模型、版本、種子、輸入資產與輸出結果。
6. **Assembly Agent**：將通過初審的鏡頭組裝為 Batch 初剪。
7. **QA Agent**：檢查角色一致性、場景連續性、畫質、時長、字幕、音訊及交付規格。

## 儲存庫結構

```text
docs/                  製片文件與工作規範
story/                 原作、改編稿、時間線與連續性資料
agents/                Agent 職責、輸入輸出契約與設定
prompts/               全域風格與模型提示詞套件
shots/SH001-SH120/     各鏡頭製作包
assets/characters/     角色參考圖與角色鎖定資料
assets/environments/   場景參考圖與環境鎖定資料
outputs/                預覽、QA 報告與交付清單
.github/workflows/     自動驗證與製片工作流
```

## Batch A｜SH001–SH030

執行順序：

1. 初始化 Director Agent。
2. 載入首批角色設定。
3. 載入冰封新安市、九龍會、靈堂環境包。
4. 生成 Veo／Sora／Kling Prompt Bundle。
5. 執行影片批次生成。
6. Assembly Agent 組裝 Batch A 初剪。
7. QA Agent 驗收；通過後進入 Batch B。

## 版權與來源管理

所有小說文本、圖片、音樂、影片、字型、模型與生成成果，均須記錄於資產登錄表。第三方素材僅能在具備授權、有效授權條款或其他可合理支持使用的法律基礎下納入專案。

## 版本

`v0.1.0 — Repository & Agent Pipeline Bootstrap`
