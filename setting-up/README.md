<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Setting Up

<sub>[previous](../) • [home](../README.md#user-content-gms2-top-down-shooter) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Lets start by getting a project and up and running.

<br>

---


##### `Step 1.`\|`SPCRK`|:small_blue_diamond:

Create a new project in UE4 and pick type **Games** and press the **Next** button:

![alt_text](images/CreateNewProject.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

Select **Blank** and press the **Next** button:

![alt_text](images/SelectBlankProjectNext.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`SPCRK`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Select C++ Basic, no starter content project and pick a directory to save it in.  Call the project `DeckOfCardsI` then press the **Create Project** button.

![alt_text](images/NewCPPDeckOCardsProj.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`SPCRK`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Press the **Add New** button and add 4 new folders called `Blueprints`, `Levels`, `Materials` and `Textures`.

![alt_text](images/AddFourNewFolders.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`SPCRK`| :small_orange_diamond:

On Moodle you will find a zip folder with all the textures you need.  Download and **unzip** the **Playing Cards** folder.  Drag all the `.png` files into the **Textures** folder.  Take a moment to look at the names.  I have very consistent naming so that we can in a loop import the textures dynamically.

![alt_text](images/DragAllCardsInFolder.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond:

Now this is a 2-D game and we will not be lighting it conventionally like a 3-D game.  In fact we will have no lights in the scene.  Click on the **Add New** button and select **Material**:

![alt_text](images/AddNewMaterial.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:
Name this material `M_Card` and double click it to enter the material editor.

![alt_text](images/.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 8.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

![alt_text](images/NameMaterialMCard.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 9.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now we right click on the graph and select a **Texture Sample** node.  Take the top **RGB** output pin and place it into the **Emissive Color** node in the M_Card node.  Since there are no lights this is a self lit texture (all will be lit with the same intensity).  Then select any of the card textures.  Look at the preview window and look at the texture on a flat plane. It is squished but we will be fixing that.

![alt_text](images/TextureSample.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 10.`\|`SPCRK`| :large_blue_diamond:

Now we want to be able to assign different card textures to different cards.  This means we need to manipulate this node.  We cannot unless we make it a parameter that we can edit. Right click on the **Texture Sample** node and select **Convert to Parameter** so we can edit it in a blueprint or in C++.

![alt_text](images/ConvertToParameter.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 11.`\|`SPCRK`| :large_blue_diamond: :small_blue_diamond: 

Now you can give this parameter a name and call it `Card_Texture`. When you finish a material you always have to press the **Apply** button so that the matelerial is rendered and usable otherwise it will not affect the actor.

![alt_text](images/CardTextureParameter.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>


##### `Step 12.`\|`SPCRK`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: 
Start a new empty level with no objects in the scene.  Call it `L_Card_Table`.

![alt_text](images/LCardTable.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 13.`\|`SPCRK`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 

Now lets set this level as the default level.  Right click on **Edit \| Project Settings** and select **Maps & Modes** and change both the **Editor Startup Map** and **Game Default Map** to **L_Card_Table**.

![alt_text](images/SetDefaultLevel.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 14.`\|`SPCRK`| :large_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:  :small_blue_diamond: 
We need to add a camera to the scene.  Type **Camera** into the **Modes** tab and drag a camera into the scene.

![alt_text](images/SelectCamera.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 15.`\|`SPCRK`| :large_blue_diamond: :small_orange_diamond: 

Press the yellow arrow next to Location and press it to reset the position to `0,0`, `0.0, 0.0`.


![alt_text](images/ResetLocationOnCam.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 16.`\|`SPCRK`| :large_blue_diamond: :small_orange_diamond:   :small_blue_diamond: 

 Now since Unreal is Z up, I want my 2-d level to be on the **X Y** plane. So move the camera up the **Z** axis, to around `310` and then rotate on the **Y** axis by `270` degrees to shoot downwards. 

![alt_text](images/FilmDownward.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 17.`\|`SPCRK`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Since this is 2-D we don't want a perspective camera, we want an [orthographic](https://en.wikipedia.org/wiki/Orthographic_projection) one. This means that objects in front of the camera do not scale, they are always the same size.  So we can stack our cards in Z without affecting the scale of the cards.

![alt_text](images/MakeCameraOrthographci.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 18.`\|`SPCRK`| :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT PAGE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../)| [home](../README.md#user-content-gms2-top-down-shooter) | [next](../)|
|---|---|---|
