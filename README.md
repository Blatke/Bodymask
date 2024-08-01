# Bodymask
This is a HS2/AI-Shoujo clothes mod for culling chara's body off the rendering process. Simply, it makes some body parts invisible.

## How to Use
1. Download the .zipmod file on the **[Release](https://github.com/Blatke/Bodymask/releases)** page, and install it like how you install any other mods.
2. In Chara Maker Mode, go to the **Top** tab on the Outfit panel, and search for "**bodymask**" in the searching box. Add it to your chara.

![AI_2024-08-01-17-49-54-447](https://github.com/user-attachments/assets/e506e0e4-fc17-4150-b146-7143f23342cd)

3. Save your chara.
4. In Studio, add your chara in the scene.
5. Please note that when the chara wearing this bodymask is added in StudioNeo, her body parts that are about to be hidden might be still shown, because the Bodymask function is overriden by the Overlay plugin.

![AI_2024-08-01-17-53-14-860](https://github.com/user-attachments/assets/4f136970-f55d-4214-88a7-24871caa9728)

Please **reload** her on the Chara tab to recover it.

![AI_2024-08-01-17-54-38-307](https://github.com/user-attachments/assets/c64640c8-95e2-46b7-83cf-3661c3d1fe2a)

6. Since the Overlay plugin overrides the Bodymask every time when the scene is loaded, it needs to reload the chara to make recover the Bodymask before you render the scecne. That is troublesome, and I'm afraid that it might not be solved until the Overlay plugin is updated.
