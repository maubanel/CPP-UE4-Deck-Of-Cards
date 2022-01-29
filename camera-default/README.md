<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Make Camera Default

<sub>[previous](../) • [home](../README.md#user-content-gms2-top-down-shooter) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Now Unreal expects a camera to be attached to a player whether the game is 2-d or 3-d.  Now our little game here is a card game, so there is no player as you are just controlling a cursor.  There is a way of telling the engine that this camera is the one we want to use.<br><br>.  Now whenever you create a new level the game creates a special blueprint.  It is called a **Level Blueprint**.  This special blueprint allows us to access objects in the game scene.  

<br>

---


##### `Step 1.`\|`SPCRK`|:small_blue_diamond:

Press the **Blueprints** button then select **Open Level Blueprint**:

![alt_text](images/SetUpCameraInLevelBP.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

Select in the game level the camera actor.

![alt_text](images/SelectCameraActor.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`SPCRK`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now go back to the **Level Blueprint** and right click on the graph.  You will notice that it adds to the top a **Create a Reference to CameraActor**.  Press this to add this node.

![alt_text](images/GetReferenceToSceneActor.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`SPCRK`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

 Now again press the right mouse button on the empty graph and select a **Get Player Controller** node.

![alt_text](images/GetPlayerController.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`SPCRK`| :small_orange_diamond:

So your level blueprint should look like this:

![alt_text](images/LevelBP.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond:

Add a **Set View Target With Blend** node and plug the **Player Controller** into the target and plug in the **Camer Actor** to the **New View Target** input node.  Then connect the execution pin from **EventBeginPlay** to the **Set View Target** node.  Add a comment that describes what we are doing.

![alt_text](images/SetViewTarget.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Run the game and now it selects the camera you set.  You can't control a player, and it is pretty much set up so we can begin.

![alt_text](images/RunGameViewCorrect.gif)

___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT PAGE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../)| [home](../README.md#user-content-gms2-top-down-shooter) | [next](../)|
|---|---|---|
