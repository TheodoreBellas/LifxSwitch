# LIFXSwitch
A small, somewhat-hastily-written PHP client for the LIFX API (V1).

# Features
- Use your LIFX Cloud Key to manage/interact with all the lights associated to your account.
- Turn lights on/off, modify brightness, and change colors to within an almost-reasonable degree of accuracy.

# Usage
```
<?php
$LifxSwitch = new LifxSwitch("your_lifx_token_here");

// Toggle power to all lights
$LifxSwitch->togglePowerAll();

// Toggle power to a single light, where $lightId is the ID string of the light to target
$LifxSwitch->togglePowerSingle($lightId)

// Set light state, used for changing brightness/color/temperature of a single light
$brightess = "0.50";
$temperature = "2200";
$color = [
'h' => "<hue>",
's' => "<saturation>",
'v' => "<variance>",
];

$LifxSwitch->setState($lightId, $colorArray, $brightness, $temperature);
```
