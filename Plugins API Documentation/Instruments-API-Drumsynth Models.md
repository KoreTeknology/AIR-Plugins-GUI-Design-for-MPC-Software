[<< Back to main page](/../..)

---

# Drumsynth Models API (2.11x)

## Basic structure of the XPL Presets, ADSM & ADSS Files Contents

Each preset is composed from several parameters and values. We must note that basicaly each type of instruments has differents parameters! Let´s look first at the basic principle of models per type. Each model contains a structured content, including parameters and data.<br>
**.adsm** = Air Drum Synth Model<br>
**.adss** = Air Drum Synth Structure

### Parameters Table

<table>
<tr>
<th align="left", width="130">Parameters</th>
<th align="left", width="650">Description</th>
<th align="center", width="180">Range</th>
<th align="center", width="90">Midi</th>
</tr>
<tr>
 <td  valign="top"><b>Tune</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.000 to 0.000</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Hold</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.000 to 0.000</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Decay</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.000 to 0.000</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Sweep</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.000 to 0.000</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Sweep-Decay</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.000 to 0.000</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Sweep-Depth</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.000 to 0.000</td><td align="center"  valign="top">000</td>
</tr>
<tr>
 <td  valign="top"><b>Harm</b></td>
 <td align="left"  valign="top">desc.</td><td align="center"  valign="top">-0.000 to 0.000</td><td align="center"  valign="top">000</td>
</tr>
<table>

 ### Models Content Table (.adsm file type)
 
 ...
 
 
## Instruments Definition
  
### Kick

Model Name | Parameters | .adsm file | .adss file | Default |
:--------------------------------------- | :--- | :---: | :---: |:---: |
Eighty | *Tune, Hold, Decay, Sweep, Harm, Click, Noise, Noise-color* | Eighty.adsm | Eighty.adss |:heavy_check_mark: |
Ninety | *Tune, Hold, Decay, Sweep, Punch, Harm, Click, Noise* | Ninety.adsm | Ninety.adss |:heavy_check_mark: |
Driven 8 | *Tune, Hold, Decay, Sweep-Decay, Sweep-Depth, Punch, Harm, Drive* | Driven8.adsm | Driven8.adss |:heavy_check_mark: |
Hybrid | *Tune, Hold, Decay, Sweep, Punch, Att-Noise, Att-Time, Att-Dirt* | Hybrid.adsm | Hybrid.adss |:heavy_check_mark: |
Transe | *Tune, Hold, Decay, Hit, Sweep, Sweep-Dec, Noise, Noise-Col* | Transe.adsm | Transe.adss |:heavy_check_mark: |
Natural A | *Tune, Decay, Attack, Body, Beat, Beat-Color, Noise, Noise-Reso* | NaturalA.adsm | NaturalA.adss |:heavy_check_mark: |
Natural B | *Tune, Decay, Body, Beat, Beat-Mid, Noise, Noise-Dec, Noise-Col* | NaturalB.adsm | NaturalB.adss |:heavy_check_mark: |
Hard 1 | *Tune, Hold, Decay, Harm, Dist, Beat, High, Noise* | Hard1.adsm | Hard1.adss |:heavy_check_mark: |
Hard 2 | *Tune, Hold, Decay, Sweep, Click, Hi-Hat, HH-Dec, HH-Tune* | Hard2.adsm | Hard2.adss |:heavy_check_mark: |
Clipped | *Tune, Hold, Decay, Sweep, Clip, Character, Soft, Click* | Clipped.adsm | Clipped.adss |:heavy_check_mark: |
Custom 1 | *Tune, Hold, Decay, Sweep, Clip, Character, Soft, Noise* | Custom1.adsm | Custom1.adss |:x: |
