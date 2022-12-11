
# Changelog

### 4.0.10 (11/DEC/2022)
* Supports Typescript. 

### 4.0.8 (24/MAY/2022)
* Enhances the Conviva inference logic for browser if its running in background.
There is a browser limitation such that setTimeOut interval is increased to 1sec from 250ms if its running in backgroung, causing the playhead position to update late.
Hence the check to detect false PLAYING state if play head position with in ~ 1 sec if application is forground, and within ~ 4 secs if application is background is added.
 

### 4.0.7 (13/MAY/2021)
* Enhances the Conviva inference logic in low bandwidth and seek scenarios to detect the PLAYING state from the play head position with in ~ 1 sec, as the playing event is not reliable.
* Fixes the player state issues of:
  * False PLAYING and BUFFERING states on timeupdate event for those instances where the currentTime returns 0 on playing event, as Conviva inference logic relies on timeupdate event counter when the currentTime is 0.
  * False PLAYING state in Windows Internet Explorer and Edge during seeking as the pause event is not triggered.
  * UNKNOWN player state at end of midroll.
* Fixes the issue of duration auto collected with Number.MAX_VALUE(1.7976931348623157e+308) for the DASH Live content.

## 4.0.5 (30/DEC/2020)
* Introduces new versioning of Major.Minor.Patch<b>L</b>(Eg.. 4.0.5<b>L</b>) for the legacy Conviva JavaScript HTML5 Integrations to be able to differentiate from the Simplified Integrations.

## 4.0.4 (07/MAY/2020)
* Uses 2.151.0.xxxxx series versioning for older integrations that use Core SDK version 4.x+.

## 4.0.3 (14/FEB/2020)
* Introduces a major upgrade to the SDK architecture that simplifies and accelerates Conviva integration.
* Introduces Analytics, VideoAnalytics, and AdAnalytics to simplify the integration of the SDK.

## 2.151.0.36976 (05/FEB/2019)
* Introduces new MetadataInterface API getDeviceCategory for setting the device category, to support the changes in Core JS SDK.

## 2.141.0.35966 (04/JUN/2018)
* Fixes an issue in some Safari browsers, with auto-play disabled, where Video Start-up Time was under-reported.
* Fixes an issue while buffering during seek that caused false playing state to be reported instead of buffering. rebuffering ration and video restart time

## 2.139.0.35500 (20/APR/2018)
* Supports the HTML5 library as a module on top of the Conviva Javascript SDK. The HTML5 module inherits all JS SDK functionality.

## 2.137.0.35314 (09/FEB/2018)
* Introduces new PlayerStateManager APIs: updateContentMetadata, setLinkEncryption, setConnectionType, setVideoResolutionWidth and setVideoResolutionHeight.
* Introduces new logic where values set by user with Client API updateContentMetadata() for duration, take higher precedence over the Conviva library auto detected values.
* Introduces new Client APIs: getAttachedPlayer and isPlayerAttached.
* Changes the HTML5PlayerInterface name space, from Conviva to Conviva.Impl and changes the integration step from using Html5SystemInterfaceFactory to using SystemInterface.
* Fixes existence of verbose logging even when it is turned off, by adding new argument of SystemFactory to HTML5PlayerInterface.
* Fixes issue where Rebuffering Ratio was over-reported for Live content.
* Fixes issue where buffering events were ignored during seek.
* Fixes the issue of under-reporting Rebuffering Ratio and Connection Induced Rebuffering Ratio during low bandwidth conditions.
* Changes the Conviva Core library file name from conviva-html5native-library.min.js to conviva-core-sdk.min.js

## 2.117.0.31658 (21/DEC/2016)
* Supports automatic detection of Seek Induced buffering.

## 2.115.0.31160 (20/OCT/2016)
* Supports a sample application with HTML5 Native reference implementation.
* Contains an HTML5 Library validated with HLS, DASH, Smooth Streaming, and Progressive Download content types.
* Replaces a previous HTML5 library which was accessible by URL.
* Fixed issue of dropping Conviva heart-beat by Conviva Backend platform.
