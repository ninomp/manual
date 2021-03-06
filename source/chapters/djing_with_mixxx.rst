.. include:: /shortcuts.rstext

DJing With Mixxx
****************

Mixxx was designed to be easy to learn for both novice and experienced DJs.

This part of the manual provides you with directions for importing and managing
you music collection and playing your tracks.

.. _djing-open:

Opening Mixxx
=============
|logo| Once you've :ref:`installed Mixxx <installing-mixxx>`, start by opening
Mixxx and import your music to the Mixxx library.

**Windows**
  Double-click the Mixxx icon on the Desktop. Alternatively, browse your Windows
  start menu and click the Mixxx icon, or perform a search for :file:`Mixxx.exe`.

**Mac OSX**
  Double-click the Mixxx icon in the :file:`Applications` folder. Alternatively,
  drag the Mixxx icon to the dock and double-click it there, or perform a search
  for :file:`Mixxx.app`.

**GNU/Linux**
  Simply type :command:`mixxx` into the terminal, then hit :kbd:`Return`. With
  some distributions like Ubuntu you can also double-click the Mixxx icon in the
  launcher. Alternatively, perform a search for :file:`mixxx`.

.. _djing-import:

Importing your audio files
==========================

.. sectionauthor::
   S.Brandt <s.brandt@mixxx.org>

.. figure:: ../_static/Mixxx-111-1st-run-choose-library-directory-win.png
   :align: center
   :width: 50%
   :figwidth: 100%
   :alt: Mixxx 1st run - Choose music library directory dialog
   :figclass: pretty-figures

   Mixxx running on Windows 8 - Choose music library directory dialog


**Setup the music library**
  The first time you run Mixxx, you are asked to select a directory where your
  music is stored. By default, the dialog points to a location where music files
  are typically held.

  Click :guilabel:`Select Folder` and Mixxx will scan your music library.
  Depending on the size of your library this could take some time. All of the
  supported music files Mixxx detects will be listed in the :ref:`library-root`.

  Mixxx automatically detects newly added tracks on each subsequent run. If you
  want to manually refresh your library without exiting (for example because you
  added or moved files), you can do this with :menuselection:`Library --> Rescan
  Library` in the menu. If you want to rescan at every launch, select
  :menuselection:`Preferences --> Library --> Rescan on startup`.

  .. warning :: On Windows 7 and 8 the import dialog points to your Windows
                “Music“ Library, a special-purpose virtual folder. You can
                **not** use these virtual folders. Select a regular folder
                instead, usually “My Music“, like pictured above.

**Compatible files**
  Mixxx supports a variety of file formats: :term:`Wave <WAV>` (wav),
  :term:`Aiff <AIFF>` (aiff, aif), :term:`MP3` (mp3), :term:`Ogg vorbis` (ogg),
  :term:`FLAC` (flac), and :term:`AAC` (aac, m4a) if supported by your :term:`OS
  <Operating System>`. :term:`DRM` protected files, such as m4p
  files purchased in the iTunes Store, are not supported.

  AAC (M4A) is supported on Windows Vista and Mac OSX 10.5 onwards. The 
  `Platform Update Supplement <http://support.microsoft.com/kb/2117917>`_ is
  required for Windows Vista.

  On Linux, AAC playback is disabled by default due to licensing restrictions.
  To enable the playback of AAC files, `build Mixxx from source with m4a files support
  <http://www.mixxx.org/wiki/doku.php/compiling_on_linux#build_with_m4a_file_support>`_.

**Changing the music directory**
  The Mixxx music directory can always be changed at a later time in
  :menuselection:`Preferences --> Library`. You might want to run a library
  rescan afterwards, select :menuselection:`Library --> Rescan Library` in the
  menu.

**Import external libraries**
  If you have iTunes, Traktor, Rhythmbox, or Banshee installed, Mixxx allows you
  to access your tracks and playlists in the Mixxx library,
  see :ref:`library-3rd-party`.

**Import remote files**
  To import audio files which are not in your music library directory, drag them
  directly from an external :term:`file manager` or from the :ref:`Browse section
  <library-browse>` to the track list. Importing files into Mixxx does not
  change the location of the files on the hard disk.

  .. note :: You can not drag complete folders to the library because currently
             Mixxx can not recursively scan folders for compatible music files.

**Import playlists**
  You can import existing :file:`m3u`, :file:`pls` , :file:`m3u8`, :file:`pls` 
  playlist files from products other than Mixxx, see :ref:`library-playlists`.

**Import music from CDs**
  Mixxx can not play music from Audio CDs. Convert the content to compatible
  files in good quality and add them to the Mixxx library. See
  `<https://en.wikipedia.org/wiki/Ripping>`_

.. _djing-loading-tracks:

Loading Tracks
==============

Tracks can be loaded into a deck in several ways:

* Right-click the :ref:`library track table <interface-library>`: Right-clicking
  on a track in the table will present the options :guilabel:`Load in Deck 1`
  and :guilabel:`Load in Deck 2`, among others. Making either selection will
  load a track into a deck.
* By :ref:`control-keyboard` to load the selected track from library track table.
* Drag-and-drop from library track table: Dragging-and-dropping a track from the
  track table onto a waveform display will load a track into a deck.
* Drag-and-drop from external file browser: Dragging-and-dropping a track from
  an external file browser directly onto a waveform display in Mixxx will load
  that track. This function also works with some other applications. For
  example, on Mac OS X, dragging-and-dropping a track from iTunes onto one of
  Mixxx's waveform displays will load that track into a deck.

.. _djing-finding-tracks:

Finding Tracks (Search)
=======================

.. sectionauthor::
   RJ Ryan <rryan@mixxx.org>
   S.Brandt <s.brandt@mixxx.org>

The :ref:`search function <library-search>` searches for a match only in the
current selected list (e.g. a playlist, a crate or even the whole library).

* Activate the search input field by pressing :kbd:`CTRL` + :kbd:`F`
  (Windows/Linux) or :kbd:`CMD` + :kbd:`F` (Mac). Alternatively click into the
  :ref:`search box <library-search>`.
* Type your search term. Mixxx filters the tracks and retains only the ones that
  match the search term. Search terms can include an artist's name, a song
  title, BPM, etc.
* To clear the search string hit :kbd:`ESC` or click the clear button right next
  to the input field.
* Hit :kbd:`TAB` to cycle between the search and the list of results in the
  library. Use the :kbd:`ARROW UP` and :kbd:`ARROW DOWN` keys to scroll in the
  list of results.

.. note:: If the search input field has focus, the Mixxx keyboard shortcuts are
          disabled, see :ref:`control-keyboard`.

Using search operators
----------------------

Search operators allow you to form more complex search queries. They allow you
to limit certain search terms to particular properties of your tracks.

.. versionchanged:: 1.12
   Adds *location* and *album_artist* search keywords

Mixxx supports the following filters:

* **Text filtering**: artist, album, album_artist, genre, title, composer,
  comment, key, location

* **Numeric filtering**: year, track, bpm, duration, played, rating, bitrate

You can combine operators but there's no way to do an “OR” search right now.
The following example list all tracks by “Danger” over 300 seconds (5 minutes)
long that are rated 4 or 5.

::

    artist:Danger duration:>300 rating:>=4

+--------------------------------------+---------------------------------------+
| Examples for text filtering          | Examples for numeric filtering        |
+======================================+=======================================+
| artist: “com truise”                 | bpm:140                               |
+--------------------------------------+---------------------------------------+
| album:Danger                         | bpm: >140                             |
+--------------------------------------+---------------------------------------+
| genre: Trance                        | year: <2010                           |
+--------------------------------------+---------------------------------------+
| title: foo                           | bpm: >=140                            |
+--------------------------------------+---------------------------------------+
| composer: foo                        | rating: <=4                           |
+--------------------------------------+---------------------------------------+
| comment: foo                         | bpm: 140-150                          |
+--------------------------------------+---------------------------------------+
|                                      | played: >10                           |
+--------------------------------------+---------------------------------------+
| Note it doesn't matter if you have   | Note that you can put a space between |
| space between the colon and the      | the colon but currently there must be |
| argument or not. Quotes must be used | no space between the operator and the |
| for multi-word text arguments.       | number.                               |
+--------------------------------------+---------------------------------------+

.. _djing-previewing-tracks:

Previewing Tracks
=================

.. sectionauthor::
   M.Linke <kain88@mixxx.org>
   S.Brandt <s.brandt@mixxx.org>

To pre-listen to a track, activate the :guilabel:`Preview` column in a library
view. Clicking the |ic_lib_preview_play| icon in the library's
:guilabel:`Preview` column loads the selected track in a special :ref:`Preview
Deck <interface-preview-deck>` that will only output sound in the
:ref:`headphones <interface-head-master>` channel. Click the
|ic_lib_preview_pause| icon to stop the playback.

Alternatively, select a track from the track list of the Mixxx library, drag the
track to the waveform view of the :ref:`Preview Deck <interface-preview-deck>`
and click the :guilabel:`Play` button next to the waveform.

To display the Preview deck, press :kbd:`CTRL` + :kbd:`4` (Windows/Linux) or
:kbd:`CMD` + :kbd:`4` (Mac).

.. _waveform-displays:

Waveform displays
=================

There are two main waveform displays in Mixxx that are used to display the
waveform of the tracks you are mixing. These are useful because they allow you
to see features in a track (like a breakdown) before you hear them.

Depending on the skin Mixxx displays either separate waveforms (default) or
parallel waveforms. Select your preferred appearance in
:menuselection:`Preferences --> Interface --> Skin`.

.. figure:: ../_static/Mixxx-111-Deere-separate-waveform.png
   :align: center
   :width: 100%
   :figwidth: 100%
   :alt: Mixxx default skin (Deere) - Separate waveforms
   :figclass: pretty-figures

   Mixxx default skin (Deere) - Separate waveforms

With some skins the waveform displays are aligned parallel to each other in
order to make :term:`beatmatching` easier, as it is possible to beatmatch
visually by aligning the beats that appear in each waveform.

.. figure:: ../_static/Mixxx-111-Latenight-parallel-waveform.png
   :align: center
   :width: 100%
   :figwidth: 100%
   :alt: Mixxx alternative skin (Latenight) - Parallel waveforms
   :figclass: pretty-figures

   Mixxx alternative skin (Latenight) - Parallel waveforms

The mouse can be used on the waveforms to scratch, spin-back or throw the
tracks.  Right-clicking and dragging on the waveforms allows you to nudge the
track and make temporary pitch adjustments. Using the mouse-wheel on the
waveform zooms the waveform in or out. You can choose whether or not to
synchronize the zoom level between the decks in :menuselection:`Preferences -->
Interface --> Waveform Display --> Synchronize`. The waveform display is updated
in real time upon seeking.

There are two smaller waveform summary displays located adjacent to the main
waveform displays. Clicking on a waveform summary allows you to seek through the
track. These smaller displays show the waveform envelope of the entire track,
and are useful because they allow DJs to see breakdowns far in advance. Vinyl
DJs will find this familiar because quiet sections of tracks can be visually
distinguished when looking at a vinyl record. This is a useful tool when
planning your mixes on-the-fly.

.. _beatmatching-and-mixing:

Beatmatching and Mixing
=======================

:term:`Beatmatching` is the process of adjusting the playback rate of a track so
that it matches the tempo of another track. Beatmatching also involves adjusting
the :term:`phase` of the beats in a track so that they are aligned with the
beats in the other track. Matching the :term:`tempo` and aligning the beats are
the two things a DJ must do to beatmatch.

Mixxx can match the tempo and align the beats for you but this requires an
accurately detected BPM value and a correct beat grid for both tracks. To enable
this feature, hit the :guilabel:`SYNC` button. To beatmatch manually, the tempo
of the two tracks must be synchronized by adjusting the playback rate
sliders. You can adjust the phase of the beats by right-clicking and dragging on
either waveform display to temporarily speed up or slow down one of the tracks
until the beats are aligned. The temporary pitch bend buttons can also be used
to momentarily adjust the playback rate, allowing you to “shuffle” the beats in
a track forwards or backwards, so they can be aligned with another track. See
the chapter :ref:`interface-rate`.

Two tracks are beatmatched once their tempos are matched and their beats beats
are aligned. A “perfect” beatmatch is nearly impossible - there will always be a
tiny difference in the playback rates. A keen DJ will keep his or her ears open
and listen for the beats drifting out of alignment. This has a distinct “double
bass kick” sound which is often preceded by the kick weakening in intensity as
the two kicks drift out of phase. When this happens, the beats can be realigned
by simply tapping one of the temporary pitch bend buttons a few times in the
appropriate direction.

.. _headphone-cueing:

Headphone Cueing
================

Headphone cueing is a technique DJs use to listen to the next track they want to
play in their headphones before playing it on the main speakers. Headphone
cueing is useful because it allows a DJ to beatmatch the next track in their
headphones before bringing it into their mix by sliding the crossfader.

Mixxx allows a DJ to route audio from either deck to their headphones by
toggling either of the :guilabel:`Headphone` buttons in the mixer section of
Mixxx's interface. See the chapter :ref:`interface-mixer`.

.. _djing-bpm-detection:

BPM and Beat Detection
======================

.. sectionauthor::
   T.Rafreider <trafreider@mixxx.org>
   S.Brandt <s.brandt@mixxx.org>

Previous versions of Mixxx were able to detect BPM values but unable to
determine where the beats are. Consequently, the beat grids often looked
unaligned. The DJ had to adjust the beat grid manually in oder to make use of
auto-beatmatching via :guilabel:`SYNC` button.

Now Mixxx comes with a new ultra-precise BPM and beat detector.
The beat grid is adjusted after track analysis is finished. Manual adjustments
are redundant in many cases because Mixxx knows where the beats are.

Analyzer Settings
-----------------

BPM and beat detection is a complex operation. Depending on your computer and
the track's bitrate and duration this may take some time. By default Mixxx
analyzes the complete track. To accelerate beat detection on slower computers, a
“Fast Analysis” option is available. If enabled, the BPM is computed by
analyzing the first minute of the track. In most cases this does not affect the
beat detection negatively because most of today's dance music is written in a
4/4 signature with a fixed tempo.

.. figure:: ../_static/Mixxx-111-Preferences-Beatdetection.png
   :align: center
   :width: 75%
   :figwidth: 100%
   :alt: Mixxx preferences - BPM settings
   :figclass: pretty-figures

   Mixxx preferences - BPM settings

The table below summarizes the beat detection settings:

+---------------------------------------+--------------------------------------+
| Option                                | Description                          |
+=======================================+======================================+
| Enable Fast Analysis                  | If enabled, BPM detection results    |
|                                       | from the first minute of audio.      |
+---------------------------------------+--------------------------------------+
| Assume constant tempo                 | If enabled, Mixxx assumes that the   |
|                                       | distances between the beats are      |
|                                       | constant. If disabled, the raw beat  |
|                                       | grid obtained by the analyzer is     |
|                                       | presented. The latter is appropriate |
|                                       | for tracks with variable tempo.      |
+---------------------------------------+--------------------------------------+
| Enable Offset Correction              | Prevents beat markers from being     |
|                                       | placed incorrectly.                  |
+---------------------------------------+--------------------------------------+
| Re-analyze beats when settings        | If enabled, Mixxx over-writes old    |
| change or beat detection data is      | beat grids from Mixxx before v1.11.  |
| outdated                              | Moreover, it will re-analyze the BPM |
|                                       | if your beat detection preferences   |
|                                       | change or BPM data from 3rd party    |
|                                       | programs are present.                |
+---------------------------------------+--------------------------------------+

Correcting Beat Grids
---------------------

There may be situations where BPM and beat detection do not result in a proper
beat grid.

Typically, the detected BPM is correct but the analyzer has failed to detect the
location of the first beat. Consequently, the beat markers are shifted, i.e.
the beat markers are always a fixed distance from the true beat. To adjust the
beat grid, cue the track before a real beat and click the :guilabel:`Beat-grid
Adjust` button in the :ref:`interface-button-grid`.

If the detected BPM is not accurate, the corresponding beat grid will also be
inaccurate. A deviation of 0.02 BPM units from the correct BPM will cause
beatgrid alignment issues on long tracks (e.g. a club mix). If this happens,
your beatgrid may look aligned for the few minutes but you will notice a slight
drift as the song goes on. Finding the correct BPM is easy in many cases - just
follow the note below.

.. note:: If the detected BPM value is not sufficiently accurate but very close
          to an integer value, try to set the BPM value manually to the integer.

.. _djing-recording-your-mix:

Recording your Mix
==================

.. sectionauthor::
   S.Brandt <s.brandt@mixxx.org>

With the integrated recording feature you can record your mix as an audio file
and listen to it later, distribute it as :term:`Podcast` or burn it to CD.
Mixxx records the master output - the audio you hear from the speakers including
the microphone.

.. figure:: ../_static/Mixxx-111-Library-Recordings.png
   :align: center
   :width: 100%
   :figwidth: 100%
   :alt: Mixxx library - Recordings view
   :figclass: pretty-figures

   Mixxx library - Recordings view

Mixxx can record your mix in various audio formats and quality settings. You can
split your recordings, generate :term:`cue files <cue sheet>`, choose a custom
recording directory and even set your own :term:`metadata`. By default, Mixxx
saves your recordings as lossless :term:`wav` files to a
:file:`Mixxx/Recordings` sub-folder in the Mixxx music directory. Before you
start recording, we recommend that you adjust the settings in
:menuselection:`Preferences --> Recording`.

If you click on the *Recordings* icon in the sidebar of the Mixxx library, the
track table to the right displays the content of your recordings directory. New
recordings are automatically saved to this directory as well as CUE files if you
choose to create them in the preferences.

Record your mix to disk
-----------------------

* Click on the *Recordings* icon in the sidebar to switch to the
  :guilabel:`Recordings` view
* Click the :guilabel:`Start Recording` button or click
  :menuselection:`Options --> Record Mix` in the menu on top of the Mixxx
  application window.
* The display above the track table shows how much data has already been
  recorded.
* Perform your mix
* Click the :guilabel:`Stop Recording` button to stop the recording when the mix
  has finished.

.. hint:: You can instantly play your recording as track in Mixxx. Simply
          drag-and-drop the track to a deck.

Burn your recorded mix to a CD/DVD
----------------------------------

* Select your recording in the :guilabel:`Recordings` view
* Right-click and select :guilabel:`Open in File Browser` to locate the file on
  your disk
* Now burn the recording to a CD/DVD using a 3rd-party program, for example
  `CDBurnerXP <http://www.cdburnerxp.se/>`_ for Windows or
  `Burn <http://burn-osx.sourceforge.net/>`_ for Mac OS X.

.. note:: Due to licensing restrictions, :term:`MP3` recording is not enabled
          per default. In order to enable MP3 streaming you must install the
          :term:`LAME` MP3 :term:`codec` yourself. Go to the chapter
          :ref:`MP3 Streaming` for more information.

.. _djing-auto-dj:

Using Auto DJ for automatic mixing
==================================

.. sectionauthor::
   S.Brandt <s.brandt@mixxx.org>

.. figure:: ../_static/Mixxx-111-Library-Auto-DJ.png
   :align: center
   :width: 100%
   :figwidth: 100%
   :alt: Mixxx library - Auto DJ view
   :figclass: pretty-figures

   Mixxx library - Auto DJ view

Auto DJ allows you to automatically load tracks from the Auto DJ playlist when
the current track is nearly finished, and crossfade into it.  See
:ref:`library-auto-dj`.

Loading tracks into Auto DJ
---------------------------

To play tracks automatically, they must first be loaded into the Auto DJ
playlist. The Auto DJ playlist is empty by default.

.. figure:: ../_static/Mixxx-111-Library-Add-to-Auto-DJ.png
   :align: center
   :width: 50%
   :figwidth: 100%
   :alt: Mixxx library - Adding a playlist to Auto DJ
   :figclass: pretty-figures

   Mixxx library - Adding a playlist to Auto DJ

There are several ways to load tracks into the Auto DJ playlist:

* Select single or multiple tracks from the library, a regular playlist or crate
  and drag them to the Auto DJ icon on the left.
* Select a regular playlist or crate, right-click with the mouse and select
  :guilabel:`Add to Auto DJ` from the mouse menu. This adds all tracks to Auto DJ.
* While in the Auto DJ view of the library, drag tracks from external file
  managers to the Auto DJ icon in the sidebar or to the Auto DJ track table on
  the right.

Playing tracks in Auto DJ
-------------------------

Now that you have loaded tracks into the Auto DJ playlist, you can activate Auto
DJ as follows:

* Click on the *Auto DJ* icon in the sidebar to switch to the :guilabel:`Auto
  DJ` view of the library.
* Click the :guilabel:`Enable Auto DJ` button.
* The first tracks from your list are loaded into the decks and the playback
  starts.
* Mixxx will continue to automatically mix until the Auto DJ playlist is empty.
* Click the :guilabel:`Disable Auto DJ` button to stop the automatic mixing

