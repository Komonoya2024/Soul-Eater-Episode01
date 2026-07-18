# CHAR-001 Image Generation Batch A

Batch ID: `CHAR-001-IMG-BATCH-A`  
Status: `READY_FOR_GENERATION`  
Target Master: `CHAR-001_APPROVED_MASTER_v001`

## 執行順序

1. 無墨鏡正面臉部校驗圖
2. 戴 AR 墨鏡正面主視覺
3. 六視角 Turnaround Sheet
4. C01／C02／C03 服裝組
5. NY-E01～NY-E08 表情組
6. QA 篩選並鎖定 Master

## Stage 01｜Face Calibration

輸出：

```text
CHAR-001_FACE_FRONT_NEUTRAL_CANDIDATE_01.png
CHAR-001_FACE_FRONT_NEUTRAL_CANDIDATE_02.png
CHAR-001_FACE_FRONT_NEUTRAL_CANDIDATE_03.png
CHAR-001_FACE_FRONT_NEUTRAL_CANDIDATE_04.png
```

規則：

- 無 AR 墨鏡
- 85mm portrait lens
- 中性灰背景
- 對稱柔光
- 中性表情
- 相同視覺年齡與臉部比例

核准輸出：

```text
CHAR-001_FACE_APPROVED_v001.png
```

## Stage 02｜Main Visual

輸出：

```text
CHAR-001_MAIN_C02_AR_CANDIDATE_01.png
CHAR-001_MAIN_C02_AR_CANDIDATE_02.png
CHAR-001_MAIN_C02_AR_CANDIDATE_03.png
CHAR-001_MAIN_C02_AR_CANDIDATE_04.png
```

規則：

- 必須引用 `CHAR-001_FACE_APPROVED_v001`
- 服裝：`CHAR-001-C02`
- AR 墨鏡：佩戴
- 姿態：中性警戒
- 全身或四分之三身

## Stage 03｜Turnaround

輸出：

```text
CHAR-001_TURN_FRONT_v001.png
CHAR-001_TURN_LEFT_v001.png
CHAR-001_TURN_BACK_v001.png
CHAR-001_TURN_RIGHT_v001.png
CHAR-001_TURN_45L_v001.png
CHAR-001_TURN_45R_v001.png
```

要求：相同臉部、髮型、身高比例、服裝、鞋款與 AR 墨鏡。

## Stage 04｜Costume Set

### C01

```text
CHAR-001_COSTUME_C01_FRONT_v001.png
CHAR-001_COSTUME_C01_45L_v001.png
CHAR-001_COSTUME_C01_BACK_v001.png
```

### C02

```text
CHAR-001_COSTUME_C02_FRONT_v001.png
CHAR-001_COSTUME_C02_45L_v001.png
CHAR-001_COSTUME_C02_BACK_v001.png
```

### C03

```text
CHAR-001_COSTUME_C03_FRONT_v001.png
CHAR-001_COSTUME_C03_45L_v001.png
CHAR-001_COSTUME_C03_BACK_v001.png
```

## Stage 05｜Expression Set

```text
CHAR-001_EXPR_NY-E01_v001.png
CHAR-001_EXPR_NY-E02_v001.png
CHAR-001_EXPR_NY-E03_v001.png
CHAR-001_EXPR_NY-E04_v001.png
CHAR-001_EXPR_NY-E05_v001.png
CHAR-001_EXPR_NY-E06_v001.png
CHAR-001_EXPR_NY-E07_v001.png
CHAR-001_EXPR_NY-E08_v001.png
```

所有表情先生成無墨鏡版本，核准後再建立佩戴 AR 墨鏡版本。

## Stage 06｜Master Lock

通過 QA 後，建立：

```text
approved/CHAR-001_APPROVED_MASTER_v001.png
approved/CHAR-001_APPROVED_MASTER_v001.json
```

JSON 必須記錄：

- Character ID
- Candidate source
- Generator / Model
- Model version
- Seed
- Face reference
- Costume ID
- Approval date
- Reviewer
- SHA-256 checksum

## Gate

只有在 `QA_Checklist.md` 全部通過後，Batch 狀態才能由 `READY_FOR_GENERATION` 改為 `APPROVED`。
