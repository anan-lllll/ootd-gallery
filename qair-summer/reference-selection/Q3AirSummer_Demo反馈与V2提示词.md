# Q3 Air Summer Demo 反馈与 V2 生图策略

## 这轮 demo 结论

### Demo 1 官网首屏

问题：
- 场景成立，但太像普通通勤图库，缺少官网主视觉的张力。
- 穿搭是“白衬衫 + 背心 + 短裤”的安全组合，但没有设计感，容易显土。
- 手机壳被展示得太直白，画面像“模特拿壳”，不是“品牌 campaign”。
- 亚洲模特版本更干净，是因为模型把清爽、年轻、精致感拉上来了，但目标市场不是亚洲，所以不能靠亚洲脸解决审美问题。

修正方向：
- 首屏不要再拍“站在咖啡店门口拿手机”。
- 改成更有叙事的夏日出门瞬间：open trunk、城市公园台阶、trailhead 前的整理装备、骑行/步行过渡场景。
- 模特可以是欧美市场，但需要更有造型：现代 athleisure、轻机能、干净层次、颜色呼应产品。
- 构图要像官网主视觉：远一点、更有空间关系、更强色块，不要胸口以上拿手机特写。

### Demo 2 Weekend Trail

问题：
- 画面勉强可用，但像常规 hiking 广告。
- 服装和姿态仍然偏普通户外，不够设计感。
- 手机壳出现得太“展示”，不是自然使用。

修正方向：
- 往 “designer outdoor / styled trail / light technical fashion” 收。
- 减少传统 hiking 元素，比如硬帽、厚裤、厚背包。
- 增加更有调性的服装层次：tech vest、light shell、utility skirt/shorts、trail sneaker、cap/sunglasses。

### Demo 3 Road Trip

成功点：
- 有真实生活事件：准备出发、后备箱、朋友、导航。
- 光线高级，有夏天和移动感。
- 穿搭自然但不土。
- 产品出现得合理，不像硬摆拍。

这张可以作为后续 demo 的基准：其他场景都要有类似的“行动前后关系”，不要只有模特拿手机。

---

## 解决参考图脸部照搬的方法

### 最推荐

参考图只用来控制：
- 服装层次
- 光线
- 构图
- 场景关系
- 人物姿态

不要用来控制：
- 脸
- 发型
- 五官
- 具体身份

### Prompt 里必须加入

```text
Use the reference images only for wardrobe styling, composition, lighting, pose energy, and scene mood. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of any reference person. Create a new fictional adult model with a different face and different hairstyle.
```

### 参考图处理建议

如果模型仍然照搬脸，可以做三种处理：

1. **提前洗图**：把参考图脸部轻微模糊或裁掉，只保留穿搭和姿态。
2. **用背影/侧脸/墨镜图做参考**：首屏和户外图可以多用侧脸、背影、低脸部信息。
3. **拆参考**：人物穿搭参考用无脸/远景图，场景参考用空景或群像，产品参考单独给。

不建议把一张清晰人脸参考图作为主参考直接喂给生图，否则模型很容易把脸当作需要保留的主体。

---

## V2 Demo 1A：官网首屏，Road Trip Hero 方向

这个方向更接近目前最满意的 Demo 3，适合作为官网首屏。  
核心：用“准备出发”代替“站着拿手机”，画面更有故事和高级感。

### 输入图

| 角色 | 图片 |
|---|---|
| 成功画面基准 | `C:\Users\Administrator\Downloads\ChatGPT Image 2026年5月9日 18_30_59.png` |
| road trip 氛围参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\A weekend on Joshua Tree. For @Chase  @marriotthotels.jpg` |
| 产品参考 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |

### 提示词

```text
Create a premium website hero image for Q3 Air Summer, a lightweight protective phone case for summer city-to-outdoor movement.

Use the reference images only for wardrobe styling, composition, lighting, pose energy, and scene mood. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of any reference person. Create a new fictional adult model with a different face and different hairstyle.

Scene: a refined summer road trip departure moment at the edge of a city park or trailhead parking area. An open car trunk, tote bag, water bottle, sunglasses, lightweight jacket, and soft landscape in the background. The scene feels accessible, modern, and real, not a luxury car ad.

Subject: one adult woman around 28-35 for a North American / European market, confident and relaxed, with refined summer outdoor-adjacent styling. Outfit should feel designed and premium: lightweight overshirt or technical camp shirt, fitted tank or ribbed top, relaxed utility shorts or clean light pants, minimal jewelry, sunglasses, trail sneakers or casual outdoor shoes. A second adult friend can appear softly in the background if it helps the story.

Product: she naturally checks a smartphone in a colorful translucent Q3 Air Summer-style protective case. The case should have aqua teal, lime, citrus orange, or pale blue accents, a rounded protective bumper, and a visible circular stand/magnetic detail. The phone is part of the action, not a forced product pose.

Composition: wide horizontal website hero, cinematic but clean, subject placed on one side, open space for headline copy on the other side, layered foreground objects, shallow depth of field, strong sunlight and natural shadows. The image should feel like a premium lifestyle campaign, not stock photography.

Lighting: warm late-afternoon summer light, realistic highlights, natural skin tones, crisp but soft.

Color palette: sun-washed neutrals, aqua teal, lime, citrus orange accents, pale blue sky, natural green.

Avoid: copying reference faces, generic stock-photo smile, basic tourist outfit, cheap hiking outfit, teenage styling, bikini, beach party, luxury fashion editorial, extreme mountain climbing, hard-core off-road adventure, black rugged phone case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### 控制要点

- 首屏优先级：高级感 > 产品大特写。
- 人物可以不看镜头，最好在真实动作中。
- 服装要有层次和材质，不要白衬衫背心短裤的默认组合。

---

## V2 Demo 1B：官网首屏，Urban Outdoor Steps 方向

如果不想首屏用车，可以改成城市与公园的过渡场景，但要避开咖啡店门口图库感。

### 输入图

| 角色 | 图片 |
|---|---|
| 穿搭/构图参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\SPRING-SUMMER 23 2.jpg` |
| 城市户外过渡参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\VANS @Feature All Things Good.png` |
| 产品参考 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |

### 提示词

```text
Create a premium website hero image for a summer lightweight protective phone case, positioned between city life and light outdoor movement.

Use the reference images only for styling language, body posture, composition, color energy, and campaign mood. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of any reference person. Create a new fictional adult model with a different face and different hairstyle.

Scene: modern city park steps or a clean urban plaza that opens into greenery, with sunlight, concrete, trees, and a hint of city architecture. No coffee shop storefront focus.

Subject: one adult woman around 28-35 for a North American / European market, stylish but practical. She is sitting or leaning on broad park steps while checking her smartphone before heading out. Outfit should be refined light outdoor / athleisure: sculptural tank, lightweight nylon overshirt or vest, utility shorts or relaxed cargo skirt, technical sneakers, small crossbody or sling bag, sunglasses.

Product: smartphone in a translucent summer protective case with aqua teal, lime, citrus orange, or pale blue accents. It should feel like a lightweight protective case with rounded corners and a circular stand/magnetic detail.

Composition: wide horizontal hero, editorial campaign framing, strong negative space for copy, layered geometry from steps and greenery, relaxed posture, not a close product pose.

Lighting: bright summer sun with graphic shadows, clear air, premium commercial photography.

Color palette: clean concrete, natural green, white, aqua teal, lime, citrus orange.

Avoid: copying reference faces, plain white shirt and basic shorts outfit, stock-photo commute look, teenage styling, bikini, beach party, overly cute dopamine props, luxury runway styling, heavy hiking gear, black rugged phone case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### 控制要点

- 如果画面又像普通通勤，把动作改成“整理包/系鞋带/坐在台阶查路线”，减少站立拿手机。
- 如果太潮牌，增加 `premium clean product campaign, less streetwear, more refined summer utility`。

---

## V2 Demo 2：Weekend Trail 高级轻户外

### 输入图

| 角色 | 图片 |
|---|---|
| 现有 demo 基准 | `C:\Users\Administrator\Downloads\ChatGPT Image 2026年5月9日 18_14_45.png` |
| 服装层次参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\Joytrek Midlayer Grid Fleece Zip Neck - L SENIQ.png` |
| 户外 campaign 参考 | `C:\Users\Administrator\Documents\QAir夏季系列\Q3AirSummer_人群参考精选\SS23 2.jpg` |

### 提示词

```text
Create a premium weekend trail lifestyle image for Q3 Air Summer phone case.

Use the reference images only for outdoor styling, natural trail posture, lighting, composition, and refined campaign mood. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of any reference person. Create a new fictional adult model with a different face and different hairstyle.

Scene: an accessible summer trailhead with layered trees, stone path, dry grass, and dappled sunlight. It should feel like a tasteful weekend route near the city, not wilderness expedition.

Subject: one adult woman around 28-35, North American / European market, confident and modern. Outfit should be more designed than standard hiking: lightweight technical shell or sleeveless utility vest, clean fitted base layer, relaxed trail shorts or modern outdoor skirt, trail sneakers, compact sling or small backpack, cap or sunglasses optional. She is checking the route, taking a photo, or pausing mid-walk with the phone in hand.

Product: smartphone in a colorful translucent Q3 Air Summer-style protective case with aqua teal, lime, citrus orange, or pale blue accents. The case should feel slim, fresh, and protective, not heavy tactical.

Composition: vertical 4:5 or horizontal carousel crop, editorial outdoor campaign style, model integrated with environment, phone visible but not over-presented, strong foreground/background depth.

Lighting: dappled golden summer light, crisp air, realistic skin tone, premium natural texture.

Color palette: forest green, sunlit stone, off-white, aqua teal, lime, citrus orange accents.

Avoid: copying reference faces, generic hiking catalog outfit, bulky hiking pants, heavy backpack, survival gear, extreme mountain summit, teenage styling, bikini, influencer selfie pose, black rugged phone case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

### 控制要点

- 把“hiking”改成“styled weekend trail”，审美会更靠近官网。
- 不要让模特把手机举到脸旁展示，尽量自然使用。
- 如果还是普通户外，加：`more editorial outdoor styling, modern technical fashion, premium campaign composition`。

---

## V2 Demo 3：保留 Road Trip 成功方向，但防止脸部照搬

### 输入图

| 角色 | 图片 |
|---|---|
| 成功 demo 基准 | `C:\Users\Administrator\Downloads\ChatGPT Image 2026年5月9日 18_30_59.png` |
| 产品参考 | `E:\漆安潞工作文件夹\2026\5月份\QAir夏季系列\项目资料\手机壳渲染图.png` |

### 提示词

```text
Create a refined variant of the provided summer road trip phone case image.

Use the reference image only for overall composition, lighting, warm summer mood, road trip context, and product-use relationship. Do not copy or preserve the face, identity, hairstyle, facial features, or exact body of the reference person. Create a new fictional adult model with a different face and hairstyle.

Keep the successful elements: open car trunk, warm sunlight, relaxed adult road trip energy, smartphone used naturally, colorful translucent protective phone case, travel objects like tote bag and water bottle.

Improve slightly: make the wardrobe feel more premium and designed, less casual snapshot. Use refined summer utility styling, clean layers, considered colors that connect with aqua teal, lime, citrus orange, and pale blue.

Composition: premium website campaign crop, phone visible but not forced, layered depth, natural candid action, no stock-photo look.

Avoid: copying reference faces, fake smile, luxury car ad, messy trunk, teen road trip party, bikini, black rugged phone case, fake phone UI text, visible brand logos, watermark, distorted hands, extra fingers.
```

---

## 后续建议

如果你继续用参考图生成，建议先给参考图做一个“洗图包”：

- 把清晰脸部裁掉或模糊，只留服装、姿势、场景。
- 对强参考图做 1-2 次 AI 风格重绘，让它变成“非真人来源”的 mood board。
- 产品图保持原始清晰，不要洗，因为产品结构要保真。

这样能最大化保留参考图的调性，同时降低直接复制模特脸的概率。
