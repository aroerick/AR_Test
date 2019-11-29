# KPMG Blue Ocean Gin AR Activation

## About

This project is a collaboration between the students of the VR/AR Developement and Design program at Vancouver Film School and KPMG.

Web based AR activation using [AR.js](https://github.com/jeromeetienne/AR.js) for marker tracking and additional components for [A-Frame](https://aframe.io/), used to display 3D objects through webXR. Assets hosted through [Glitch](https://glitch.com/edit/#!/continuous-ocarina).

## Pages
- index: Landing page, splash screen to ensure people have sound enabled and are provided a pleasent user experience
- ar: This page contains 3D content that forms a cylinder of fish and ocean around the bottle
- videoAR: overlays a pre-rendered video over the AR marker

## Customization

In ar.html and videoAR.html, within the `<a-marker-camera>` element, change the `url` if you would like to use a custom marker pattern. Also make sure change `<a-scene arjs="patternRatio: x">` to match your custom marker.

## Known Issues
- Stability on ar.html is very low. Need to optimize textures, models, and marker.
- Landing page currently only works on mobile. Update for tablet and a "Please switch to mobile" message for desktop
- Touch interaction play for videoAR.html isn't working at all. Video autoplays.
- Sound recording is poor, very reverb-y
- Ocean floor needs texture lightened
