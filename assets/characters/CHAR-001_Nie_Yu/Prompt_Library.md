# CHAR-001｜Prompt Library

## Global Style

```text
ultra-realistic cinematic near-future East Asian science-fiction crime thriller,
New An City in 2055,
grounded human anatomy,
realistic skin pores and age details,
subtle facial asymmetry,
neo-noir atmosphere,
cold blue-gray palette,
deep blacks,
HDR global illumination,
cinematic volumetric lighting,
ARRI Alexa 35,
Cooke S4/i lens character,
Unreal Engine 5 photorealistic rendering,
8K production concept art,
consistent face identity,
no celebrity likeness
```

## Character Lock

```text
CHAR-001 Nie Yu,
32-year-old East Asian male undercover investigator,
181 cm, lean athletic build,
narrow angular face, defined jawline,
short black hair with closely trimmed sides,
deep brown eyes,
faint scar near the end of his left eyebrow,
subtle under-eye fatigue,
restrained and highly observant expression,
controlled body language,
alert stance
```

## Main Visual Prompt

```text
full-body front-facing production character key art of CHAR-001 Nie Yu,
wearing CHAR-001-C02 charcoal-black fitted single-breasted suit,
white plain shirt, narrow black tie,
matte black AR smart glasses,
black Oxford shoes,
concealed right-side waist holster,
neutral controlled posture,
cold blue-gray studio environment,
soft frontal key light and subtle cool rim light,
realistic East Asian facial anatomy,
85mm portrait character for face, 50mm full-body perspective,
clean production reference composition,
no text, no logo, no watermark
```

## Turnaround Prompt

```text
professional six-view character turnaround sheet of the exact same CHAR-001 Nie Yu,
front, left profile, back, right profile, left three-quarter, right three-quarter,
identical neutral standing posture,
identical facial identity, body proportions, hairstyle and costume,
CHAR-001-C02 costume,
plain neutral gray background,
flat soft production lighting,
minimal lens distortion,
full body visible from head to shoes,
no labels, no text, no watermark
```

## Face Reference Prompt

```text
passport-style cinematic face reference of the exact same CHAR-001 Nie Yu,
head and shoulders,
neutral expression,
no AR glasses for identity calibration,
short black hair,
deep brown eyes,
faint scar near left eyebrow tail,
subtle under-eye fatigue,
realistic pores and natural skin texture,
85mm lens,
neutral gray background,
soft symmetrical lighting,
no beauty filter,
no celebrity likeness
```

## Negative Prompt

```text
anime, manga, cartoon, stylized illustration,
celebrity likeness, famous actor,
plastic skin, excessive beauty filter,
overly smooth face, de-aged face,
incorrect age, inconsistent facial identity,
different hairstyle, different eye color,
beard, long hair, military buzz cut,
bodybuilder physique, fashion model pose,
extra fingers, malformed hands,
duplicate limbs, distorted anatomy,
fantasy armor, excessive cyberpunk neon,
visible brand logo, text, watermark
```

## Model Notes

- Veo／Sora／Kling：以已核准主視覺作為角色 reference image。
- 圖像模型：先生成無墨鏡 Face Reference，再生成佩戴墨鏡版本。
- 每輪候選至少生成 4 張，僅保留通過 QA 的版本。
- 所有後續 Shot Prompt 必須包含 `CHAR-001`、Costume ID、Expression ID、Pose ID。
