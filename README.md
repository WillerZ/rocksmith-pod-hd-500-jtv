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

It is also important that any effects before the loop are
stereo-in/stereo-out and do not mix their left- and right- channels at
all so that the Guitar/Bass separation is maintained.

There are some useful tonally-neutral effects, in particular the Hard
Gate: it is a good way to cut down on unwanted noise during the quiet
bits of Plug In Baby and other high-gain tracks. I am not as sure as I
would like to be that this is a non-channel-mixing stereo-in stereo-out
effect.

Post-Rocksmith Effects
----------------------
After the FX Loop you will find the tone-altering effects blocks.
Guitar-altering blocks go into the top path (Path A) and Bass-altering
blocks go into the lower path (Path B). Anything which applies equally
to both can go in the common section after the paths come back together.
The common path before the paths split can only be used for
non-channel-mixing stereo-in stereo-out effects that need to apply to
both instruments.
