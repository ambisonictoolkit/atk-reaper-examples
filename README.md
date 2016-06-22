# atk-reaper-examples

This is a collection of example projects for the [REAPER DAW](http://reaper.fm) illustrating how to use the [atk-reaper plugins](http://www.ambisonictoolkit.net/documentation/reaper/) to [work with Ambisonics surround sound](http://www.ambisonictoolkit.net/documentation/workflow/).

## List of examples

### Decoding examples

#### Decode UHJ Stereo

Decodes an Ambisonics B-format file to UHJ stereo.

* The "B-format" track is set up to have 4 channels, all of which are sent to the master/parent track.
* The Master track is set up to have 4 channels as well. This is necsessary in order to receive all four channels of the Ambisonics B-format signal. The UHJ decoder plugin decodes to UHJ stereo, and the resulting audio is output to outlets 1 and 2.

The window size of the UHJ plugin is set to the maximum value (8192) for best quality.

**Important:**

The UHJ processing introduces some latency. This is compensated for in the plugin, but as a consequence, when rendering this project, some audio will be lost at the very beginning. For this reason the media file is set to start at bar 2 rather than on the very first bar of the project.
