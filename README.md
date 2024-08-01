# Bodymask
Most modders create their tops with putting bodymask in them in order to cull body parts to prevent clipping between top and body. However, bodymask only functions for top instead of other clothes slots, by which reason when a pair of shoes are combined with a full-body tight or latex, it cannot add bodymask into the shoes and thus might leave the tight clipping with the body.


This is a HS2/AI-Shoujo clothes mod for culling chara's body off the rendering process. Simply, it makes some body parts invisible. When wearing that sort of shoes with full-body tight, you can also add this bodymask in the Top slot to hide the body.

If you're already a modder and don't know how to make bodymask, please check: https://github.com/Blatke/Bodymask/blob/main/How%20to%20mod%20it%3F%20-%20For%20Modders.md .

## How to Use
1. Download the .zipmod file for the latest version on the **[Release](https://github.com/Blatke/Bodymask/releases)** page, and install it like how you install any other mods.
2. In Chara Maker Mode, go to the **Top** tab on the Outfit panel, and search for "**bodymask**" in the searching box. Add it to your chara.

![AI_2024-08-01-17-49-54-447](https://github.com/user-attachments/assets/e506e0e4-fc17-4150-b146-7143f23342cd)

3. Save your chara.
4. In Studio, add your chara in the scene.
5. Please note that when the chara wearing this bodymask is added in StudioNeo, her body parts that are about to be hidden might be still shown, because the Bodymask function is overriden by the Overlay plugin.

![AI_2024-08-01-17-53-14-860](https://github.com/user-attachments/assets/4f136970-f55d-4214-88a7-24871caa9728)

Please **reload** her on the Chara tab to recover it.

![AI_2024-08-01-17-54-38-307](https://github.com/user-attachments/assets/c64640c8-95e2-46b7-83cf-3661c3d1fe2a)

6. Since the Overlay plugin overrides the Bodymask every time when the scene is loaded, it needs to reload the chara to make recover the Bodymask before you render the scecne. That is troublesome, and I'm afraid that it might not be solved until the Overlay plugin is updated.

## Current Types
### Body
It culls the whole chara's body.
![2024-08-01_182744](https://github.com/user-attachments/assets/81c21edf-f89e-4590-9814-c9d75d85d0c8)
### Vagina
It culls the chara's body except her vagina and anal.
![2024-08-01_183102](https://github.com/user-attachments/assets/02ac192b-751a-4ff9-bc8d-b7ee63040586)
