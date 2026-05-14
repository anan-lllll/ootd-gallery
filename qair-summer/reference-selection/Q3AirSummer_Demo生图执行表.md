# Q3 Air Summer Demo 生图执行表 v1

## 先修正 demo 问题

上一轮纯 prompt demo 的问题：

- 模特穿搭偏普通，缺少品牌 campaign 感。
- 构图像素材图库，不像官网主视觉。
- 人物状态不够“成年人轻行动”，有点土味户外/普通郊游。
- 产品和场景关系还可以，但审美没有跟上参考图。

这轮策略：

- 参考图主导审美，prompt 只负责方向和边界。
- 大场景先控人、穿搭、构图，不强求手机壳 100% 准。
- 产品功能近景再加入产品渲染/实拍作为强参考。
- 每张图最多 2-3 张参考，避免模型混乱。

---

## Demo 1：官网首屏调性大图

目标：首屏 hero，建立“城市到轻户外的夏日行动壳”气质。  
画面不要变成户外品牌大片，也不要像普通城市通勤图库。

### 输入图

| 角色 | 图片 |
|---|---|
| 人物穿搭/调性参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\SPRING-SUMMER 23 2.jpg` |
| 城市休闲构图参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\SPRING-SUMMER 23.jpg` |
| 产品色彩参考，可选 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |

### 最终生图提示词

```text
Create a premium website hero lifestyle image for Q3 Air Summer, a lightweight protective phone case for city-to-outdoor summer days.

Use the reference images mainly for styling, framing, model energy, and tasteful adult summer fashion. Do not copy the exact people or scene. Keep the visual mood elevated, modern, relaxed, and editorial, closer to a premium lifestyle campaign than a stock photo.

Scene: a sunny city edge that naturally connects to greenery, such as a coffee shop street corner near a park entrance, a clean sidewalk with trees, or a light urban leisure area.

Subject: one adult woman around 28-35 with a healthy, confident, natural presence. She wears refined summer casual / light outdoor styling: white or pale tank top, light overshirt or wind shirt, relaxed shorts or utility skirt, clean sneakers, small crossbody bag, sunglasses or cap optional. She is holding a smartphone naturally while walking or pausing before heading out.

Product direction: the phone should feel like it has a colorful translucent summer protective case, using aqua teal, lime, citrus orange, or pale blue accents. It should look lightweight, protective, and fresh, not black, not bulky, not tactical.

Composition: wide horizontal website hero, subject slightly off-center, clean negative space on one side for headline copy, layered depth, natural body language, no forced pose.

Lighting: bright summer daylight with soft shadows, fresh air, realistic skin tones, crisp but not harsh.

Color palette: white, aqua teal, citrus orange, soft lime, natural green, warm concrete.

Avoid: stock-photo smile, basic tourist outfit, teenage styling, bikini, glamorous beach party, overly cute dopamine styling, luxury fashion editorial, hard-core hiking gear, black rugged phone case, visible brand logos, fake phone UI text, watermark, distorted hands, extra fingers.
```

### 控制要点

- 核心看 **模特是否成熟、穿搭是否有设计感、画面是否能做首屏**。
- 手机壳不需要完全精准，但不能是黑壳或厚重户外壳。
- 如果画面又变土，下一轮加强：`more refined athleisure styling, premium Japanese/Korean lifestyle campaign, less generic outdoor wear`。
- 如果太时装，下一轮加强：`more practical everyday movement, less fashion editorial, more product campaign realism`。

---

## Demo 2：Weekend Trail 轻户外轮播

目标：证明它适合周末轻户外，但不进入专业登山/硬核装备。

### 输入图

| 角色 | 图片 |
|---|---|
| trail 穿搭/姿态参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\Joytrek Midlayer Grid Fleece Zip Neck - L SENIQ.png` |
| 户外质感/成年人状态参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\SS23 2.jpg` |
| 产品色彩参考，可选 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |

### 最终生图提示词

```text
Create a premium light-trail lifestyle image for a phone case website carousel.

Use the reference images for the level of styling, adult model energy, natural trail posture, and refined outdoor color control. Do not copy the exact face, outfit, or location.

Scene: an accessible weekend trailhead with trees, rocks, soft dirt path, and dappled summer sunlight. It should feel like a nearby weekend route, not a dramatic mountain expedition.

Subject: one adult woman around 28-35, relaxed and capable, wearing tasteful light outdoor / athleisure styling: fitted or clean technical top, light overshirt or wind layer, shorts or relaxed outdoor pants, cap optional, compact backpack. She is checking a route or taking a photo with a smartphone.

Product direction: the smartphone has a colorful translucent lightweight protective case with aqua teal, lime, citrus orange, or pale blue accents. It feels protective enough for trail movement, but slim and summer-ready.

Composition: vertical or 4:5 campaign crop, medium shot, trail texture visible, phone clearly in hand, model integrated into the environment, natural movement instead of posing.

Lighting: dappled natural sunlight, clear summer air, realistic skin tones, crisp details.

Color palette: forest green, aqua teal, soft lime, warm orange accent, off-white, natural stone.

Avoid: extreme mountaineering, helmet, climbing rope, heavy backpack, survival gear, muddy adventure race, teenage styling, bikini, influencer beach pose, generic catalog hiking look, black rugged phone case, visible brand logos, fake phone UI text, watermark, distorted hands, extra fingers.
```

### 控制要点

- 户外程度要刚好：像 **周末 trail / park hike**，不是高山徒步广告。
- 穿搭要轻机能、有审美，不要像普通速干衣淘宝图。
- 手机动作要真实：看地图、拍照、握持，不要硬举手机。

---

## Demo 3：Road Trip / 车载导航

目标：把手机变成“夏日移动工具”，自然带出磁吸、导航、路上使用。

### 输入图

| 角色 | 图片 |
|---|---|
| road trip 人物氛围参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\A weekend on Joshua Tree. For @Chase  @marriotthotels.jpg` |
| 成熟夏日社交/光线参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\5 tips to manage your blood sugar while dining out @Stelo赞助的 Pin 图.png` |
| 产品图，建议强参考 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |

### 最终生图提示词

```text
Create a premium summer road trip lifestyle image for a phone case website.

Use the reference images for adult energy, warm sunlight, casual outdoor-adjacent styling, and relaxed travel mood. Do not copy exact people, car, or location.

Scene: a parked car at a sunny trailhead or scenic roadside, open door or open trunk, water bottle, sunglasses, tote bag, lightweight jacket, clean practical travel objects. The setting should feel accessible and real, not luxury travel.

Subject: one or two adults around 28-35 preparing for a short weekend drive. One person is checking a smartphone for directions or placing it on a magnetic car mount.

Product direction: the phone has a colorful translucent summer protective case with aqua teal, lime, citrus orange, or pale blue accents. If a product reference is provided, follow its rounded bumper, translucent color, and ring-stand/magnetic detail as closely as possible.

Composition: close-to-medium lifestyle crop, phone and hand clearly visible, car and travel objects secondary, shallow depth of field, polished campaign framing.

Lighting: bright summer daylight, warm but clean, natural reflections, no harsh overexposure.

Color palette: sky blue, teal, citrus orange, lime, neutral car interior, warm road tones.

Avoid: luxury car ad, messy dashboard, teen road trip party, beach bikini, hard-core off-road adventure, black rugged phone case, fake navigation text, visible brand logos, watermark, distorted hands, extra fingers.
```

### 控制要点

- 不能像汽车广告，车只是场景，手机才是行动工具。
- 如果手机支架/磁吸不准，下一轮可以改成“手拿手机看导航”，再后期合成产品。
- 画面要有“出发前”的轻松，而不是旅行大片。

---

## Demo 4：Summer Social / 公园支架看内容

目标：自然带出支架功能，同时保留夏日社交和色彩。

### 输入图

| 角色 | 图片 |
|---|---|
| 公园社交构图参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\Summer Picnic Aesthetic 2.jpg` |
| 近景躺坐/自然互动参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\Summer Picnic Aesthetic.jpg` |
| 产品图，强参考 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |

### 最终生图提示词

```text
Create a premium lifestyle product image showing the built-in phone stand in a summer park social setting.

Use the reference images for relaxed adult park energy, candid interaction, sunny color, and natural composition. Do not copy exact people or pose.

Scene: city park lawn with picnic blanket, small snacks, water bottle, sunglasses, paperback book, tote bag, soft trees and distant city hints.

Subject: three adults around 26-35 relaxing on the blanket. A smartphone in a colorful translucent protective case is propped up with its ring stand so they can watch a video, take a video call, or frame a group shot. People are natural and secondary; the phone stand should be visually understandable.

Product direction: if product reference is provided, follow its translucent aqua-lime / coral-teal summer color language, rounded air-cushion bumper, and ring stand detail. The case should look premium, lightweight, protective, and fresh.

Composition: medium-wide lifestyle image with a clear foreground product moment. The phone and stand should be visible, but the image should still feel like a tasteful lifestyle campaign, not a catalog close-up.

Lighting: sunny afternoon, soft natural shadows, crisp details, warm social atmosphere.

Color palette: grass green, aqua teal, lime, citrus orange, white, pale blue.

Avoid: college party, teenage styling, exaggerated laughter, bikini, messy picnic clutter, overly cute dopamine props, fake phone UI text, visible brand logos, black rugged phone case, watermark, distorted hands, extra fingers.
```

### 控制要点

- 这张要重点看 **支架功能能不能自然成立**。
- 如果人物抢戏，就改成半近景，只保留手和身体局部。
- 如果产品形态不准，下一轮改用产品图做局部合成，不强求一次生成成功。

---

## Demo 5：产品握持 / 侧边防滑

目标：局部卖点图，体现轻量、防滑、侧边和按键细节。

### 输入图

| 角色 | 图片 |
|---|---|
| 产品实拍强参考 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳实拍图\20260509-164039.475-4.jpg` |
| 产品渲染强参考 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |
| 场景调性参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\Birkenstock Womens Boston Soft Footbed Suede Clog in Mocha, Womens at.jpg` |

### 最终生图提示词

```text
Create a premium close-up lifestyle product photo for the grip and side protection of Q3 Air Summer phone case.

Use the product reference images as the strongest reference for the phone case structure, translucent bumper, color, side button, grip texture, rounded air-cushion corner, and ring stand detail. Use the lifestyle reference only for relaxed summer styling and surface mood.

Scene: outdoor cafe bench or park-side table, subtle summer objects such as sunglasses, iced drink, tote strap, and soft greenery in the background.

Subject: an adult hand naturally holding the smartphone in the colorful translucent protective case. The side edge, colored button, grip texture, and corner bumper should be visible and sharp.

Style/medium: premium macro lifestyle product photography, realistic hand anatomy, tactile material detail, polished e-commerce quality.

Composition: close-up vertical or square crop, phone edge and hand dominate the frame, shallow depth of field, clean background.

Lighting: bright soft daylight, realistic reflections on translucent material, crisp edges.

Color palette: aqua teal, lime, citrus orange, pale blue, white, warm neutral.

Constraints: preserve the case design from reference as much as possible; no brand changes; no fake UI text; no black rugged case; no unrealistic bulky armor.
Avoid: distorted hand, extra fingers, warped phone, wrong ring stand shape, visible third-party logos, watermark, messy desk, cheap plastic look.
```

### 控制要点

- 这张产品准确性最重要，场景可以弱一点。
- 如果 AI 把支架或边框画错，改成“只露侧边和角落”的局部构图。
- 背景必须干净，否则会变成普通买家秀。

---

## 第一轮建议生成顺序

1. Demo 1：先看首屏审美能不能起来。
2. Demo 2：判断轻户外边界是否合适。
3. Demo 4：判断支架功能能不能自然融入生活场景。
4. Demo 5：如果前三张方向成立，再做产品近景校准。

## 总负向词库

```text
Avoid: stock-photo smile, basic tourist outfit, teenage look, bikini, swimsuit, glamorous beach party, luxury fashion editorial, extreme mountain climbing, survival gear, overly cute dopamine style, childish styling, heavy tactical gear, black rugged phone case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers, cheap catalog look, messy composition.
```
