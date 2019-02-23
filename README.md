## Home Assistant component for Roon

Custom component for Home Assistant (www.home-assistant.io) to control Roon (www.roonlabs.com) zones as mediaplayers.


## Installation

While this is a work in progress, the component must be installed as a custom component on your hass setup.
I will soon be submitted to the hass source for inclusion as an official component.


1. Download/install the hass component

   * Download the contents of this Github repo into a local folder. 

   TIP: Click the green 'Clone or Download' button and select 'Download ZIP' and extract the files from there.

   * In your Home Assistant configuration directory (where all the yaml files reside), create a directory 'custom_components'

   * Inside the 'custom_components' folder, place the whole 'roon' folder you've downloaded.

   * The .py files reside in this directory.

   * Add the roon component in your hass configuration. In your configuration.yaml add an entry for Roon:

   ```
    roon:
    ```

3. Almost Done !

    * Now restart Home Assistant

    * In Home Assistant go to Settings --> Integrations

    * Configure the Roon integration by following the steps.


3. Done !



## What is supported ?

* All player command are supported, like controlling the volume, play/pause, next etc.
* Each player represents a "Roon output". A zone with multiple outputs will be displayed as multiple media players in hass.
* The source of each hass media player represents the Roon zone it's attached to.
* You can start playback of Playlists or Internet Radio, playback of other content is not supported.
* To start a playlist, set the name of the playlist as the "media_content_id" and set "media_content_type" to "playlist".
* To start a radio, set the name of the radio station as the "media_content_id" and set "media_content_type" to "radio".
* Use the usual Hass configuration to control your media players with Alexa or Homekit.
* The code should be fully async safe so it should not hog the hass event loop.
* New players will be auto detected, no need to restart hass.


Note: In a previous version of this component there was a "player widget", that code is now removed.
I'm planning on creating a Lovelace UI component instead.


## Feedback and TODO

This is considered to be a work in progress. I'm sure there will be some bugs in the code somewhere.
Let's test it, fix it and when stable enough submit it to Home Assistant for inclusion (with Roon's approval offcourse).

Please use the Roon forum to discuss the progress:

https://community.roonlabs.com/t/roon-module-for-home-assistant







