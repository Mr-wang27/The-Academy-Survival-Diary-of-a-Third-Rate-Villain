# 生成记录

工具：内置 ImageGen；背景：白色非透明。实际输入参考均来自 `人物资源/贝尔/`，生成图复制到本目录。下列为实际提交的提示词，路径详见角色档案。

## front-v001.png

输入：R03 `078.png`、R01 `068.png`、R02 `071.png`、R04 `074.png`。返回：`exec-a2c4a3e2-e312-432c-a8ba-0917eb0f92d5.png`。

> Use case: illustration-story. Full-body strictly FRONT character design sheet of BELL, the FEMALE BLACK-HAIRED MAID in the attached original webtoon panels. Reference 078.png is authoritative for her face, narrow golden yellow eyes, black straight blunt bangs, chin-to-neck-length black bob, white ruffled maid headband, white collar and narrow deep-red ribbon. References 068.png and 071.png show her complete maid outfit: dark black-brown short puff-sleeve dress, white shoulder ruffles and apron straps, white apron bib and front apron with ruffled edge, full calf-length black skirt with pale gray ruffled hem, gray knee-high stockings, flat black Mary Jane strap shoes. 074.png supports skirt and footwear only; its dramatic glowing eyes and windblown long hair are NOT the normal design. Neutral expression and relaxed upright standing pose, arms loosely aside, entire hair to shoes visible, pure white background, eye-level flat webtoon ink lines and simple cel shading. Absolutely no blond man, no basket, no glowing eyes, no extra jewelry, no lettering.

## right-profile-v001.png

输入：R02、R01、R03、`front-v001.png`。返回：`exec-de90b3b8-0163-42da-9bdf-44999513c18c.png`。采用 C01/C03。

> Use case: illustration-story. Create one single full-body STRICT RIGHT SIDE PROFILE view of Bell, the female black-haired golden-eyed maid in original comic references 071.png, 068.png, 078.png, matching the checked front sheet image 4. She faces image LEFT, exact 90-degree side profile, upright natural pose with hands relaxed at sides. Keep white ruffled maid headband, straight black blunt bangs and neck-length bob, dark short puff-sleeve dress, white shoulder ruffles and apron strap, small white collar with narrow dark-red ribbon, white bib and ruffled front apron, black full skirt reaching mid-calf with pale-gray ruffled hem, gray knee-high stockings, flat black Mary Jane shoes. Eye-level white background, complete hair and both shoes, crisp original webtoon line art and cel shading. No basket, no other characters, no glowing eyes, no long windblown hair, no text. Match front sheet height, head/body ratio, waist and hem lines.

## back-v001.png

输入：R01、R02、`front-v001.png`、`right-profile-v001.png`。返回：`exec-5059714b-62e5-4f5e-b2a2-db687c7d6ff1.png`。采用 C01–C03。

> Use case: illustration-story. Create one full-body STRAIGHT BACK character sheet of Bell, the young black-haired female maid in attached original comic references and the checked front and strict right-profile design images. Match exactly her height, slim proportions, neck-length straight black bob haircut, broad white ruffled maid headband, dark black-brown short puff-sleeve dress, white shoulder ruffles and apron straps, simple white apron waist band with a small practical tied knot at center back, full black calf-length skirt with pale gray ruffled hem, gray knee-high stockings and flat black Mary Jane strap shoes. Back garment construction is a conservative completion: plain dark back panel and simple strap connections, no ornament, no large bow, no exposed back, no emblem. Both arms relaxed at sides; figure faces directly away with no face visible. White background, eye-level, head and both shoes complete. Crisp black webtoon lines and cel shading. No props, basket, text, glowing effects, or other characters. Original 074.png is only for hem and shoes, not its magic long-hair effect.

## portrait-v001.png

输入：R03、R01、`front-v001.png`。返回：`exec-b3b15140-bc72-43aa-8df9-daeae08771cf.png`。检查发现头饰顶端被裁切。

> Use case: illustration-story. Create a clean FRONT HEAD-AND-SHOULDERS COMIC ID PORTRAIT of BELL, the FEMALE black-haired maid in original 078.png. Image 1 is authoritative for her actual face: youthful slim pointed chin, narrow golden-yellow eyes, strong black upper eyeliner, blunt straight black bangs with central thin divisions, sleek chin-to-neck-length black bob, pale skin. Image 2 is supporting face and shoulder evidence. Image 3 is checked full-body front character sheet and defines her white ruffled maid headband, white collar, deep-red narrow ribbon, black bodice, white shoulder ruffles and apron straps. Neutral closed-mouth expression, gaze directly at viewer, head upright and not tilted. Pure white background, full headband and shoulders visible. Flat colorful original webtoon line art, subtle cel shading. No photorealism, no glowing eyes, no basket, no other person, no words.

## portrait-v002.png

输入：`portrait-v001.png`、R03。返回：`exec-74a4905c-077a-4162-92c3-2bf403341a61.png`。修正头饰裁切；最终采用此版。

> Edit image 1, the current portrait of Bell. Make ONLY a composition/framing correction: zoom out moderately and add clean white space above the white ruffled maid headband so the entire top edge is visibly inside the canvas with generous margin. Keep the SAME female face, narrow golden eyes, black blunt bangs and bob, neutral expression, headband design, collar, red ribbon, shoulder ruffles, webtoon linework and cel shading. Keep a centered straight-on head-and-shoulders ID portrait. Do not alter her identity, facial proportions, accessories, or outfit. Image 2 is the original comic face reference for identity.

误识别说明：最初把同框金发男性误认作贝尔，相关图和档案已移至 `../误识别归档/`，不属于本次交付。
