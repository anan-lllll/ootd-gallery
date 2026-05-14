# Q3 Air Summer V3 生图质量控制

## 当前主要问题

1. 颜色偏暗，夏季清爽和轻量感不足。  
2. 模特肤质过度平滑、塑料感、AI 感强。  
3. 模特情绪不真实，笑容或表情像生成图，不像真实 campaign。  
4. 上一张满意的 road trip 图不适合作为新参考图，因为它会继续污染色调和皮肤质感。  
5. 参考图如果包含清晰脸部，模型可能照搬模特脸。

## 核心修正策略

### 1. 不再用生成图作为主参考图

生成图可以用于“讨论方向”，但不要继续作为强参考输入。  
原因：
- 会继承 AI 皮肤、AI 光感和假情绪。
- 会把色调越带越脏、越暗。
- 会放大产品和手部的小错误。

后续参考优先级：

1. 原始真人 campaign / lifestyle 参考图
2. 洗脸后的参考图
3. 产品渲染图 / 实拍图
4. 生成图只作为低权重构图说明，不作为输入图

### 2. 色调要从“暖黄电影感”改成“清透日光”

不要再强调：
- warm cinematic
- golden hour
- dramatic sunlight
- moody summer
- deep contrast

这些词会让画面变暗、变油、变成熟过头。

改用：
- bright clean summer daylight
- airy high-key natural light
- soft open shade
- fresh morning or early afternoon sunlight
- low contrast, clear whites, breathable shadows
- crisp but gentle highlights

### 3. 皮肤要从“精修商业大片”改成“真实生活摄影”

不要再强调：
- flawless skin
- cinematic portrait
- beauty campaign
- glossy skin
- perfect model face

改用：
- realistic skin texture
- natural pores and subtle imperfections
- no plastic skin
- no over-smoothing
- documentary lifestyle photography
- candid expression, not posed smile

### 4. 情绪要从“笑得很漂亮”改成“真实动作中的自然状态”

更适合的动作：
- checking the route
- adjusting the bag strap
- reaching into the tote
- closing the car trunk
- walking through shade
- resting on park steps
- looking at the map, not posing for camera

不适合：
- holding phone beside face
- smiling directly at camera
- influencer selfie pose
- exaggerated happy laugh

---

## 全局追加提示词：清爽色调版

把这一段加到每条人物场景提示词里：

```text
Lighting and color grade: bright clean summer daylight, airy high-key natural light, soft open shade, clear whites, breathable shadows, low-to-medium contrast, fresh greens, pale sky blue, aqua teal, lime, citrus orange accents. The image should feel light, fresh, and breathable, not dark, moody, golden, or heavy.
```

## 全局追加提示词：真实肤质版

```text
Model rendering: realistic adult skin texture with natural pores and subtle imperfections, no plastic skin, no beauty filter, no over-smoothed face, no waxy AI skin. Natural candid expression, relaxed face, not a forced commercial smile, not an influencer pose.
```

## 全局负向词：避免 AI 感和暗色

```text
Avoid: dark color grade, moody contrast, heavy golden-hour orange cast, cinematic teal-orange grading, glossy plastic skin, waxy face, airbrushed beauty skin, over-smoothed skin, fake smile, influencer pose, stock-photo expression, uncanny eyes, overly perfect teeth, dramatic fashion editorial, copied reference face, visible brand logos, watermark, distorted hands, extra fingers.
```

---

## V3 Prompt 模板：人物场景通用版

```text
Create a premium photorealistic lifestyle image for Q3 Air Summer, a lightweight protective phone case for city-to-outdoor summer days.

Use the reference images only for wardrobe styling, composition, lighting direction, pose energy, and scene mood. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of any reference person. Create a new fictional adult model with a different face and different hairstyle.

Scene: [具体场景：city park steps / trailhead / car trunk / picnic blanket / cafe-to-park edge].

Subject: one adult model around 28-35 for a North American / European market, stylish but practical, with refined light outdoor / athleisure styling. Wardrobe should look designed and modern, not basic tourist wear: lightweight technical overshirt or camp shirt, ribbed tank or clean base layer, utility shorts, outdoor skirt, relaxed light pants, trail sneakers, small sling or crossbody bag, sunglasses or cap optional.

Action: the model is in a real movement moment, such as checking a route, adjusting a bag strap, reaching into a tote, closing the car trunk, or walking through shade. The phone is used naturally as part of the action, not posed beside the face.

Product direction: smartphone in a translucent summer protective phone case with aqua teal, lime, citrus orange, or pale blue accents. The case should feel lightweight, protective, fresh, and summer-ready, not black, bulky, or tactical.

Composition: premium website campaign photography, clean visual hierarchy, layered foreground and background, useful negative space, natural body language, not stock photography.

Lighting and color grade: bright clean summer daylight, airy high-key natural light, soft open shade, clear whites, breathable shadows, low-to-medium contrast, fresh greens, pale sky blue, aqua teal, lime, citrus orange accents. The image should feel light, fresh, and breathable, not dark, moody, golden, or heavy.

Model rendering: realistic adult skin texture with natural pores and subtle imperfections, no plastic skin, no beauty filter, no over-smoothed face, no waxy AI skin. Natural candid expression, relaxed face, not a forced commercial smile, not an influencer pose.

Avoid: dark color grade, moody contrast, heavy golden-hour orange cast, cinematic teal-orange grading, glossy plastic skin, waxy face, airbrushed beauty skin, over-smoothed skin, fake smile, influencer pose, stock-photo expression, uncanny eyes, overly perfect teeth, dramatic fashion editorial, copied reference face, visible brand logos, watermark, distorted hands, extra fingers.
```

---

## V3 首屏建议：不要用“手持手机特写”

首屏更适合以下构图：

### A. Open Trunk / Summer Pack Light

画面：打开后备箱，模特在整理包或拿水瓶，手机放在手里或车边，不用强行怼近。  
优点：有故事，有移动感，能承接你喜欢的 road trip 方向。  
注意：用清透早午光，不用金色傍晚光。

### B. Park Steps / Urban Outdoor

画面：城市公园台阶，模特坐着查路线或整理鞋带，手机在手边。  
优点：比咖啡店门口更有设计感，也更适合官网首屏留白。  
注意：台阶和树影形成几何构图，避免普通通勤街拍。

### C. Trailhead Prep / Before The Walk

画面：trailhead 前整理背包、看地图、拿水瓶。  
优点：轻户外表达明确，但不会硬核。  
注意：不要进入深林暗光，背景要明亮开阔。

---

## V3 参考图使用规则

### 人物参考图

使用前最好处理：
- 裁掉脸，只留身体、服装、姿态。
- 或给脸部轻微模糊。
- 或选择背影、侧身、墨镜遮挡的人物参考。

### 产品参考图

保持清晰：
- `手机壳渲染图.png`
- 产品实拍近景

产品图只负责结构和配色，不负责场景光线。

### 生成图

不建议作为输入参考。  
如果非要用，只能作为低权重构图参考，并且提示：

```text
Do not inherit the color grade, skin texture, face, or AI rendering style from the generated reference. Use it only as a loose composition reference.
```

---

## 可直接替换的 V3 Road Trip Prompt

```text
Create a premium website hero image for Q3 Air Summer, a lightweight protective phone case for summer city-to-outdoor movement.

Use the reference images only for wardrobe styling, composition, lighting direction, pose energy, and scene mood. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of any reference person. Create a new fictional adult model with a different face and different hairstyle.

Scene: a clean summer road trip departure moment near a city park or accessible trailhead. An open car trunk, canvas tote, water bottle, sunglasses, lightweight jacket, and soft greenery in the background. The setting feels real, fresh, and modern, not a luxury car ad.

Subject: one adult woman around 28-35 for a North American / European market. She is stylish but practical, wearing refined light outdoor / athleisure styling: lightweight technical overshirt or camp shirt, ribbed tank, relaxed utility shorts or light pants, trail sneakers, minimal jewelry, sunglasses. A friend can appear softly in the background only if it helps the story.

Action: she is naturally preparing to leave, checking the route, adjusting a tote, or picking up the phone from the trunk area. The phone is part of the action, not held beside the face.

Product direction: smartphone in a translucent summer protective phone case with aqua teal, lime, citrus orange, or pale blue accents, rounded protective bumper, and circular stand/magnetic detail. It should look lightweight, protective, fresh, and summer-ready.

Composition: wide horizontal website hero, clean negative space for copy, layered foreground objects, natural body language, premium product campaign framing, no stock-photo feeling.

Lighting and color grade: bright clean summer daylight, airy high-key natural light, soft open shade, clear whites, breathable shadows, low-to-medium contrast, fresh greens, pale sky blue, aqua teal, lime, citrus orange accents. The image should feel light, fresh, and breathable, not dark, moody, golden, or heavy.

Model rendering: realistic adult skin texture with natural pores and subtle imperfections, no plastic skin, no beauty filter, no over-smoothed face, no waxy AI skin. Natural candid expression, relaxed face, not a forced commercial smile, not an influencer pose.

Avoid: dark color grade, moody contrast, heavy golden-hour orange cast, cinematic teal-orange grading, glossy plastic skin, waxy face, airbrushed beauty skin, over-smoothed skin, fake smile, influencer pose, stock-photo expression, uncanny eyes, overly perfect teeth, luxury car ad, messy trunk, teenage styling, bikini, beach party, hard-core off-road adventure, black rugged phone case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

## 可直接替换的 V3 Weekend Trail Prompt

```text
Create a premium weekend trail lifestyle image for Q3 Air Summer phone case.

Use the reference images only for outdoor styling, composition, lighting direction, posture, and refined campaign mood. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of any reference person. Create a new fictional adult model with a different face and different hairstyle.

Scene: an accessible summer trailhead close to the city, with open shade, pale stone path, dry grass, trees, and bright sky peeking through. It should feel fresh and breathable, not dark forest or wilderness expedition.

Subject: one adult woman around 28-35 for a North American / European market. Outfit should be more designed than standard hiking: lightweight technical shell, sleeveless utility vest or camp shirt, clean base layer, modern trail shorts or outdoor skirt, trail sneakers, compact sling or small backpack, cap or sunglasses optional.

Action: she is checking a route, adjusting a bag strap, or pausing mid-walk with the phone in hand. The phone is used naturally, not held beside the face as a product pose.

Product direction: smartphone in a translucent summer protective phone case with aqua teal, lime, citrus orange, or pale blue accents. The case feels slim, fresh, protective, and summer-ready.

Composition: premium outdoor campaign photography, medium-wide or 4:5 crop, layered depth, model integrated with trail environment, clear but subtle phone visibility.

Lighting and color grade: bright clean summer daylight, airy high-key natural light, soft open shade, clear whites, breathable shadows, low-to-medium contrast, fresh greens, pale sky blue, aqua teal, lime, citrus orange accents. The image should feel light, fresh, and breathable, not dark, moody, golden, or heavy.

Model rendering: realistic adult skin texture with natural pores and subtle imperfections, no plastic skin, no beauty filter, no over-smoothed face, no waxy AI skin. Natural candid expression, relaxed face, not a forced commercial smile, not an influencer pose.

Avoid: dark forest, moody contrast, heavy golden-hour orange cast, glossy plastic skin, waxy face, airbrushed beauty skin, generic hiking catalog outfit, bulky hiking pants, heavy backpack, survival gear, extreme mountain summit, teenage styling, bikini, influencer selfie pose, black rugged phone case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```
