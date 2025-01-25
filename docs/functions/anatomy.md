# Function Anatomy
Functions can be used for either Top-Level or Slot-Level behavior but the result is similar in nature.

| Function Properties | Description |
| :---- | :---- |
| Function Headers | Function Headers are a required function property, but are essential to sectioning certain functions. An added benefit is that these Function Headers can be named whatever you want. It is best to keep these descriptive as they will help aid in potential troubleshooting or updating. |
| Types | Types are the different function types to determine how the GUI is desired to behave. You can have either a single type in the form of a string, or, you can have types in the form of a list. These are the different available types: ```switch_menu``` ```load``` ```click``` ```left``` ```right``` ```middle``` ```shift_click``` ```shift_left``` ```shift_right``` ```fail``` ```exit_menu``` |
| Functions | This is where you will place your functions. You can have either a single function in the form of a string, or, you can have functions in the form of a list. |
| Fail-On | The specified function where its condition was not expected or met. Whenever you need a function to occur based on a condition not expected, you will need to use the ```fail``` type. |

## Top-Level Functions
Example of Top-Level functions:

```yaml
functions:
  broadcast-load: #This is a Function Header.
    type: "load" #This is a type, using the 'load' type. 
    functions:
    - 'HasPermission: essentials.broadcast' #This is a list function.
  broadcast-click: #This can be named anything but it should be descriptive
    type: #This is a type, using the 'left' and 'right' types in the form of a list function.
    - "left"
    - "right"
    functions:
    - 'Broadcast: This is an important broadcast.' #This is a list function.
    function-failure-permission: #This is also a Function Header
      fail-on: "fail" #This is the fail type.
      functions: "Pmsg: Insufficient permission." #This is a string function.
```

## Slot-Level Functions
Example of Slot-Level functions:

```yaml
'13':
  icon: paper
  name: "tutorial"
  functions:
    loader: #This is a Function Header.
      type: "load" #This is a type, using the 'load' type in the form of a string function.
      functions: #This is a list function.
      - 'permission: tutorial'
      - 'setlore: &cUNLOCKED'
      function-fail-permission: #This is also a Function Header
        fail-on: 'permission: tutorial' #This is a function in which its condition was not met, while also utilizing a string function.
        type: "fail" #This is a type, using the 'fail' type.
        functions: "setlore: &cLOCKED" #This is a function.
    clicker: #This is a Function Header.
      fail-on:
      - 'permission: tutorial' #This is a function in which its condition was not met, while also utilizing a list function.
      type: "click" #This is a type, using the 'click' type in the form of a string function.
      functions: #This is a list function.
      - 'pmsg: Insufficient permission.'
      - 'sound: ENTITY_BLAZE_HURT,1.0,2.0'
```