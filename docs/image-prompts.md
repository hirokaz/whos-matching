# 画像生成プロンプト集

タイトル：マッチしたのは、誰？

---

## ■ 基本方針

- **フル顔は全フェーズ通じて見せない**（没入維持・絶対ルール）
  - 横顔・斜め・視線外し・手元・シルエット中心
  - `ui-spec.md`「前半:見せる／中盤:ぼかす／後半:見せない」の「見せる」もフル顔は対象外
- 実写風・自然光・日本の都市感
- 前半：暖かい / 後半：冷たい
- 過剰な演出NG（リアル重視）

---

## ■ 1. プロフィール画像（最重要）

### ■ 目的

「惹かれる相手」を作る

### ■ 使い分け

主人公の性別オプション（`character-spec.md` 参照）に応じて切り替える。

- 主人公が女性 → 男性プロンプトを使用（デフォルト）
- 主人公が男性 → 女性プロンプトを使用
- 同性パターン → 主人公と同性のプロンプトを使用

**いずれの場合もフル顔は避ける**（横顔・斜め・視線外し）。

---

### ■ プロンプト（男性）

```
Japanese man, late 20s to early 30s, clean and neat appearance, soft natural smile, business casual outfit, indoor natural light, shallow depth of field, slightly looking away from camera, calm and intelligent vibe, realistic photography, minimal background, high detail, face partially obscured or turned away
```

---

### ■ プロンプト（女性）

```
Japanese woman, late 20s to early 30s, natural makeup, soft gentle smile, casual elegant outfit, indoor natural light, slightly looking sideways, calm and approachable, realistic photography, shallow depth of field, minimal background, face partially obscured or turned away
```

---

### ■ NGワード

- dramatic lighting
- cinematic horror
- exaggerated emotion
- anime style
- direct frontal face shot（フル顔の正面ショット）

---

## ■ 2. カフェシーン（デート）

### ■ 目的

距離感・親密さ・安心感（恋愛モード）

### ■ 使用シーン

- **使用するシーン**: Chapter1 Scene5（初デート）専用
  - 時間帯：平日夜、退勤後
  - 場所：駅近くのカフェ
  - 目的：恋愛モード、安心感、親密さの演出
- **使用しないシーン**:
  - 朝の通勤シーン（Scene1〜2）
  - 社内シーン（Scene3）
  - 後半ホラーシーン（Chapter2）
  - 玄関以降（Scene10 以降）

`evening atmosphere` のプロンプトは初デートシーン専用であり、他のシーンには流用しない。

---

### ■ プロンプト

```
cozy cafe interior near a Tokyo train station in the evening after work, soft warm lighting, wooden table, two coffee cups, hands resting on table, shallow depth of field, blurred background, calm and intimate mood, realistic photography
```

---

### ■ バリエーション

- 窓際席（夜景あり）
- カップに手を添える
- ぼかし人物

---

### ■ 補足ルール

- 前半の恋愛演出では暖色
- 玄関に近づくほど寒色へ移行
- カフェ画像は「安心できるデート空間」としてのみ使用する

---

## ■ 3. メッセージ中の雰囲気カット

### ■ 目的

感情補強（直接見せない）

---

### ■ プロンプト

```
smartphone on table in cafe, chat screen glowing, dim lighting, warm tone, shallow depth of field, minimal composition, realistic
```

---

## ■ 4. 夜の移動シーン

### ■ 目的

違和感の入り口

---

### ■ プロンプト

```
quiet residential street in Tokyo at night, dim street lights, empty road, subtle shadows, cool color tone, realistic photography, minimal people, slightly eerie but still realistic
```

---

### ■ タクシー内

```
inside taxi at night, city lights blurred outside window, dark interior, reflection on glass, quiet atmosphere, realistic photography
```

---

## ■ 5. 住宅街（違和感強化）

### ■ 目的

安全→不安の移行

---

### ■ プロンプト

```
empty suburban street Japan night, low light, silent atmosphere, slightly cold color grading, no people, minimal composition, realistic photo
```

---

## ■ 6. 玄関（最重要）

### ■ 目的

恐怖の入り口

---

### ■ プロンプト

```
apartment entrance door in Japan at night, dim hallway light, door slightly open, dark interior beyond door, no visible room details, minimalistic, realistic photography, subtle eerie atmosphere
```

---

### ■ ポイント

- 中は見せない
- 暗さで隠す

---

## ■ 7. 後半（拘束後）

### ■ 方針

ほぼ見せない、抽象化

---

### ■ プロンプト（壁）

```
dark room wall with scattered photos, photos barely visible, low light, high contrast shadows, unsettling atmosphere, realistic texture
```

---

### ■ プロンプト（視界ぼやけ）

```
blurred vision perspective, dark room, vague shapes, low clarity, realistic distortion, subtle noise
```

---

## ■ 8. 写真（監視の証拠）

### ■ 目的

恐怖の確定

---

### ■ プロンプト

```
printed photos scattered on wall, candid street photos of a person walking, taken from distance, slightly grainy, surveillance-like but realistic, not exaggerated
```

---

### ■ 注意

- 明確な犯罪描写NG
- あくまで「気持ち悪さ」

---

## ■ 9. TVニュース

### ■ 目的

伏線回収

---

### ■ プロンプト

```
television screen in dark room, news broadcast, Japanese news style, blurred text, serious tone, dim lighting, realistic
```

---

## ■ 10. 抽象演出（後半）

### ■ プロンプト

```
dark abstract background, subtle noise texture, low light, minimal visual information, unsettling but not explicit, realistic texture
```

---

## ■ カラールール

| フェーズ | 色                             |
| ---- | ----------------------------- |
| 前半   | 暖色（オレンジ・ベージュ）                 |
| 中盤   | 中間（白〜グレー）                     |
| 後半   | 寒色（青・黒）                       |

---

## ■ 共通ネガティブプロンプト

```
anime, illustration, cartoon, exaggerated lighting, horror monster, gore, blood, extreme expression, fantasy, unrealistic
```

---

## ■ Claudeへの指示

- 各シーンに対応した画像を使用
- 画像は背景・雰囲気補強として使用
- キャラクターは直接見せすぎない
- 恐怖は視覚ではなく認知で作る

---

## ■ 最重要ルール

「見せないことで想像させる」
