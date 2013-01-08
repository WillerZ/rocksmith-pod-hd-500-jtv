£50 Game, £1500 Peripheral
==========================

These are the patches I use on my Pod HD-500 to make it easier to play
Rocksmith with my JTV-69.

Connections
-----------
The patches assume that you have connected your Variax to the VARIAX
socket with a VDI cable. You should connect the Rocksmith RealTone cable
to the FX SEND of your Pod HD-500. For best results, connect the
RealTone cable for your guitar only to the Left channel of the FX SEND.

You may optionally also connect a Bass to the GUITAR socket of the Pod
HD-500. If you do so, be sure to split the FX SEND into Left and Right
mono channels and connect the RealTone cables correctly (Left = Guitar,
Right = Bass).

You do not need to connect anything to the FX RETURN inputs. Anything
you do connect will be disregarded by these patches.

General Structure of all Patches
--------------------------------

Input 1 is set to Variax.
The Variax model, tuning, and tone level are customised by the patch.
The Variax volume, tone, and toggle controls are locked.

Input 2 is set to Guitar.
The Guitar socket input impedance is set to 1MΩ.

The FX Loop is one of the first effects blocks in the patch.
The MIX parameter of the FX Loop is set to 0%.

Control Conventions
-------------------
The Variax TONE control adjusts the Open and Close levels of the noise
gate in the patch, if any. Turn the TONE knob up to make the gate more
aggressive and down to make it less aggressive.

If a noise gate is present in the patch, FS1 controls whether or not it
is enabled.

Pre-Rocksmith Effects
---------------------
I am going to avoid putting tone-altering effects blocks before the FX
Loop so as not to disrupt Rocksmith's note detection.

All effects produce output on both the left and right channels if there
is input on either channel. This means that in order to place effects
before the loop without compromising the channel separation we have to
use the A and B paths and place the FX Loop after the mixer. This
applies even if the effects on paths A and B are identical in every way.

Unfortunately if we do this it means that we can't process the Guitar
and Bass separately post-Rocksmith.

There are some useful non-disruptive effects, in particular the Hard
Gate is a good way to cut down on unwanted noise during the quiet bits
of high-gain tracks.

Post-Rocksmith Effects
----------------------
After the FX Loop you will find the tone-altering effects blocks.
Guitar-altering blocks go into the top path (Path A) and Bass-altering
blocks go into the lower path (Path B). Anything which applies equally
to both can go in the common section after the paths come back together.
The common path before the paths split cannot be used because all
effects blocks produce output on both channels when there is input on
either channel – this ruins the Guitar/Bass signal separation.
