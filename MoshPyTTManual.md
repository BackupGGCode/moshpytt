# Introduction #

moshPyTT is an editor for Tesseract boxfiles. The main window consists of two parts: the image pane, where the image associated with the boxfile is displayed, and the text pane, where the boxfile's text is displayed.

# Running moshPytt #

moshPyTT does not need installing. You simply run it using the following:

```
./moshpytt.py
```

## Command-line options ##

### Image name ###
You can provide an image name to moshPyTT using the `-i` parameter:

```
./moshpytt.py -i eng.example.001.tif
```

### Debugging ###
Some debugging information can be obtained by giving the `-d` flag. This is unlikely to be useful unless you are trying to improve moshPyTT's code.

# Viewing boxes #

If you place your cursor into the text pane, the box described by that line will be drawn on top of the image in the image pane. If you select a range of boxes with your mouse, all the selected boxes will be shown.

# Editing boxes #

You can edit boxes in several ways.

## Direct editing ##
Firstly, you can directly edit the boxfile's text in the text pane. The new box will be shown immediately in the image pane. This is the only way to edit the text in the box, but you can also edit the dimensions of the box in this way.

## Keyboard shortcuts ##

There are keyboard shortcuts for editing the dimensions of boxes. You can stretch, shrink, move, merge, split and delete boxes using shortcut keys. The shortcut keys are arranged to use the number-pad for ease of remembering, but the "normal" number keys are also usable if you don't have a numpad.

  * Directions: 8 - Up, 4 - Left, 6 - Right, 2 - Down, 5 - All
  * Ctrl-direction: Stretch box in direction
  * Ctrl-shift-direction: Shrink box in direction
  * Alt-direction: Move box in direction

  * Ctrl-0: Delete selected boxes
  * Ctrl-1: Merge selected boxes
  * Ctrl-3: Split selected boxes

  * Ctrl-Z: Undo change
  * Ctrl-Y: Redo change

The merge, split and delete options are also accessible by the "Edit" menu.

## Text attributes ##

You can add text attributes (bold, italic and underline) by clicking the checkboxes in the bottom left corner.

## Finding text ##

You can use the text box in the bottom right corner to find a given string in the boxfile, which can be very useful when looking for a box with an incorrect string which is upsetting the training process.

## Saving boxfiles ##

You can save boxfiles by pressing Ctrl-S or choosing "File>Save". If you save the boxfile as, the boxfile will be saved with a new name, and the image file will be copied to match it.

If you make changes and close the program, you will be prompted to save your changes.

moshPyTT autosaves your work regularly. If the program exits improperly, the autosave file will remain, and you can continue near where you left off. If moshPyTT exits properly, whether or not you choose to save your changes, the autosave file will be removed.