# KPMG Blue Ocean Gin AR Activation

## About

This project is a collaboration between the students of the VR/AR Developement and Design program at Vancouver Film School and KPMG.

Web based AR activation using [AR.js](https://github.com/jeromeetienne/AR.js) for marker tracking and additional components for [A-Frame](https://aframe.io/), used to display 3D objects through webXR. Assets hosted through [Glitch](https://glitch.com/edit/#!/continuous-ocarina).

## Pages
- index: Landing page, splash screen to ensure people have sound enabled and are provided a pleasent user experience
- ar: This page contains 3D content that forms a cylinder of fish and ocean around the bottle
- videoAR: overlays a pre-rendered video over the AR marker

## Customization

The current QR code/marker we are using directs to my personal website, [itsadam.tech](https://www.itsadam.tech). To update the marker use any QR code generator ([like this one](https://www.the-qrcode-generator.com/)) to create a custom QR code and replace the one found in the Adobe Illustrator file at `assets/patterns/QR_Marker.ai`. Export that new image as a png (make sure to remove any white background from the QR code you created) and upload it to the [marker generator](https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html) with a pattern ratio of 0.87 and an image size of 1024px.

With your new .patt file downloaded, move it into `assets/patterns/`, find the `<a-camera>` element in ar.html and videoAR.html and change the `url` to your new pattern (or simply replace the current .patt file with one of the same name, `pattern-AR_Marker.patt`). Make sure change `<a-scene arjs="patternRatio: x">` if you altered the pattern ratio.

<img src="./assets/patterns/pattern-QR_Marker.png" width="250">

All models are currently hosted through a personal [Glitch](https://glitch.com/) CDN, but I have included the models at `assets/models/` where you can choose to host them as you prefer. Simply update the `src` of each model in their `<a-asset-item>` element of ar.html. External hosting is needed for A-Frame to work properly, rather than direct linking to the file.

## Known Issues
- Touch interaction play for videoAR.html isn't working properly. Video autoplays. Not huge issue, experience still runs.
- Sound recording is poor, very reverb-y
