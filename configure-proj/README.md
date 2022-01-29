<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

### Configure Projects

<sub>[previous](../) • [home](../README.md#user-content-gms2-top-down-shooter) • [next](../)</sub>

<img src="https://via.placeholder.com/1000x4/45D7CA/45D7CA" alt="drawing" height="4px"/>

Now we want to take out the extraneous object we don't need and set the default camera to the one we loaded into the scene.  We do this by adding some custom setup files that default ones are provided for us (and add all these files).

<br>

---


##### `Step 1.`\|`SPCRK`|:small_blue_diamond:

Add a new **Blueprint** and this time select a **Player Controller** class.  We need to add a cursor and cursor events as we will be handling the cards with a mouse.

![alt_text](images/SelectPlayerControllerClass.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 2.`\|`FHIU`|:small_blue_diamond: :small_blue_diamond: 

Now name the blueprint `BP_Card_PlayerController` and make sure that you enable **Show Mouse Cursor**, **Enable Click Events** and **Enable Mouse Over Events**.  We are not supporting mobile so you can leave the touch events disabled.

![alt_text](images/PlayerControllerCursor.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 3.`\|`SPCRK`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Now create a new **Blueprint** and select **Game Mode Base** as the base class.

![alt_text](images/SelectGameModeBaseClass.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 4.`\|`SPCRK`|:small_blue_diamond: :small_blue_diamond: :small_blue_diamond: :small_blue_diamond:

Call this file `BP_Card_GameModeBase`.

![alt_text](images/CardGameModeBaseName.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 5.`\|`SPCRK`| :small_orange_diamond:

 Now double click this blueprint and turn off the **Game Session Class** as we will not be using networking features.  Change the **Player Controller Class** to `BP_Card_PlayerController`.  Turn off the **Default Pawn Class** so that you don't control a player when playing the game.

![alt_text](images/CustomizeGameMode.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 6.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond:

 Now we are not done.  This Game Mode still won't launch until we set it.  Press the **Settings** button and select **World Settings**.

![alt_text](images/WorldSettingsWindow.jpg)

<img src="https://via.placeholder.com/500x2/45D7CA/45D7CA" alt="drawing" height="2px" alt = ""/>

##### `Step 7.`\|`SPCRK`| :small_orange_diamond: :small_blue_diamond: :small_blue_diamond:

Now the **World Settings** tab appears to the right behind the **Details** panel.  Change the **GameMode Override** to `BP_Card_GameModeBase`.

![alt_text](images/NewGameModeBaseWS.jpg)


___


<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

<img src="https://via.placeholder.com/1000x100/45D7CA/000000/?text=Next Up - ADD NEXT PAGE">

<img src="https://via.placeholder.com/1000x4/dba81a/dba81a" alt="drawing" height="4px" alt = ""/>

| [previous](../)| [home](../README.md#user-content-gms2-top-down-shooter) | [next](../)|
|---|---|---|
