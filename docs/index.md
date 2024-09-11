# Welcome

Welcome to the DynamicGui documentation. To begin, it's recommended that you are familiar with at least one of the following configuration types: yaml, json, xml, or hocon. Examples will be provided for the yaml syntax, although DynamicGui supports all of the previously mentioned file types. For an introduction to working with DynamicGui, refer to the "Getting Started" section, where high-level concepts of writing a GUI will be covered.

## Getting Started

Before delving into DynamicGui, it's essential to grasp the anatomy or components comprising a GUI. At the highest level, GUIs consist of slots, which represent the various sections within the menu. Slots can inherit characteristics from the top-level GUI and also have the ability to override characteristics from the top level GUI. These concept should become clearer as you examine the provided examples. 

### Anatomy of a GUI

In this example, we'll create a GUI with 2 rows named test.yml with an inventory title of "Test Menu". It will feature a single slot containing dirt. When a player clicks on the dirt block, the server will broadcast the message "Test Broadcast".

```yaml
title: 'Test Menu' #The title of the menu
rows: 2 #The amount of rows in the inventory, this will have 18 slots
0:
  icon: 'DIRT'
  functions:
    broadcast-click: #This can be named anything but it should be descriptive
      type: 'click' #The type of function to run
      function:
      - 'Broadcast: Test Broadcast'
```
