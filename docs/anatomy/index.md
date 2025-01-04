# Basic GUI Anatomy

Before diving deep into DynamicGUI, it’s essential to grasp the anatomy or components comprising a GUI.

## Top-Level Properties
At its highest level, a GUI consists of properties determining the base behavior.

|  | Property Name | Description | Requirements |
| :---- | :---- | :---- | :---- |
|  | ```title``` | This is the title of the GUI Menu. This will appear at the top of each GUI. For no title, keep as ‘’ or “” | Required. For no title, keep as ‘’ or “” |
|  | ```rows``` | Rows determine the amount of rows the GUI will generate. For each row, it will generate 9 configurable slots. The player's inventory slots cannot be configured. This is a required property **ONLY IF** your ```type``` property is set to ```CHEST``` or is not mentioned as a property. (minimum: 1 \- maximum: 6\) | Required. Min.: 1; Max.: 6 |
|  | ```close``` | A boolean argument which determines the behavior of the GUI when a slot has been interacted with. 'true' will close the GUI when a slot is interacted. 'false' will NOT close the GUI when a slot is interacted. | Optional. |
|  | ```type``` | Set the GUI type. Available types can be found [here](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/event/inventory/InventoryType.html). Type is ```CHEST``` by default. | Optional. |
|  | ```alias``` | The different command aliases available to open the GUI. This is optional. | Optional. |
|  | ```functions``` | A set of behaviors based on a specified action. | Optional. |
|  | ```macros``` | User-defined placeholders holding strings or values. | Optional. |

type:

Example of these properties in use:

```yaml
title: "Cosmetics Menu"
rows: 6
type: chest
close: false
alias:
- cosmetics
- cosmeticsmenu
```

### 

## Slot-Level Properties

Just below properties, a GUI consists of individual slots (of course, the amount of slots available within a GUI is determined by the ```rows``` top-level property) which represent various sections within the GUI. Slots can inherit characteristics from the top-level GUI, or can have the ability to override those characteristics or have unique characteristics entirely.

Example of Unique Characteristics:

- Notice how both have macros of the same name, but their string values are unique for each slots' desired actions.

```yaml
0:
  macros:
    '%name%': '&aCosmetics'
    '%take-me-to%': 'cosmetics'
  icon: 'DIRT'
  functions:
    broadcast-click:
      type: 'click'
      function:
      - 'gui: %take-me-to%'

1:
  macros:
    '%name%': '&aColored Names'
    '%take-me-to%': 'colored-names'
  icon: 'DIRT'
  functions:
    broadcast-click:
      type: 'click'
      function:
      - 'gui: %take-me-to%'
```