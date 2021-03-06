# DesktopFormFactor element

Specifies the settings for an add-in for the desktop form factor. The desktop form factor includes Office for Windows, Office for Mac, and Office Online. It contains all the add-in information for the desktop form factor except for the  **Resources** node.

Each DesktopFormFactor definition contains the  **FunctionFile** element and one or more **ExtensionPoint** elements. For more information, see [FunctionFile element](./functionfile.md) and [ExtensionPoint element](./extensionpoint.md). 

## Child elements

| Element                               | Required | Description  |
|:--------------------------------------|:--------:|:-------------|
| [ExtensionPoint](./extensionpoint.md) | Yes      | Defines where an add-in exposes functionality. |
| [FunctionFile](./functionfile.md)     | Yes      | A URL to a file that contains JavaScript functions.|
| [GetStarted](./getstarted.md)         | No       | Defines the callout that appears when installing the add-in in Word, Excel, or PowerPoint hosts. |

## DesktopFormFactor example

```xml
...
<Hosts>
  <Host xsi:type="Presentation">
    <DesktopFormFactor>
      <FunctionFile resid="residDesktopFuncUrl" />
      <GetStarted>
        <!-- GetStarted callout -->
      </GetStarted>
      <ExtensionPoint xsi:type="PrimaryCommandSurface">
        <!-- information on this extension point -->
      </ExtensionPoint> 
      <!-- possibly more ExtensionPoint elements -->
    </DesktopFormFactor>
  </Host>
</Hosts>
...
```
