# Figma guidelines

# **Component variants**

When setting up component variants in Figma, if applicable, the following order and naming convention must be respected for both properties and values. Any component-specific properties should be defined **below** the ones listed in the table.

The general rule of thumb for determining the order of properties is starting with the ones affecting mainly visual attributes (like `Active`, `State`, `Styling`) and moving on towards properties affecting sizing and the functionality of the component (eg. `Size`, `Layout`, `Breakpoint`, other custom properties).

| Property | Values | Description |
| --- | --- | --- |
| `Breakpoint` | - `XXS` (320px)
- `XS` (425px)
- `SM` (768px)
- `MD` (1024px)
- `LG` (1440px)
- `XL` (1920px)
- `XXL` (2560px) | Complex components might require additional variants for different viewport sizes. In such case, the above-mentioned order should be used. |
| `Active` | - `True`
- `False` | Components with "multi-dimensional" `Active` states (eg. a checkbox with a unique set of `Default`, `Hover`, etc. states) must have the `Active` state defined outside of the `State` property. |
| `State` | - `Default`
- `Hover`
- `Pressed`
- `Focus`
- `Active`*
- `Disabled`
- `Loading` | Please note, that not all states are applicable to all components and that is fine.

* — Not applicable, if the `Active` property has been defined above. |
| `Styling` | - `Default`
- `Error`
- `Warning`
etc.

*or...*

- `Primary`
- `Secondary`
- `Teritiary`
- `Error`
- `Warning`
etc. | Some components can come in different styling options (eg. a button). In such case, the above-mentioned values should be used to define this property. |
| `Size` | - `Large`
- `Medium`
- `Small` |  |
| `Layout` | - `Text`
- `Text + Icon`
- `Icon + Text`
- `Icon + Text + Icon`
- `Icon` |  |

# Library update messages

- 🔴 ACTION REQUIRED AFTER UPDATE: [What’s changed and what and what needs to be done]
- 🟠 REVIEW AFTER UPDATE: [What’s changed and what needs to be reviewed]
- 🟢 SAFE TO UPDATE:
    - Examples:
        - 🟢 SAFE TO UPDATE: Inheriting and propagating `FILE NAME` library changes.
- ⚪️ NO CHANGES
    - Examples:
        - ⚪️ NO CHANGES: Inheriting and propagating `FILE NAME` library changes.