ModPE-Functions
===============

## Functions

```JavaScript

public void addItemInventory(int id, int amount, int damage) {}
> addItemInventory(264, 16, 0); //gives 10 diamonds to player


public void bl_setMobSkin(int entity, String tex) {}
> bl_setMobSkin(victim, "mob/zombie.png"); //sets an entities skin to an image included in MCPE


public int bl_spawnMob(double x, double y, double z, int typeId, String tex) {}
> bl_spawnMob(128, 70, 128, 12, "mob/pig.png"); //spawns a pig with pig texture at the coordinates [128,70,128]


public void clientMessage(String text) {}
> clientMessage("Hello Player"); //Sends a chat Message with the content of Hello Player


public static void explode(double x, double y, double z, double radius) {}
> explode(100, 150, 30, 6); //explodes at the location [100,150,30] within a radius of 6 blocks


public int getCarriedItem() {}
> getCarriedItem(); //returns the id of the players carried item


public NativePointer getLevel() {}
> getLevel(); //returns the level


public double getPitch(Object entObj) {}
> getPitch(getPlayerEnt()); //returns the pitch of an entity (Players pitch in example)


public int getPlayerEnt() {}
> getPlayerEnt(); //get's the player's entity


public double getPlayerX() {}
> getPlayerX(); //returns the x coordinate of the player


public double getPlayerY() {}
> getPlayerY(); //returns the y coordinate of the player


public double getPlayerZ() {}
> getPlayerZ(); //returns the z coordinate of the player


public int getTile(int x, int y, int z) {}
> getTile(1,2,3); { //returns the blocks id which is located at the coordinates [1,2,3]


public double getYaw(Object entObj) {}
> getYaw(getPlayerEnt()); //returns the yaw of an entity (Players yaw in example)


public void preventDefault() {}
> preventDefault(); //prevents MCPE to execute the action it normally should


public void print(String str) {}
> print("I'm an android Toast"); //A message as clientMessage but is displayed as an Android Toast


public void rideAnimal(int rider, int mount) {}
> rideAnimal(victim, attacker); //victim-attacker is only an example if used in attackHook, victim would ride attacker


public void setNightMode(boolean isNight) {}
> setNightMode(true); //Sets NightMode to true or false


public static void setPosition(int ent, double x, double y, double z) {}
> setPosition(getPlayerEnt(), 50, 100, 200); //would teleport player to the coordinates [50,100,200]


public static void setPositionRelative(int ent, double x, double y, double z) {}
> setPositionRelative(getPlayerEnt(), 10, 5, 20); //would teleport player to the coordinates [10,5,20]


public void setRot(int ent, double yaw, double pitch) {}
> setRot(victim, 1, 2); //would set victims (attackHook) yaw to 1 and pitch to 2


public static void setTile(int x, int y, int z, int id, int damage) {}
> setTile(70, 80, 90, 17, 2); //sets a block to a position: Birch Wood at [70,80,90]


public static void setVelX(int ent, double amount) {}
> setVelX(getPlayerEnt(), 4); //sets entitys (in example: players) X Velocity to 4


public static void setVelY(int ent, double amount) {}
> setVelY(getPlayerEnt(), 2); //sets entitys (in example: players) Y Velocity to 2


public static void setVelZ(int ent, double amount) {}
> setVelZ(getPlayerEnt(), 7); //sets entitys (in example: players) Z Velocity to 7


public int spawnChicken(double x, double y, double z, ~~String tex~~) {}
> spawnChicken(getPlayerX(), getPlayerY(), getPlayerZ(), ~~String tex~~); //Textures unsupported; spawns chicken


public int spawnCow(double x, double y, double z, ~~String tex~~) {}
> spawnCow(7, 8, 9, ~~String tex~~); //Textures unsupported; spawns cow at coords of [7,8,9]


public int spawnPigZombie(double x, double y, double z, int item, ~~String tex~~) {}
> spawnPigZombie(20, 200, 200, 283, ~~String tex~~); //Textures unsupported; spawns pigmen at coords of [20,200,200] with gold sword

```

## Comming soon

```JavaScript
/*
ModPE.getItemName(par1int, par2int, par3boolean);
ModPE.joinServer(par1String, par2int);
ModPE.langEdit(par1String, par2String);
ModPE.leaveGame();
ModPE.log(par1String);
ModPE.overrideTexture(par1String, par2String);
ModPE.readData(par1String);
ModPE.removeData(par1String);
ModPE.resetImages();
ModPE.saveData(par1String, par2String);
ModPE.selectLevel(par1String, par2String, par3String, par4int);
ModPE.setFoodItem(par1int, par2String, par3int, par4int, par5String);
ModPE.setGameSpeed(par1double);
ModPE.setGuiBlocks(par1String);
ModPE.setItem(par1int, par2String, par3int, par4String);
ModPE.setItems(par1String);
ModPE.setTerrain(par1String);
ModPE.takeScreenshot(par1String);

Level.destroyBlock(par1int, par2int, par3int, par4boolean);
Level.dropItem(par1double, par2double, par3double, par4double, par5int, par6int, par7int);
Level.explode(par1double, par2double, par3double, par4double);
Level.getAddress();
Level.getChestSlot(par1int, par2int, par3int, par4int);
Level.getChestSlotCount(par1int, par2int, par3int, par4int);
Level.getChestSlotData(par1int, par2int, par3int, par4int);
Level.getData(par1int, par2int, par3int);
Level.getGameMode();
Level.getSignText(par1int, par2int, par3int, par4int);
Level.getTile(par1int, par2int, par3int);
Level.getTime();
Level.getWorldDir();
Level.getWorldName();
Level.playSound(par1double, par2double, par3double, par4String, par5double, par6double);
Level.playSoundEnt(par1int, par2String, par3double, par4double);
Level.setChestSlot(par1int, par2int, par3int, par4int, par5int, par6int, par7int);
Level.setGameMode(par1int);
Level.setNightMode(par1boolean);
Level.setSignText(par1int, par2int, par3int, par4int, par5String);
Level.setSpawn(par1int, par2int, par3int);
Level.setTile(par1int, par2int, par3int, par4int, par5int);
Level.setTime(par1int);
Level.spawnChicken(par1double, par2double, par3double, par4String);
Level.spawnCow(par1double, par2double, par3double, par4String);
Level.spawnMob(par1double, par2double, par3double, par4int, par5String);

Player.addItemCreativeInv(par1int, par2int, par3int);
Player.addItemInventory(par1int, par2int, par3int);
Player.clearInventorySlot(par1int);
Player.getArmorSlot(par1int);
Player.getArmorSlotDamage(par1int);
Player.getCarriedItem();
Player.getCarriedItemCount();
Player.getCarriedItemData();
Player.getEntity();
Player.getInventorySlot(par1int);
Player.getInventorySlotCount(par1int);
Player.getInventorySlotData(par1int);
Player.getName(par1int);
Player.getSelectedSlotId();
Player.getX();
Player.getY();
Player.getZ();
Player.isPlayer(par1int);
Player.setArmorSlot(par1int, par2int, par3int);
Player.setHealth(par1int);

Entity.getAnimalAge(par1int);
Entity.getEntityTypeId(par1int);
Entity.getHealth(par1int);
Entity.getPitch(par1int);
Entity.getVelX(par1int);
Entity.getVelY(par1int);
Entity.getVelZ(par1int);
Entity.getX(par1int);
Entity.getY(par1int);
Entity.getYaw(par1int);
Entity.getZ(par1int);
Entity.remove(par1int);
Entity.rideAnimal(par1int, par2int);
Entity.setAnimalAge(par1int, par2int);
Entity.setCarriedItem(par1int, par2int, par3int, par4int);
Entity.setFireTicks(par1int, par2int);
Entity.setHealth(par1int, par2int);
Entity.setMobSkin(par1int, par2String);
Entity.setPosition(par1int, par2double, par3double, par4double);
Entity.setPositionRelative(par1int, par2double, par3double, par4double);
Entity.setRenderType(par1int, par2int);
Entity.setRot(par1int, par2double, par3double);
Entity.setSneaking(par1int, par2boolean);
Entity.setVelX(par1int, par2double);
Entity.setVelY(par1int, par2double);
Entity.setVelZ(par1int, par2double);
Entity.spawnMob(par1double, par2double, par3double, par4int, par5String);

Block.defineBlock(par1int, par2String, par3Object, par4Object, par5Object, par6Object);
Block.setColor(par1int, par2Scriptable);
Block.setDestroyTime(par1int, par2double);
Block.setExplosionResistance(par1int, par2double);
Block.setLightLevel(par1int, par2int);
Block.setRenderLayer(par1int, par2int);
Block.setShape(par1int, par2double, par3double, par4double, par5double, par6double, par7double);
*/
```
