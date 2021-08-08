# API 1.1 (08/08/2021) for designing new themes for the AIR plugins

This document presents the keys and values associated with the interactive components of the user interfaces of AIR plugins, present in the latest versions of Akai MPC software. You will find here all the reference information to develop your own graphic themes.

---

## General structure

All plugin´s themes are constructed in the same way, thanks to a list of references (parameters) and a list of components (controls). Each plugin then has a JSON file which links these elements. let's start to see the list of parameters accessible for the plugins that interest us here (Solina, Hype, Drumsynth):

### Solina Parameters <> Fnctions

| fnKeyIndex (Tab/Page) | Keys | Functions (Type)  | Line of Code |
| :---: | :---: | :----------------- | :---: |
| 0 (1/ENSEMBLE) | **Parameter 17** | Contra Bass (btnOn)  | 1818 |
| 0 (1/ENSEMBLE) | **Parameter 18** | Contra Bass Vol (sliderMix)  | 1847 |
| 0 (1/ENSEMBLE) | **Parameter 19** | Contra Bass Pan (knobPan)  | 1876 |
| 0 (1/ENSEMBLE) | **Parameter 20** | Contra Bass Octave (knobOct)  | 1905 |
| 0 (1/ENSEMBLE) | **Parameter 21** | Cello (btnOn)  | 1935 |
| 0 (1/ENSEMBLE) | **Parameter 22** | Cello Vol (sliderMix)  | 1964 |
| 0 (1/ENSEMBLE) | **Parameter 23** | Cello Pan (knobPan)  | 1992 |
| 0 (1/ENSEMBLE) | **Parameter 24** | Cello Octave (knobOct)  | 2021 |
| 0 (1/ENSEMBLE) | **Parameter 1** | Viola (btnOn)  | 2050 |
| 0 (1/ENSEMBLE) | **Parameter 2** | Viola Vol (sliderMix)  | 2079 |
| 0 (1/ENSEMBLE) | **Parameter 3** | Viola Pan (knobPan)  | 2108 |
| 0 (1/ENSEMBLE) | **Parameter 4** | Viola Octave (knobOct)  | 2137 |
| 0 (1/ENSEMBLE) | **Parameter 5** | Violin (btnOn)  | 2166 |
| 0 (1/ENSEMBLE) | **Parameter 6** | Violin Vol (sliderMix)  | 2195 |
| 0 (1/ENSEMBLE) | **Parameter 7** | Violin Pan (knobPan)  | 2224 |
| 0 (1/ENSEMBLE) | **Parameter 8** | Violin Octave (knobOct)  | 2253 |
| 0 (1/ENSEMBLE) | **Parameter 9** | Trumpet (btnOn)  | 2282 |
| 0 (1/ENSEMBLE) | **Parameter 10** | Trumpet Vol (sliderMix)  | 2311 |
| 0 (1/ENSEMBLE) | **Parameter 11** | Trumpet Pan (knobPan)  | 2340 |
| 0 (1/ENSEMBLE) | **Parameter 12** | Trumpet Octave (knobOct)  | 2369 |
| 0 (1/ENSEMBLE) | **Parameter 13** | Horn (btnOn)  | 2398 |
| 0 (1/ENSEMBLE) | **Parameter 14** | Horn Vol (sliderMix)  | 2427 |
| 0 (1/ENSEMBLE) | **Parameter 15** | Horn Pan (knobPan)  | 2456 |
| 0 (1/ENSEMBLE) | **Parameter 16** | Horn Octave (knobOct)  | 2485 |
| 0 (1/ENSEMBLE) | **Parameter 0** | Ensemble (btnEnsemble)  | 2514 |
| 0 (1/ENSEMBLE) | **Parameter 26** | Volume Bass (sliderMix)  | 2543 |
| 0 (1/ENSEMBLE) | **Parameter 25** | Split/Dual (btnDual)  | 2572 |
| 0 (1/ENSEMBLE) | **Parameter 27** | Volume upper (sliderMix)  | 2601 |
| 0 (1/ENSEMBLE) | **Parameter 70** | Master Level (knobLg)  | 2630 |
|  |  |  |  |
| 1 (2/SOUND) | **Parameter 28** | Crescendo (sliderSound)  | 2723 |
| 1 (2/SOUND) | **Parameter 29** | Sustain (sliderSound)  | 2752 |
| 1 (2/SOUND) | **Parameter 30** | Formant (sliderSoundBi)  | 2781 |
| 1 (2/SOUND) | **Parameter 31** | Filter (sliderSound)  | 2810 |
| 1 (2/SOUND) | **Parameter 32** | Age (sliderSound)  | 2839 |
| 1 (2/SOUND) | **Parameter 33** | Vel -> Amp (knobLg)  | 2868 |
| 1 (2/SOUND) | **Parameter 34** | MW Vibrato (knobLg)  | 2897 |
| 1 (2/SOUND) | **Parameter 35** | AT Vibrato (knobLg)  | 2926 |
| 1 (2/SOUND) | **Parameter 36** | Vibrato SPeed (knobLg)  | 2955 |
| 1 (2/SOUND) | **Parameter 69** | Sample Poly (valueSlider)  | 2984 |
|  |  |  |  |
| 2 (3/FLAVOR) | **Parameter 42** | Flavor On (btnOn)  | 3076 |
| 2 (3/FLAVOR) | **Parameter 43** | Flavor Timbre (flavorType)  | 3105 |
| 2 (3/FLAVOR) | **Parameter 44** | Flavor Depth (sliderSound)  | 3134 |
| 2 (3/FLAVOR) | **Parameter 45** | Flavor Vinyl Dist (knobLgTall)  | 3163 |
| 2 (3/FLAVOR) | **Parameter 46** | Flavor Vinyl Noise (knobLgTall)  | 3192 |
| 2 (3/FLAVOR) | **Parameter 47** | Flavor Flutter (knobLgTall)  | 3221 |
| 2 (3/FLAVOR) | **Parameter 48** | Flavor Monofy (knobLgTall)  | 3250 |
|  |  |  |  |
| 3 (4/CHORUS/EQ) | **Parameter 37** | Chorus On (btnOn)  | 3341 |
| 3 (4/CHORUS/EQ) | **Parameter 38** | Chorus Rate (sliderFx)  | 3370 |
| 3 (4/CHORUS/EQ) | **Parameter 39** | Chorus Depth (sliderFx)  | 3399 |
| 3 (4/CHORUS/EQ) | **Parameter 40** | Chorus Tone (sliderFx)  | 3428 |
| 3 (4/CHORUS/EQ) | **Parameter 41** | Chorus Mix (sliderFx)  | 3357 |
| 3 (4/CHORUS/EQ) | **Parameter 49** | EQ On (btnOn)  | 3486 |
| 3 (4/CHORUS/EQ) | **Parameter 50** | EQ Low (sliderFx)  | 3515 |
| 3 (4/CHORUS/EQ) | **Parameter 51** | EQ Low Mid (sliderFx)  | 3544 |
| 3 (4/CHORUS/EQ) | **Parameter 52** | EQ High Mid (sliderFx)  | 3573 |
| 3 (4/CHORUS/EQ) | **Parameter 53** | EQ high (sliderFx)  | 3602 |
| 3 (4/CHORUS/EQ) | **Parameter 54** | Delay On (btnOn)  | 3631 |
| 3 (4/CHORUS/EQ) | **Parameter 62** | Spring Reverb (btnOn)  | 3660 |
|  |  |  |  |
| 4 (5/DELAY/REVERB) | **Parameter 54** | Delay On (btnOn)  | 3752 |
| 4 (5/DELAY/REVERB) | **Parameter 55** | Delay Time (sliderFx)  | 3781 |
| 4 (5/DELAY/REVERB) | **Parameter 56** | Delay L/R Ratio (sliderFx)  | 3810 |
| 4 (5/DELAY/REVERB) | **Parameter 57** | Delay Feedback (sliderFx)  | 3839 |
| 4 (5/DELAY/REVERB) | **Parameter 58** | Delay Reso LP Freq (knobLgTall)  | 3868 |
| 4 (5/DELAY/REVERB) | **Parameter 59** | Delay Reso Bell Freq (knobLgTall)  | 3897 |
| 4 (5/DELAY/REVERB) | **Parameter 60** | Delay Reso Bell Gain (knobLgTall)  | 3926 |
| 4 (5/DELAY/REVERB) | **Parameter 61** | Delay Mix (sliderFx)  | 3955 |
| 4 (5/DELAY/REVERB) | **Parameter 62** | Spring Reverb (btnOn)  | 3984 |
| 4 (5/DELAY/REVERB) | **Parameter 63** | Reverb Pre-Dealy (sliderFx)  | 4013 |
| 4 (5/DELAY/REVERB) | **Parameter 64** | Reverb Time (sliderFx)  | 4042 |
| 4 (5/DELAY/REVERB) | **Parameter 65** | Reverb Low Cut (sliderFx)  | 4071 |
| 4 (5/DELAY/REVERB) | **Parameter 66** | Reverb Diffusion (sliderFx)  | 4100 |
| 4 (5/DELAY/REVERB) | **Parameter 67** | Reverb Width (sliderFx)  | 4129 |
| 4 (5/DELAY/REVERB) | **Parameter 68** | Reverb Mix (sliderFx)  | 4158 |
| 4 (5/DELAY/REVERB) | **Parameter 37** | Chorus On (btnOn)  | 4187 |
| 4 (5/DELAY/REVERB) | **Parameter 49** | EQ On (btnOn)  | 4216 |


