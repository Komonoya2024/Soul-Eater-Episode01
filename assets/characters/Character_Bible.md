# 《噬魂者》Character Bible｜P1

Version: 1.0  
Status: Production Canon  
Project: `Soul-Eater-Episode01`

## 目的

本文件為《噬魂者》主要角色的唯一視覺基準。Director、Character、Prompt、Video 與 QA Agent 均須以此文件及各角色資產資料夾為準，禁止在未經核准情況下自行改動角色年齡、臉型、身高、髮型、服裝、配件或陣營識別。

## 核心角色索引

| ID | 角色 | 劇情職能 | 狀態 |
|---|---|---|---|
| CHAR-001 | 聶宇 | 主角／潛入調查 | 已建立完整 P1.1 規格 |
| CHAR-002 | 趙杰 | 警方搭檔／融合共存人格 | 已建立角色卡 |
| CHAR-003 | 崔震海 | 九龍會會長／命案核心 | 已建立角色卡 |
| CHAR-004 | 宋世彰 | 九龍會副會長／靈堂壓迫者 | 已建立角色卡 |
| CHAR-005 | 辛思遠 | 意識融合權威／後期核心人物 | 已建立角色卡 |

## 全域視覺規格

- 時代：2055 年
- 地域：近未來東亞城市新安市
- 類型：科幻／犯罪／懸疑／動作
- 視覺：電影級寫實、Neo-Noir、冷青灰、深黑
- 攝影：ARRI Alexa 35、Cooke S4/i 質感
- 渲染：UE5 photorealistic、HDR global illumination
- 解析度：8K Master
- 禁止：動漫臉、明星臉、過度磨皮、年齡漂移、體型漂移、髮型漂移、服裝跳接

## 角色資產標準

每位主要角色至少具備：

1. `Character_Card.md`
2. `Face_Reference.md`
3. `Turnaround.md`
4. `Costume_Bible.md`
5. `Expression_Library.md`
6. `Pose_Library.md`
7. `Prompt_Library.md`
8. `QA_Checklist.md`

## Continuity ID 規則

```text
CHAR-XXX
CHAR-XXX-C01  # Costume
CHAR-XXX-E01  # Expression
CHAR-XXX-P01  # Pose
CHAR-XXX-FACE-APPROVED-v001
CHAR-XXX-MASTER-APPROVED-v001
```

## 變更控制

- 任何外觀修改須新增版本，不可覆蓋已核准 Master。
- 改動臉部、身高、年齡或核心配件，需經 Director Agent 與 QA Agent 雙重核准。
- Shot Prompt 必須明確引用 Character ID、Costume ID、Expression ID 與 Pose ID。
- 多角色鏡頭須執行臉部互換檢查與身高比例檢查。
