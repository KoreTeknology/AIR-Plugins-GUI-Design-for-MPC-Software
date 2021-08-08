# API (Mini) for designing new themes for the AIR plugins

This document presents the keys and values associated with the interactive components of the user interfaces of AIR plugins, present in the latest versions of Akai MPC software. You will find here all the reference information to develop your own graphic themes.

---

## General structure

All plugin´s themes are constructed in the same way, thanks to a list of references (parameters) and a list of components (controls). Each plugin then has a JSON file which links these elements. let's start to see the list of parameters accessible for the plugins that interest us here (Solina, Hype, Drumsynth):

### Solina Parameters

| fnKeyIndex (Tab/Page) | Keys | Functions (Type)  | Line of Code |
| :---: | :---: | :----------------- | :---: |
| 0 (1/ENSEMBLE) | **Parameter 17** | Contra Bass (btnOn)  | 1818 |
| 0 (1/ENSEMBLE) | **Parameter 18** | Contra Bass Vol (sliderMix)  | 1847 |
| 0 (1/ENSEMBLE) | **Parameter 19** | Contra Bass Pan (knobPan)  | 1876 |
| 0 (1/ENSEMBLE) | **Parameter 20** | Contra Bass Octave (knobOct)  | 1905 |
|  |  |  |  |
| 0 (1/ENSEMBLE) | **Parameter 21** | Cello (btnOn)  | 1935 |
| 0 (1/ENSEMBLE) | **Parameter 22** | Cello Vol (sliderMix)  | 1964 |
| 0 (1/ENSEMBLE) | **Parameter 23** | Cello Pan (knobPan)  | 1992 |
| 0 (1/ENSEMBLE) | **Parameter 24** | Cello Octave (knobOct)  | 2021 |
|  |  |  |  |
| 0 (1/ENSEMBLE) | **Parameter 1** | Viola (btnOn)  | 2050 |
| 0 (1/ENSEMBLE) | **Parameter 2** | Viola Vol (sliderMix)  | 2079 |
| 0 (1/ENSEMBLE) | **Parameter 3** | Viola Pan (knobPan)  | 2108 |
| 0 (1/ENSEMBLE) | **Parameter 4** | Viola Octave (knobOct)  | 2137 |
|  |  |  |  |
| 0 (1/ENSEMBLE) | **Parameter 5** | Violin (btnOn)  | 2166 |
| 0 (1/ENSEMBLE) | **Parameter 6** | Violin Mix (sliderMix)  | 2195 |
| 0 (1/ENSEMBLE) | **Parameter 7** | Violin Pan (knobPan)  | 2224 |
| 0 (1/ENSEMBLE) | **Parameter 8** | Violin Octave (knobOct)  | 2253 |
|  |  |  |  |
| 0 (1/ENSEMBLE) | **Parameter 9** | Violin Octave (knobOct)  | 2253 |
