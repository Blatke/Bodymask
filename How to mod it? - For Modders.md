# How to mod it? - A Simple Guide for Modders Using hooh's Modding Tools
Since there is so far no such a plugin in HS2/AIS Chara Maker Mode to edit bodymask, it still needs modders to add bodymask in their modding process.

This text simply introduces how to add bodymask by using hooh Modding Tools. In addition, I won't in this text to elaborate everything, and I suppose that you have already known the basic knowledge on hooh's Modding Tool, at least for modding studio items. For newbie modder who would like to learn hooh's Modding Tools from scratch to  mod for HS2 or AI-Shoujo, please check hooh's guide (https://hooh-hooah.github.io/#/README), or my more detailed tutorials (https://www.blatke.cc/index.html#tutorials).

## Prepare A Texture for Bodymask
A bodymask, using HS2/AIS Bodymask function, culls chara's body according to the body's UV mapping. You can have a template like this:
![1](https://github.com/user-attachments/assets/054da1ad-7684-4cb2-a356-a231ee10dd78)

See? It looks like what you got from the Overlay plugin. 

Now, you can download and edit this template image. Draw some patterns on it by using white color (#FFFFFF). In bodymask, white color let it know which body parts NOT to cull or hide. For the remaining parts to be culled, make it in cyan color (#00FFFF). So, you can see what I've done:
![1](https://github.com/user-attachments/assets/c942e556-89c4-4d56-a5e5-226842bc4ef5)

I made some white blocks on the vagina and anal parts, left the other parts cyan and deleted the template background of the body. This means I want to cull the body except the vagina and anal. BTW, if I don't delete the background, and make it semi-transparent, it should be like this:
![image](https://github.com/user-attachments/assets/6528d8ce-5d8a-4ee7-a30e-9d686e2542a9)

But we must delete this background, or the bodymask might be messed up.

Save it as a **.png** file, name it, let's say, "vagina".

## Mod It
Let's go to your Unity Editor with hooh's Modding Tools already installed in it.

Create an **Empty** object in Hierarchy view. It's automatically named "GameObject".

![image](https://github.com/user-attachments/assets/4ca3b8ad-101c-448e-abf9-7cc2c9adc279)

Select GameObject, and in Inspector view, click **Common** button, then choose **Clothing**. 

![image](https://github.com/user-attachments/assets/ed41deef-ab9c-43fc-93fe-a2869ffe8ab0)

In Project view, create a folder named "**prefabs**". This folder is to be put target files in it.

![image](https://github.com/user-attachments/assets/b91a1b06-baf5-4f3a-b4c1-ebe2fa708c16)

Select GameObject in Hierarchy view and open **hooh Tools** menu on the topbar, then click **Create Prefab**.

![image](https://github.com/user-attachments/assets/1e473f6e-36b7-4b85-9bcc-24a3b63c3acf)

Then, you got a **GameObject.prefab** file in Project view, drag and drop it in **prefabs** folder.

Also, drag and drop your bodymask image, **vagina.png**, in **prefabs** folder. Now you got a .prefab and a .png files in it.

Outside the prefabs folder, create an xml (sxml) file. Edit it by using this script:
```
<packer>
  <guid>[YourGuid]Bodymask</guid>
  <name>Bodymask</name>
  <version>0.0.1</version>
  <author>Your Name</author>
  <description></description>
  <bundles>
    <folder auto-path="prefabs" from="prefabs" filter=".*?\.(psd|png|tif|prefab)"/>
  </bundles>
<build>
    <list type="ftop">
      <item
              kind="0" possess="1" name="Bodymask Vagina" state="0" 
              coordinate="0" 
              mesh-a="GameObject" en-us="0" no-bra="0" 
              bodymask-tex="vagina"
       />
    </list>
</build>
</packer>
```
Just feel free to change <guid>, <name>, <version>, <author> and <description>. As it was told, only top has bodymask functioning on body, so we use <list type="ftop"> standing for "female top". In the tag <item>, the field "**mesh-a**" is the file name of the prefab you have in the prefabs folder. You have to create a prefab, even for an empty object, otherwise hooh tools cannot pack it into a mod. The field "**bodymask-tex**" is the file name of the png image in the prefabs folder.

For other fields, please check: https://hooh-hooah.github.io/#/technical/category-list-female?id=female-top . 

With everything above, you can now **Build** the mod.

Then, we got a culled body without vagina and anal being hidden:
![image](https://github.com/user-attachments/assets/1d0347a4-5506-46d6-bcd3-8bdc483f9608)
