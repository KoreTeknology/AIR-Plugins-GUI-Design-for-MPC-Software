# Tutorial "Solina" plugin - Plugin structure JSON/PNG files

This tutorial is intended for **beginner users**. If you have some programming basics, it will help you understand the different terms used here. Also, if your graphic skills allow you to edit and publish beautiful images, feel free to modify some images in the interface. Each theme is located in a separate **folder** containing all the files needed to display the plugin.

![Solina prview](images/mpc-plugins-effects-solina-img.png)


The **"SOLINA PLUGIN SKINS"** folder includes:

## The background:

| BACKGROUNDS | Page 1  | Page 2  | Page 3  | Page 4  | Page 5  | Dimensions (px) |
| --- | --- | --- | --- | --- | --- | :---: |
| BG Pages: | fbank_01.png | fbank_02.png | fbank_03.png | fbank_04.png | fbank_05.png | **1280x630** |

## The Switch buttons:

| GUI Elements: Switches (Buttons with 2 states) | Images OFF  | Images ON  | Dimensions (px) |
| --- | --- | --- | :---: |
| Instrument Switch: | btn_off.png  |  btn_on.png | **70x70** |
| Ensemble Switch: | btn_off.png  |  btn_ensemble.png | **70x70** |
| Dual Switch: | btn_off.png  |  btn_dual.png | **70x70** |

## The Sliders and Knobs:

| GUI Elements: Sliders & Knobs (Vertical steps) | Images  | Dimensions (px) |
| --- | --- | :---: |
| Flavor Slider: | flavor.png  | **216x7360** |
| Knob: | knob.png  | **127x16129** |
| Octave knob: | knob_octave.png  | **75x225** |
| Pan knob: | knob_pan.png  | **92x11684** |
| Slider Long: | slider_long.png  | **80x31115** |
| Slider Short: | slider_short.png  | **80x31115** |

## The structured data/setup files:

| GUI structure: JSON files |  Data | Weight (Kb) |
| --- | --- | :---: |
| Main: | TUI.json  | **192** |
| Qlinks: | Q-Links.json | **4.28** |
| Extra: | Q-Links - 8by1.json | **4.28** |

---

# Customizations and Compositions

Before we do any modification to the plugin, let s have a look at the **design file** structure. We will use this JSON programming language all over this tutorial, if you are not familiar with it, i suggest you to visit the [Introducing JSON Website](https://www.json.org/json-en.html) and learn from the ground how it is made and what are the benefit of using this data file format.

The main Object is a **"PageData" container**, it has 4 sections:
- version
- componentDefinitions
- info
- tabs

Each one contains some sort of data to publish a user interface for the plugin.
```diff 
! from there, you must understand that we cannot add more features than it has before
! you can only change the visual aspect of the GUI elements !!!
```

---

**Let´s see in detail, what is there and what we can do or modify to get the desired effect or interface composition.**

- [x] The "version" section only contains a single number as "data object referencing tag".

- [x] The "componentDefinitions" first load some external files as libraries, then describe all the components or graphical elements on the plugin that do an action or interaction with the user. It is based on key-value relationship by design.

- [x] The "info" section presents the type of content, it can be a main file or a secondary file.

- [x] The "tabs" section presents the general images structure, by placing accuratly the graphics at the good place and at the good size. This section is especialy interesting because of the potential of moving controls and re-structure the whole plugin*

*by this technique, you can make a single page plugin and place all the controls over it ;)
```diff 
- Dont create a plugin that will not fit the Akai MPC Software maximum dimensions in pixels > 1280x629px
```
---

Now, we understand how to modify our plugin GUI, to accomodate the design to our preferences. The next step is start applying changes, but before that, dont forget to make a copy of the original folder !!! Let´s go for the plugin **"SOLINA"** :) I personaly dont like the original design of this nice little synth, the poor and non-logical graphic design and the complete chaos in the page contents organisation... but this is how i feel, doesn t mean we are equal on those feelings.

It has 5 pages in a row, from left to right **(6400x629px)**, this is a huge surface!
Let´s look at the first page, **6 main controls** with strange shapes with basic synthesis params, **8 controls** for filter, distortions, Fx and Master Volume, and a **set of switches** for each section of the synth. Well, let´s try something simple, edit the first param-control: **"layer {oscillators} mix"**!

---

Open the **TUI.json** file included into the theme folder.
Where are located the content for this control in this file? search for:

## 5 Pages/Tabs Plugin:

```yaml
"page 1": "ENSEMBLE"
"page 2": "SOUND"
"page 3": "FLAVOR"
"page 4": "CHORUS/EQ"
"page 5": "DELAY/REVERB"
```

## Various types of components used in this GUI:
```yaml
- btnOn
- btnEnsemble
- btnDual
- valueSlider
- comboBox
- flavorType
- knobPan
- sliderMix
- sliderSound
- sliderFx
- sliderSoundBi
- knobLg
- knobLgTall
- knobOct
```

![sepratator](https://github.com/KoreTeknology/AIR-Plugins-GUI-Design-for-MPC-Software/blob/main/Documentation/images/separator.png)

## Exemple: 1 Tab (various Sub-components)
```yaml
Line 3021 - Component >>> "fnKeyIndex": 2
"tabName": "FLAVOR"
"colour": "ff1e1d1e"
"image": ""


Line 3045 - Sub-component >>> "type": "Image"
"name": "Image"
"value": "Invalid"
"image": "fbank_03_bg.png"
"bounds": "0 0 1280 630"

Line 3077 - Sub-component >>> "type": "btnOn"
"name": "Flavor On"
"value": "Parameter 42"
"bounds": "1074 68 121 74"

Line 3106 - Sub-component >>> "type": "flavorType"
"name": "Flavor Timbre"
"value": "Parameter 43"
"bounds": "122 241 216 230"

Line 3134 - Sub-component >>> "type": "sliderSound"
"name": "Flavor Depth"
"value": "Parameter 44"
"bounds": "357 298 121 295"

Line 3163 - Sub-component >>> "type": "knobLgTall"
"name": "Flavor Vinyl Dist"
"value": "Parameter 45"
"bounds": "509 370 155 217"

Line 3192 - Sub-component >>> "type": "knobLgTall"
"name": "Flavor Vinyl Noise"
"value": "Parameter 46"
"bounds": "669 370 155 217"

Line 3221 - Sub-component >>> "type": "knobLgTall"
"name": "Flavor Flutter"
"value": "Parameter 47"
"bounds": "829 270 155 217"

Line 3250 - Sub-component >>> "type": "knobLgTall"
"name": "Flavor Monofy"
"value": "Parameter 48"
"bounds": "989 270 155 217"
```
![sepratator](https://github.com/KoreTeknology/AIR-Plugins-GUI-Design-for-MPC-Software/blob/main/Documentation/images/separator.png)

## Exemple: 1 Type (slider built on 3 Sub-components)
```yaml
Line 928 - "key": "sliderSound"
size= 80x245px

Line 971 - Focus
"name": "Focus"
"type": "Focus"
"backgroundColour": "10ffffff"
"outlineColour": "ffe81f40"
"backgroundInset": 4.0
"outlineThickness": 1.0

Line 998 - Knob
"name": "Knob"
"type": "Knob"
"knobType": "FilmStrip"
"filmStrip": "slider_long.png"
"numFrames": 127
"bounds": "20 0 80 245"

Line 1026 - Data Bloc 
"name": "Label"
"type": "Label"
"name": "Titillium Web"
"style": "SemiBold"
"height": 24.0
"colour": "ffffffff"
"justification": "horizontallyCentred verticallyCentred"
"bounds": "0 255 121 28"
```
