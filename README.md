# YumeInput
A enhanced input wrapper for Unity3D

#### Requirements
*YumeInput* requires a Unity3D Project installed.

#### How to use
*YumeInput* has been developed to be simple and easy to setup and use.
##### Setup
1) Add a YumeInputBridge conponent to the object you want to control.
2) Give that YumeInputBridge the PlayerIndex of the player you want to control it (1 for player 1, 2 for plyer 2)
3) In your main object's code add a global YumeInputBridge named yinput
4) In your main object's start function add these 2 lines:
```cs
yinput = GetComponent<YumeInputBridge>();
yinput.SetPlayerIndex(1);
yinput.core = new YumeInputCore();
```
5) in your main object's update function add this line, run the project and press button 3 on your controller:
```cs
if(yinput.GetButtonDown(3)) Debug.Log("Button 3 down!");
```
