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

Before we do any modification to the plugin,
