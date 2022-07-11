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

<table>
 <tr><H3>Param. Offset Data / Models Content Table (.adsm file type)</h3></tr>
<tr>
<th align="left", width="120">Column:</th>
<th align="center", width="60">1</th>
<th align="center", width="60">2</th>
<th align="center", width="60">3</th>
<th align="center", width="60">4</th>
<th align="center", width="120">5</th>
<th align="center", width="120">6</th>
<th align="center", width="60">7</th>
<th align="center", width="60">8</th>
<th align="center", width="120">9</th>
<th align="center", width="60">10</th>
</tr>
<tr>
 <td><b>Content:</b></td>
 <td align="center">Level</td>
 <td align="center">Order</td>
 <td align="center">Type</td>
 <td align="center">Type Value</td>
 <td align="center">Minimum Value</td>
 <td align="center">Maximum Value</td>
 <td align="center">?*</td>
 <td align="center">Def</td>
 <td align="center">Default Value</td>
 <td align="center">Name</td>
</tr>
<tr>
 <td><b>Data type:</b></td>
 <td align="center">STRING</td>
 <td align="center">INTEGER</td>
 <td align="center">STRING</td>
 <td align="center">INTEGER</td>
 <td align="center">FLOAT</td>
 <td align="center">FLOAT</td>
 <td align="center">INTEGER</td>
 <td align="center">STRING</td>
 <td align="center">FLOAT</td>
 <td align="center">STRING</td>
</tr>
 <tr>
 <td><b>Exemple:</b></td>
 <td align="center">Macro</td>
 <td align="center">2</td>
 <td align="center">Param</td>
 <td align="center">255</td>
 <td align="center">0.01736</td>
 <td align="center">0.9556</td>
 <td align="center">0</td>
 <td align="center">Def</td>
 <td align="center">0.50</td>
 <td align="center">Hold</td>
</tr>
<table>
 
* ? is that binary data ? 0/1, for what ?
 
 
## Instruments Definition: KICK
  
### Main Kick Models Definition

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

### CLIPPED Model ParamOffset (1)
 
<table>
<tr>
<th align="left", width="100">Col. 1</th>
<th align="left", width="100">Col. 2</th>
<th align="left", width="100">Col. 3</th>
<th align="left", width="100">Col. 4</th>
<th align="left", width="100">Col. 5</th>
<th align="left", width="100">Col. 6</th>
<th align="left", width="100">Col. 7</th>
<th align="left", width="100">Col. 8</th>
<th align="left", width="100">Col. 9</th>
<th align="left", width="100">Col. 10</th>
</tr>
<tr>
 <td>Macro</td>
 <td>0</td>
 <td>Param</td>
 <td>257</td>
 <td>0.01738</td>
 <td>0.9556</td>
 <td>0</td>
 <td>Def</td>
 <td>0.0805</td>
 <td>Tune</td>
</tr>
<table> 
 
 
