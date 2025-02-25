# Fan Control

<p align=center>
  <img src="Images/logo.gif" width=60/>
</p>
<p align=center>This is the release repository for Fan Control, a focused and highly customizable fan controlling software for Windows.</span>

<br>
<br>

[![Download](https://img.shields.io/badge/Download-FanControl-green.svg?style=flat&logo=download)](/FanControl.zip?raw=true)
[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg?style=flat&logo=paypal)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=N4JPSTUQHRJM8&currency_code=USD&source=url&item_name=Fan+Control)


## Main features

* Guided __setup__ process on first launch
* Save, edit and load multiple __profiles__
* Change the __theme__ and __color__ to fit your setup
* Multiple temperature __sources__ ( CPU, GPU, motherboard, hard drives... )
* Multiple fan curve __[functions](#fan-curve-types)__, including a custom __[graph](#graph-fan-curve-editor)__
* __Mix__ fan curves or sensor togethers (max, min, average)
* Low ressource usage
* Advanced tuning with steps, start %, stop %, response time and hysteresis

![Fan Control](Images/MainUI.png)

## New
* __Configurable temperature range for graphs__
* Decimal support in graphs
* Nickname any temperature sensor from the sensor settings dialog
* Auto fan curve (BETA): Automatically adjust speed to keep target temperature
* Sensor settings dialog window. Activate or deactivate specific sources.

## Installation

1. [Download the latest archive](/FanControl.zip?raw=true)
2. Extract to the desired installation folder
3. Start FanControl.exe
4. (Optional) -c or --config [json config file] command line arg 

## Plugins

 The plugin system let you inject any type of sensor into FanControl, see [Plugins wiki](https://github.com/Rem0o/FanControl.Releases/wiki/Plugins)

 Some examples:
* https://github.com/Rem0o/FanControl.HWInfo
* https://github.com/Rem0o/FanControl.DellPlugin
* https://github.com/medevil84/FanControl.AquacomputerHighFlowNext

## Issues and hardware compatibility

* I am not the main developer for the driver/backend portion of this software. Fan Control is basically a UI on top of existing hardware libraries. Any issue regarding hardware compatibility entirely depends on:
  * https://github.com/LibreHardwareMonitor/LibreHardwareMonitor
  * https://github.com/falahati/NvAPIWrapper
  
* Please only open issues for the software itself, UI, feature request and so on.
* If you do have a hardware compatibility request and you can provide a __working__ sample of code that can be used in .NET, like with a [Plugin](https://github.com/Rem0o/FanControl.Releases/wiki/Plugins), then feel free to submit that.

## FAQ
* __Q__: There is no control cards / control cards are missing / control cards are not changing my fan speeds, what's the issue?
<br>__A__: See section above.

* __Q__: How does __[FAN CURVE TYPE]__ works and what does its parameters do?
<br>__A__: Click on its card's icon at the top left, a dialog will tell you.
* __Q__: Does it run on my OS?
<br>__A__: If your OS is Windows 10 __Or 11__, yes.

## Fan curve types

* (NEW) Auto: PI-ish type function. % will surf until temp is stable at load. 
* Linear : Temperature based linear function
* Graph : Temperature based custom curve
* Target: Temperature based that holds speed until target temperature is reached
* Mix : Use two different curves and apply a mix function (Min, Max, Sum, Average)
* Sync : Sync to an existing control
* Flat: Set a fixed %

## Graph fan curve editor

* (NEW) Change the temperature range for finer control over a small range
* Add, remove and drag points arround the graph
* Copy and paste points from a graph to another
* Fine-tune the response with the hysteresis and response time parameters

![Fan Control](Images/GraphDialog.png)

## Libraries used:
* https://github.com/LibreHardwareMonitor/LibreHardwareMonitor
* https://github.com/MaterialDesignInXAML/MaterialDesignInXamlToolkit
* https://github.com/falahati/NvAPIWrapper
