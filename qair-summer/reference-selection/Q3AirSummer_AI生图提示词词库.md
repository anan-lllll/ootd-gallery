# Q3 Air Summer AI 生图提示词词库 v1

## 总方向

核心视觉关键词：城市轻行动、夏日出门、轻户外边缘、成年人、清爽机能、随身装备、真实使用手机。

不要生成：海边辣妹、泳装、校园少女、夸张多巴胺、硬核登山、极限运动、过度时装大片、明显网红摆拍、手机壳功能看不出来的纯氛围图。

建议先分两种生成方式：

- 场景氛围图：先生成没有具体手机壳特写的人物/场景，后期再合成产品。
- 产品使用图：需要使用手机壳实拍或渲染图作为参考图，再做“人物拿手机/车载/支架”的合成，否则模型容易把壳子画错。

通用负向约束可追加在每条提示词末尾：

```text
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

---

## 01 官网首屏调性大图

用途：官网首屏 hero，建立“夏天出门版 Air 壳”的气质。  
画面重点：成年人、夏日、城市到轻户外、轻装上阵、留出页面文案空间。

### Prompt A：城市到公园的夏日移动

```text
Use case: ads-marketing
Asset type: website hero image for a premium phone case landing page
Primary request: A photorealistic summer lifestyle hero image for a lightweight protective phone case made for city-to-outdoor days.
Scene/backdrop: a sunny city park edge near a coffee shop and bike path, warm late-morning light, trees, clean sidewalks, soft summer shadows.
Subject: a stylish adult woman around 30, healthy and relaxed, wearing a white tank top, light overshirt, casual shorts, sneakers, crossbody bag, holding a modern smartphone naturally while walking from the city street toward the park.
Style/medium: premium commercial lifestyle photography, natural and candid, not fashion editorial.
Composition/framing: wide horizontal composition, subject slightly right of center, clean negative space on the left for website copy, subtle sense of movement.
Lighting/mood: bright, airy, optimistic, fresh summer energy, realistic skin tones.
Color palette: aqua teal, citrus orange, soft lime, white, warm concrete, natural green.
Constraints: adult model, realistic everyday movement, phone visible but not an extreme close-up, no swimsuit, no teen styling, no heavy outdoor gear.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### Prompt B：短途出发前的车边场景

```text
Use case: ads-marketing
Asset type: website hero image for a summer phone case campaign
Primary request: A premium lifestyle scene showing a light summer road trip moment before departure.
Scene/backdrop: open car trunk near a sunny trailhead parking area, canvas tote, water bottle, sunglasses, lightweight jacket, soft trees in the background.
Subject: two adults around 28-35 preparing for a short weekend outing, one person checking a smartphone for directions, relaxed and practical, not posing dramatically.
Style/medium: photorealistic commercial lifestyle photography with real textures and natural expressions.
Composition/framing: wide horizontal frame, product-use moment in the foreground, enough clean sky or soft background space for website headline.
Lighting/mood: clear summer daylight, fresh, mobile, ready-to-go.
Color palette: teal, lime, warm orange accents, pale blue sky, neutral clothing.
Constraints: adult lifestyle, light outdoor, phone used as a navigation tool, no extreme sports, no luxury car focus.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

---

## 02 模特场景轮播

用途：页面中段人物轮播，支撑“不同夏日移动场景都适用”。  
建议 4 张：通勤、公园/社交、road trip、轻 trail。

### Prompt C：City Commute

```text
Use case: photorealistic-natural
Asset type: website carousel lifestyle image
Primary request: A realistic city commute lifestyle scene for a summer phone case landing page.
Scene/backdrop: bright city sidewalk outside a small coffee shop, morning commute, tote bag, iced coffee, light street greenery.
Subject: an adult professional woman around 30 holding a smartphone in one hand and coffee in the other, wearing clean summer casual clothes, calm and capable.
Style/medium: candid premium lifestyle photography, natural pose, no exaggerated fashion styling.
Composition/framing: medium shot, phone hand visible, enough environmental context to show city daily movement.
Lighting/mood: soft morning sun, fresh, clear, lightweight.
Color palette: white, teal, lime, warm orange detail, neutral beige, natural green.
Constraints: adult, grounded, everyday, no office suit stiffness, no teenage styling.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### Prompt D：Summer Social / Park Picnic

```text
Use case: photorealistic-natural
Asset type: website carousel lifestyle image
Primary request: Adults relaxing in a city park on a summer weekend, using a smartphone with a stand to share content.
Scene/backdrop: green city park lawn, picnic blanket, small snacks, water bottles, sunglasses, soft trees, urban buildings faintly visible in the distance.
Subject: three adults around 26-35 sitting casually, one phone propped up on a small stand angle as they watch or video call, relaxed laughter, natural interaction.
Style/medium: premium candid lifestyle photography, warm but not sentimental.
Composition/framing: medium-wide shot, phone visible in the foreground or center, people form a natural triangle around it.
Lighting/mood: sunny afternoon, friendly, light, social, authentic.
Color palette: summer green, white, aqua teal, citrus orange, soft yellow.
Constraints: adult friend group, not college-party energy, phone stand use should be understandable.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### Prompt E：Road Trip / Navigation

```text
Use case: photorealistic-natural
Asset type: website carousel lifestyle image
Primary request: A realistic summer road trip moment showing a smartphone used for navigation.
Scene/backdrop: car interior or open driver-side door near a scenic but accessible roadside, sunlight, water bottle, sunglasses, lightweight backpack.
Subject: an adult around 30 placing or checking a smartphone on a magnetic car mount, preparing for a short weekend drive.
Style/medium: realistic commercial lifestyle photography, practical and polished.
Composition/framing: close-to-medium shot, hand and phone mount visible, background softly blurred, no distracting dashboard clutter.
Lighting/mood: bright daylight, ready, efficient, mobile.
Color palette: black dashboard as small accent, teal, lime, orange, sky blue, warm neutrals.
Constraints: show phone as a tool for movement; avoid making the car the hero.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### Prompt F：Weekend Trail

```text
Use case: photorealistic-natural
Asset type: website carousel lifestyle image
Primary request: A light trail lifestyle scene for adults who enjoy easy weekend outdoor movement.
Scene/backdrop: accessible trailhead with trees, rocks, and soft sunlight, not a dramatic mountain summit.
Subject: an adult woman around 30 in light hiking clothes, cap, small backpack, holding a smartphone while checking the route or taking a photo.
Style/medium: natural outdoor lifestyle photography, realistic and approachable.
Composition/framing: medium shot with trail texture visible, phone in hand, relaxed posture.
Lighting/mood: dappled sunlight, fresh air, quiet confidence, summer.
Color palette: forest green, aqua teal, lime, warm orange accent, off-white.
Constraints: light outdoor, not professional expedition, no heavy gear, no extreme pose.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

---

## 03 产品使用近景

用途：支架、磁吸、侧边防滑、握持这些局部功能场景。  
注意：如果要准确呈现 Q3 Air Summer 手机壳，建议把产品实拍/渲染图作为参考图一起输入。

### Prompt G：支架看内容

```text
Use case: product-mockup
Asset type: website feature image for phone case stand function
Primary request: A close lifestyle product scene showing a colorful summer protective phone case using its built-in ring stand on a picnic blanket.
Scene/backdrop: city park picnic blanket, sunlight, water bottle, sunglasses, paperback book, soft grass blur.
Subject: a smartphone in a translucent aqua-lime or coral-teal protective case, propped up by a clean metal ring stand, with adult hands nearby reaching for snacks.
Style/medium: photorealistic product lifestyle photography, premium e-commerce quality.
Composition/framing: close-up three-quarter angle, phone and stand are the hero, background lifestyle elements secondary.
Lighting/mood: bright natural summer sunlight, crisp details, relaxed.
Color palette: aqua teal, lime, citrus orange, soft white, grass green.
Constraints: the stand must look stable and useful, no fake UI text, no oversized phone, no distorted product geometry.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### Prompt H：单手握持 / 防滑侧边

```text
Use case: product-mockup
Asset type: website feature image for grip and side protection
Primary request: A close-up product lifestyle photo showing a hand securely holding a colorful translucent summer protective phone case.
Scene/backdrop: outdoor cafe table with iced coffee, sunglasses, tote strap, soft greenery in the background.
Subject: adult hand holding a modern smartphone in a translucent teal-lime or coral-blue protective case, side grip texture and colored button details visible.
Style/medium: premium macro lifestyle product photography, realistic hand and product texture.
Composition/framing: close-up vertical crop, side edge and corner protection clearly visible, natural hand position.
Lighting/mood: bright but soft daylight, clean, tactile, trustworthy.
Color palette: teal, lime, coral orange, white, warm wood or concrete.
Constraints: realistic hand anatomy, phone case should feel lightweight but protective, no exaggerated rugged armor.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### Prompt I：磁吸充电 / 桌面出门前

```text
Use case: product-mockup
Asset type: website feature image for MagSafe convenience
Primary request: A premium lifestyle product scene showing a summer phone case magnetically charging before going out.
Scene/backdrop: clean entryway table or cafe table, tote bag, keys, sunglasses, water bottle, lightweight jacket partially visible.
Subject: smartphone in a translucent colorful protective case attached to a magnetic wireless charger, ready to be picked up for a summer day out.
Style/medium: photorealistic e-commerce lifestyle photography, clean and polished.
Composition/framing: close-up with product centered, surrounding objects create an out-the-door story.
Lighting/mood: fresh morning light, organized, ready, lightweight.
Color palette: aqua teal, lime, citrus orange, neutral white, light wood.
Constraints: no fake charging text, no brand logos, magnetic connection should be visually clear.
Avoid: teenage look, bikini, glamorous beach party, luxury fashion editorial, extreme mountain climbing, overly cute dopamine style, childish styling, heavy tactical gear, black rugged case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

---

## 04 技术结构/气囊动画参考帧

用途：气囊结构动画的概念帧，可给 3D/动效参考。  
建议这里不要生成人物，用干净产品技术视觉。

### Prompt J：气囊结构透明剖面

```text
Use case: infographic-diagram
Asset type: website technical feature visual
Primary request: A clean premium 3D technical visualization of a translucent phone case corner air cushion structure.
Scene/backdrop: minimal light background, no environment clutter.
Subject: enlarged phone case corner with transparent teal outer bumper, inner air cushion channels, subtle compression arrows, layered protective structure.
Style/medium: high-end 3D product render, technical but elegant, not medical or industrial.
Composition/framing: close-up macro cutaway angle, corner protection is the hero, plenty of clean space.
Lighting/mood: crisp studio lighting, precise, trustworthy, lightweight.
Color palette: translucent teal, lime glow, soft gray, white, small orange accent.
Text (verbatim): no text.
Constraints: no labels unless added later by design, no messy exploded parts, no unrealistic machinery.
Avoid: black rugged case, heavy tactical style, fake logo, watermark, cluttered diagram, unreadable text, distorted geometry.
```

### Prompt K：多色气囊结构动效帧

```text
Use case: product-mockup
Asset type: animation key visual frame for website product detail
Primary request: A premium 3D render showing two colorful translucent phone case corners with air cushion structures, suggesting impact absorption and rebound.
Scene/backdrop: clean white-to-light-gray studio background.
Subject: two case corners, one aqua-lime and one coral-blue, with subtle transparent layers and soft motion trails showing impact energy dispersing through the corner.
Style/medium: high-end 3D product render, polished website visual.
Composition/framing: diagonal dynamic composition, corners large enough to show structure, not cluttered.
Lighting/mood: clean, technical, energetic, modern.
Color palette: aqua teal, lime, coral orange, sky blue, white.
Text (verbatim): no text.
Constraints: premium and lightweight, not sci-fi armor, no excessive glow.
Avoid: black rugged case, heavy tactical style, fake logo, watermark, cluttered diagram, unreadable text, distorted geometry.
```

---

## 05 色彩理念视觉

用途：个性配色设计理念段落。  
重点：颜色来自夏天的光、水、路、装备，而不是甜美少女。

### Prompt L：两款配色的夏日地貌静物

```text
Use case: ads-marketing
Asset type: website color story visual
Primary request: A premium still-life composition expressing two summer phone case colorways inspired by coastal light and trail energy.
Scene/backdrop: clean sunlit surface with natural shadows, hints of water reflection, trail map paper, sunglasses, small carabiner, citrus slice, smooth stone.
Subject: abstract color story objects arranged around two empty phone-case-shaped color blocks or translucent material swatches, one aqua-lime, one coral-blue.
Style/medium: editorial product still life photography, sophisticated and fresh.
Composition/framing: top-down or low three-quarter angle, clean spacing, suitable for a website design section.
Lighting/mood: bright summer light, crisp, airy, tactile.
Color palette: aqua teal, lime, coral orange, pale blue, white, warm sand.
Constraints: no childish props, no beach party props, no fake brand logos, no text.
Avoid: candy-like dopamine overload, teenage styling, luxury jewelry styling, heavy camping gear, clutter, watermark.
```

---

## 06 首轮 demo 建议

建议先生成这 3 张，用来校准方向：

1. Prompt A：官网首屏，检验整体调性是否成熟、清爽、轻行动。
2. Prompt F：轻 trail，检验户外程度是否刚好，不硬核。
3. Prompt G：支架看内容，检验功能场景是否能自然带出产品。

第一轮不要急着追求手机壳 100% 准确，先看人物年龄、场景、光线、情绪是否对。第二轮再引入产品渲染图做合成或局部产品图。
