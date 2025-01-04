# Introdunction to Macros

Macros, macros, macros.. They certainly make your configuration life easier. From simple to complex GUIs, you can count on macros to increase ease of GUI production as well for GUI configuration and maintenance, such as making user-defined placeholders to keep easy-to-remember or easy-to-recall values or strings, lists of functions, or an entire section of functions. You can even use macros within a macro to increase customization!

## **Types of Macros**

There are three macro types: String Macros, List Macros, and Section Macros.

## 1. String Macros

String Macros are the most basic type of macros. They act as placeholders to keep basic or lengthy values or strings.

Examples of String Macros:

```yaml
macros:
  '%name%': 'Your name is: %prefix% %player%'
  '%prefix%': '%luckperms_prefix%'
```

*Note:* ```%prefix%``` *placeholder may vary on your plugin needs. If you're using luckperms, you may use* ```%luckperms_prefix%``` *in lieu. You can also macro these long plugin placeholders for your own.*

###

## 2. List Macros

List macros are useful for a lengthy list of functions like checks and conditions.

Example of a List Macro:

```yaml
macros:
  '%function-list%':
  - 'HasPermission: permission.check'
  - 'pmsg: You do have permission for this.'
  - 'Broadcast: Hey everybody! %player% has permission for this!'
```

###

## 3. Section Macros

Section Macros contain an entire section of functions typically for a particular slot, but can be called for use by any slot. Instead of repetative copy-and-paste functions where the intent for multiple slot items to use identical functions, a Section Macro can be used.

Section Macro syntax is List Macros you read about above. However, your value cannot be within apostrophies or quotations -- these are to be placed within the slot item function call.

Full Example of a Section Macro:

- With this example, when you click on slot 4 with paper as the icon, the Section Macro will be executed by messaging the player because it was called as a function with the slot item being clicked, assuming your ping is equal to or less than 50. If your ping is higher than 50, it will instead message the player saying your ping is too high.

```yaml
macros:
  '%macro-ping%':
  - 'pmsg: Your ping is too high.'
  '%macro-function1%':
    clicker:
      type: "click"
      functions:
      - 'condition: %essentials_ping% <= 50'
      - 'pmsg: %name%'
      function-failure-ping:
        fail-on: 'condition: %essentials_ping% <= 50'
        type: "fail"
        functions:
        - '%macro-ping%'

'4':
  macros:
    '%name%': 'Your name is %prefix% %player%.'
    '%prefix%': '%luckperms_prefix%'
  icon: paper
  name: '%name%'
  functions: "%macro-condition1%"
```