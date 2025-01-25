# List of Functions

### ‎

> ## **Navigation and GUI Management**

>> ### **Back**
>> Navigate back to a previous state or location with a GUI.

>> Syntax: ```- 'Back'```

>> Example: ```- 'Back'```

>###

>> ### **HasBack**
>> Checks if navigation history ('Back' functionality) is available.

>> Syntax: ```- 'HasBack'```

>> Example: ```- 'HasBack'```

>###

>> ### **SetBack**
>> Sets a designated back location or state within a GUI.

>> Syntax: ```- 'SetBack: <boolean result>'```

>> Example: ```- 'SetBack: true'```

>###

>> ### **Gui**
>> Open a specified GUI.

>> Syntax: ```- 'Gui: <name of gui>.yml'```

>> Example: ```- 'Gui: cosmetics.yml'```

>###

>> ### **RefreshGUI**
>> Update or refresh the contents of the GUI currently being viewed.

>> Syntax: ```- 'RefreshGui'```

>> Example: ```- 'RefreshGui'```

>###

>> ### **RefreshSlot**
>> Update or refresh the contents of a specific slot within the GUI.

>> Syntax: ```- 'RefreshSlot: <Slot # (Range: 0-53)>'```

>> Example: ```- 'RefreshSlot: 31'```

>###

>> ### **HasMetadata**
>> Checks if metadata is set.

>> Syntax: ```- 'HasMetadata'```

>> Example: ```- 'HasMetadata'```

>###

>> ### **CopyBackMetadata**
>> Copies metadata associated with navigation history.

>> Syntax: ```- 'CopyBackMetadata: true'```

>> Example: ```- 'CopyBackMetadata: true'```

>###

>> ### **IsGuiMetadataSet**
>> Checks if specific GUI metadata is set.

>> Syntax: ```- 'IsGuiMetadataSet: <user defined metadata>'```

>> Example: ```- 'IsGUIMetadataSet: %metadata_custom%'```

>###

>> ### **SetMetadata**
>> Sets metadata for a specific entity or block.

>> Syntax: ```- 'SetMetadata: <entity>,<metadata string you want to set>,<metadata you want to use>'```

>> Examples:

>> ```- 'SetMetadata: gui,preset_value,300'```

>> ```- 'SetMetadata: gui,preset_value,%defined_macro-metadata_price1%'```

>###

>> ### **CheckMovable**
>> Checks if an entity or block is movable.

>> Syntax: ```- ''```

>> Example: ```- ''```


### ‎


>## **Player and Entity Management**

>> ### **AsyncRunning**
>> Checks if an asynchronous task is currently running.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **CheckItemTypeInHand**
>> Checks the type of item currently held by the player.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **CheckLevel**
>> Verifies if a specified level meets a certain criteria.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **CheckPlayerWorld**
>> Determines the world in which a player is located.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **Executec**
>> Executes a command on the server.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **Executep**
>> Executes a command as if a player had typed it.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **IsBedrockPlayer**
>> Checks if a player is using Minecraft: Bedrock Edition.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **LoggedIn**
>> Checks if a player is logged into the server.

>> Syntax: ```- ''```

>> Example: ```- ''```

### ‎

>## **Cooldown and Timing**

>> ### **CheckTick**
>> Retrieves the current tick (unit of time) in the game.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **IsOnCooldown**
>> Checks if a specified action or player is currently on cooldown.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **SetCooldown**
>> Sets a cooldown for a specified action or player.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **Delay**
>> Introduces a delay or pause in script execution.

>> Syntax: ```- ''```

>> Example: ```- ''```

### ‎

> ## **Game Rule and Environment**

>> ### **GetGameRule**
>> Retrieves the value of a specific game rule in the world.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **SetGamerule**
>> Sets a specific game rule in the world.

>> Syntax: ```- ''```

>> Example: ```- ''```

### ‎

> ## **Logging and Messaging**

>> ### **Log**
>> Logs a message or event to the server console.

>> Syntax: ```- 'Log: <message to be displayed as a log in the console>'```

>> Example: ```- 'Log: %player% purchased an item.'```

>###

>> ### **Msg** or **Pmsg**
>> Sends a message to players in the server.

>> Syntax: ```- 'Msg: <message sent to player, supports vanilla colors codes only>'``` OR ```- 'Pmsg: <message sent to player>'```

>> Example: ```- 'Msg: Insufficient permission.'``` OR ```- 'Pmsg: Insufficient permission.'```

>###

>> ### **MiniMsg**
>> Sends a message to the player on the server using the [minimessage](https://docs.advntr.dev/minimessage/format.html) format.

>> Syntax: ```- 'MiniMsg: <message sent to player, supports minimessage codes only>'```

>> Example: ```- ''```

>###

>> ### **MsgJson**
>> Sends a message to the player on the server using JSON format.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **Broadcast**
>> Sends a message to all players in the Minecraft server.

>> Syntax: ```- 'Bradocast: <message sent to all players>'```

>> Example: ```- 'Broadcast: An event will occur soon. Meet us at spawn! /spawn'```

>###

>> ### **MiniBroadcast**
>> Sends a minimized message to all players in the Minecraft server.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **BroadcastJson**
>> Sends a JSON-formatted message to all players in the Minecraft server.

>> Syntax: ```- ''```

>> Example: ```- ''```

### ‎

> ## **Inventory and Item Management**
>> ### **OpenInventorySlots**
>> Checks if a player has an open inventory slot within their inventory. Opens additional inventory slots within a GUI.

>> Syntax: ```- 'OpenInventorySlots: <# of slots, maximum: 36>'```

>> Example: ```- 'OpenInventorySlots: 1'```

>###
>> ### **RemoveSlot**
>> Removes an item from a specified inventory slot within the player's inventory.

>> Syntax: ```- 'RemoveSlot: <Slot #, maximum: 36>'```

>> Example: ```- 'RemoveSlot: 1'```

>###
>> ### **SetAmount**
>> Sets the display quantity for an item as if it is a stack of items.

>> Syntax: ```- 'SetAmount: <Amount, maximum: 64>'```

>> Example: ```- 'SetAmount: 32'```

>###
>> ### **SetClose**
>> Closes the current GUI.

>> Syntax: ```- 'SetClose: <boolean result>'```

>> Example: ```- 'SetClose: true'```

>###
>> ### **SetDurability**
>> Sets the durability of an item.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###
>> ### **SetEnchants**
>> Enchants an item with specified enchantments.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###
>> ### **SetName**
>> Sets the name of an item.

>> Syntax: ```- 'SetName: <user-defined item name>'```

>> Example: ```- 'SetName: &aCosmetics'```

>###
>> ### **SetLore**
>> Sets the lore text for an item. For multiple lines, quotation marks ```""``` are required in lieu of apostraphies ```''```.

>> Syntax: ```- 'SetLore: <user-defined lore text>'```

>> Example:

>>```- 'SetLore: This item is locked.'```

>> ```- "SetLore: This item is locked&r\nMessage an Admin if this is an error."```

>###
>> ### **SetNBT** *(obsolete)*
>> Sets NBT (Named Binary Tag) data for an entity or block.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###
>> ### **SetType**
>> Sets the slot item type of an entity or block.

>> Syntax: ```- 'SetType: <entity or block>'```

>> Example: ```- 'SetType: grass_block'```

### ‎

> ## **Permission Management**
>> ### **HasPermission** or **Permission**
>> Checks if a player has a specific permission.

>> Syntax: ```- 'HasPermission: <permission node>'``` OR ```- 'Permission: <permission node>'```

>> Example: ```- 'HasPermission: essentials.home'``` OR ```- 'Permission: essentials.home'```

>###

>> ### **AddPermission**
>> Grants a player a specific permission.

>> Syntax: ```- 'AddPermission: <permission node>'```

>> Example: ```- 'AddPermission: essentials.home'```

>###

>> ### **RemovePermission**
>> Removes a specific permission from a player.

>> Syntax: ```- 'RemovePermission: <permission node>'```

>> Example: ```- 'RemovePermission: essentials.home'```

### ‎

> ## **Game Mechanics**

>> ### **Condition**
>> Evaluates a specified condition and returns a boolean result.

>> Syntax: ```- 'Condition: <numeral value or placeholder> <expressions: ==, <=, >=> <numeral value or placeholder>'```

>> Example: ```- 'Condition: %essentials_ping% >= 30'```

>> ```- 'Condition: %value% == %acceptable_value%'```

>###

>> ### **Particle**
>> Generates particle effects at a specified location.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **ResetFrame**
>> Resets the frame counter.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **ResetTick**
>> Resets the tick counter.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **Send**
>> Sends a message or data to a specified server.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **Sound**
>> Plays a sound at a specified location in the game world. Available compatible minecraft sound IDs can be found [here](https://helpch.at/docs/1.21.1/org/bukkit/Sound.html).

>> Syntax: ```- 'Sound: <valid minecraft sound ID>,<volume>,<pitch>'```

>> Example: ```- 'Sound: ENTITY_PLAYER_LEVELUP,1.0,2.0'```

### ‎

> ## **Economy Functions**
>> ### **MoneyBalance**
>> Retrieves the current balance of in-game currency for a player.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###

>> ### **MoneyDeposit**
>> Deposits a specified amount of in-game currency into a player's balance.

>> Syntax: ```- 'MoneyDeposit: <currency>,<amount>'```

>> Example: ```- 'MoneyDeposit: money,%cosmetic-price%'```

>###

>> ### **MoneyWithdraw**
>> Withdraws a specified amount of in-game currency from a player's balance.

>> Syntax: ```- '<currency>,<amount>'```

>> Example: ```- 'money,%cosmetic-price%'```

### ‎

> ## **Miscellaneous**
>> ### **Random**
>> Generates a random number within a specified range.

>> Syntax: ```- ''```

>> Example: ```- ''```

>###