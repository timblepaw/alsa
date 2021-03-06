AlsaApps
========

### From the ALSA wiki

Jump to: [navigation](#mw-head), [search](#p-search)

This is just a seed page to start any threads about ALSA based apps. For
now, just throw any notes anywhere and they will get organised
eventually, or, by all means, get down and seriously add some pages if
you feel so inclined. Here's a link to the apps section of the official
ALSA webpage:

[http://www.alsa-project.org/applications.php3](http://www.alsa-project.org/applications.php3)

Here's a link to the apps section of the jack website [might be of
interest]:

[http://jackit.sourceforge.net/apps/](http://jackit.sourceforge.net/apps/)

Contents
--------

-   [1 Ardour](#Ardour)
-   [2 Jack](#Jack)
-   [3 Muse](#Muse)
-   [4 Ltsb](#Ltsb)
-   [5 Hydrogen](#Hydrogen)
-   [6 LinuxSampler](#LinuxSampler)
-   [7 Midicomp](#Midicomp)
-   [8 Rosegarden](#Rosegarden)
-   [9 RTSynth](#RTSynth)
-   [10 TiMidity](#TiMidity)
-   [11 WildMidi](#WildMidi)
-   [12 XMMS](#XMMS)
-   [13 Other applications?](#Other_applications.3F)

Ardour
------

See [ardour](/Ardour "Ardour").

Jack
----

See [jack](/Jack "Jack").

Muse
----

See [muse](/Muse "Muse").

Ltsb
----

See
[ltsb](?title=Ltsb&action=edit&redlink=1 "Ltsb (page does not exist)").

Hydrogen
--------

Hydrogen is a pattern based drum sequencer
[http://hydrogen.sourceforge.net/](http://hydrogen.sourceforge.net/).

*How do you get Hydrogen to sync to ardour?*

In the hydrogen preferences, audio driver, select "jack", and check
"jack transport slave". Then click the play button and note that it
isn't playing, then in Ardour, record-enable some tracks, click record,
click play, and note that hydrogen starts playing instantly. Paul
Winkler (from linux-audio-users)

LinuxSampler
------------

LinuxSampler is a SoundFont (DLS2) and GigaSampler compatible softsynth
only available via CVS at this stage. See the LinuxSampler page for more
details.

Midicomp
--------

MidiComp is a SMF MIDI disassembler/compiler which will convert a MIDI
file into plain text and also convert that plain text version back into
a playable MIDI file. Not strictly an ALSA app but uses ALSA to hear the
results.

Rosegarden
----------

[Rosegarden](/Rosegarden "Rosegarden") is both a *musical notation
editor* and a *MIDI sequencer*. One of Rosegarden's major features is
that musical notation is created automatically when you play a MIDI
keyboard connected to your PC's soundcard.

RTSynth
-------

RTSynth a MIDI-event-triggered real-time synth
[http://www.linux-sound.org/rtsynth/](http://www.linux-sound.org/rtsynth/)

1.  start RTsynth.
2.  check the client/port ids via aconnect

` `

       % aconnect -o
       ...
       client 128: 'RTSynth v1.9.2 synthesizer' [type=user]
           0 'RTSynth         '

1.  load the patch from Examples directory.
2.  turn on the power button of rtsynth.
3.  play MIDI, e.g. via pmidi with the ids found above

` `

       % pmidi -p 128:0 foo.wav

- TakashiIwai

TiMidity
--------

TiMidity is a soft synth that uses Gravis GusPatches and SoundFonts
[http://www.onicos.com/staff/iz/timidity/](http://www.onicos.com/staff/iz/timidity/)

WildMidi
--------

WildMidi is a soft synth that uses the same configs and patches as
Timidity
[http://wildmidi.sourceforge.net/](http://wildmidi.sourceforge.net/)

XMMS
----

XMMS has an alsa plugin. Configuring XMMS with alsa for digital output
(spdif): In xmms, Options -\> Preferences (Ctrl P) select the tab
**Audio I/O Plugins**, and in the box **Output Plugin** select the
**ALSA 1.2.8 output plugin [libALSA.so]** and press the **Configure**
button. In the **ALSA Driver configuration**, Click the checkbox "[x]
User defined:", and enter **spdif** instead of **default**. Leave the
**Mixer card:** set to "0", and **Mixer device:** set to "PCM". This
will select the digital output for the soundcard, and now
[xmms](/Xmms "Xmms") will send the output to alsa's digital output. For
some unknown reason, "mono" tracks don't play. Only "stereo" tracks work
at the moment.

Other applications?
-------------------

More hints for other applications ?

Retrieved from
"[http://alsa.opensrc.org/AlsaApps](http://alsa.opensrc.org/AlsaApps)"

[Category](/Special:Categories "Special:Categories"):
[Software](/Category:Software "Category:Software")

