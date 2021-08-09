# Tutorial "Solina" plugin - Plugin structure JSON/PNG files

This tutorial is intended for **beginner users**. If you have some programming basics, it will help you understand the different terms used here. Also, if your graphic skills allow you to edit and publish beautiful images, feel free to modify some images in the interface. Each theme is located in a separate **folder** containing all the files needed to display the plugin.

![Solina prview](images/structure-solina.jpg)

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
Let´s look at the first page, **6 main controls** for instruments (mix, mute, pan and octave), **2 controls** for EQ (Bass, Upper), and a **set of switches** for Ensemble and Dual Voices, and finally, a **Main volume** knob.

---

Open the **TUI.json** file included into the theme folder.

