# Introduction to Functions

Functions are the building blocks of DynamicGui and are part of what makes DynamicGui truly dynamic. Function sections can be written as simple or as complex as the user needs to make them. To evaluate functions we will start by looking at the example again.


```yaml
0:
  functions:
    broadcast-click: #This can be named anything but it should be descriptive
      type: 'click' #The type of function to run
      functions:
      - 'Broadcast: Test Broadcast'
```

**Navigation and GUI Management:**

1. **Back**: Navigates back to a previous state or location within a GUI.
2. **Gui**: Opens a graphical user interface (GUI) with the specified name.
3. **HasBack**: Checks if there's a navigation history (back functionality) available.
4. **RefreshGui**: Updates or refreshes the contents of a GUI.
5. **RefreshSlot**: Updates or refreshes the contents of a specific slot within a GUI.
6. **SetBack**: Sets a designated back location or state within a GUI.
7. **CopyBackMetadata**: Copies metadata associated with navigation history.
8. **HasMetadata**: Checks if metadata is available.
9. **IsGuiMetadataSet**: Checks if GUI metadata is set.
10. **SetMetadata**: Sets metadata for a specific entity or block.
11. **CheckMovable**: Checks if an entity or block is movable.

**Player and Entity Management:**

1. **AsyncRunning**: Checks if an asynchronous task is currently running.
2. **CheckItemTypeInHand**: Checks the type of item currently held by the player.
3. **CheckLevel**: Verifies if a specified level meets a certain criteria.
4. **CheckPlayerWorld**: Determines the world in which a player is located.
5. **Executec**: Executes a command on the server.
6. **Executep**: Executes a command as if a player had typed it.
7. **IsBedrockPlayer**: Checks if a player is using the Bedrock edition of Minecraft.
8. **LoggedIn**: Checks if a player is logged into the server.

**Cooldown and Timing:**

1. **CheckTick**: Retrieves the current tick (unit of time) in the game.
2. **IsOnCooldown**: Checks if a specified action or player is currently on cooldown.
3. **SetCooldown**: Sets a cooldown for a specified action or player.
4. **Delay**: Introduces a delay or pause in script execution.

**Game Rule and Environment:**

1. **GetGameRule**: Retrieves the value of a specific game rule in the world.
2. **SetGamerule**: Sets a specific game rule in the world.

**Logging and Messaging:**

1. **Log**: Logs a message or event to the server console.
2. **Msg**: Sends a message to players in the server.
3. **MiniMsg**: Sends a message to the player on the server using the [minimessage](https://docs.advntr.dev/minimessage/format.html) format.
4. **MsgJson**: Sends a message to the player on the server using JSON format.
5. **Broadcast**: Sends a message to all players in the Minecraft server.
6. **BroadcastJson**: Sends a JSON-formatted message to all players in the Minecraft server.
7. **MiniBroadcast**: Sends a minimized message to all players in the Minecraft server.

**Inventory and Item Management:**

1. **OpenInventorySlots**: Opens additional inventory slots within a GUI.
2. **RemoveSlot**: Removes an item from a specified inventory slot.
3. **SetAmount**: Sets the quantity of items in a stack.
4. **SetClose**: Closes a GUI.
5. **SetDurability**: Sets the durability of an item.
6. **SetEnchants**: Enchants an item with specified enchantments.
7. **SetLore**: Sets the lore text for an item.
8. **SetName**: Sets the name of an item.
9. **SetNBT**: Sets NBT (Named Binary Tag) data for an entity or block.
10. **SetType**: Sets the type of an entity or block.

**Permission Management:**

1. **AddPermission**: Grants a player a specific permission.
2. **HasPermission**: Checks if a player has a specific permission.
3. **RemovePermission**: Removes a specific permission from a player.

**Misc:**

1. **Random**: Generates a random number within a specified range.

**Game Mechanics and Events:**

1. **Condition**: Evaluates a specified condition and returns a boolean result.
2. **Particle**: Generates particle effects at a specified location.
3. **ResetFrame**: Resets the frame counter.
4. **ResetTick**: Resets the tick counter.
5. **Send**: Sends a message or data to a specified server.
6. **Sound**: Plays a sound at a specified location in the game world.

**Economy:**

1. **MoneyBalance**: Retrieves the current balance of in-game currency for a player.
2. **MoneyDeposit**: Deposits a specified amount of in-game currency into a player's balance.
3. **MoneyWithdraw**: Withdraws a specified amount of in-game currency from a player's balance.