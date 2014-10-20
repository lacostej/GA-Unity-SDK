[Download and Setup](http://support.gameanalytics.com/entries/22584741-Download-and-setup)

NOTE: To use this GIT repository in your Unity game please add the contents directly to your Assets folder.

### Recent Changes:

##### v.0.6.6:
- Deprecated Heatmaps.
- Minor fixes.

##### v.0.6.5:

- Fix to Android advertising ID.
- Fixed a bug with custom user id.
- Fixed OS Version filter values for iOS / Android.
- Changed the default Critical FPS settings and fixed the event value sent.
- Fixed an issue with the PlayMaker and Facebook SDK integration.

##### v.0.6.4:

- Fixed unknown SDK version (displayed on web).
- Improved security.
- Fixed a bunch of minor bugs.

##### v.0.6.3:

- Added support for the Android Advertising ID. Please see the Android readme file under GameAnalytics > Plugins > Android.
- Updated Ad support for Chartboost to reflect their newest SDK version.
- Various bug fixes.

##### v.0.6.2:

- Greatly improved support for PlayMaker (see support.gameanalytics.com for more info).
- New sign up and login system in the SDK.
- Automatically sets your Game Key and Secret Key when you login.
- Added GA_Queue.RestartSubmit(), which can be called to start sending data again after GA_Queue.EndSubmit() was called.
- Added a Delay Quit option under GA_Settings > Advanced, which determines whether the SDK should pause Application.Quit actions to send remaining data (only PC/MAC).
- Removed Quality events (Error events should now be used instead of Quality).
- Added GA.API.GenericInfo.SetSessionUUID(string newSessionID), which dynamically sets a new session ID.
- Minor bug fixes.

##### v.0.6.1:

- Fixed an error when checking for updates while the update server is down.
- Fixed a build error caused by AdBannerView on non-iOS platforms.
- You will now be warned about missing Game key or API key when updating heatmaps.
- Some minor updates to the way new versions are handled.

##### v.0.6.0:

- New Ad Support feature for mobile games (see the Ad Support tab under GA_Settings). Supports iAd and Chartboost ad networks.
- Fixed some issues with building for Unity Metro (in the newest version of Unity).
- You can now call GA.SettingsGA.SetKeys(gamekey, secretkey) to change your keys dynamically.
- Minor bug fixes and improvements.

##### v.0.5.9:

- Added a new debug option, Debug Add Event, which will log a debug message every time an event is added. This option is disabled by default, but can be enabled from the Debug tab in GA_Settings.
- Fixed a missing link in the iOS_Readme file.

##### v.0.5.8:

- Apple has started rejecting some apps using IDFA (identifier for advertisers) which do not show ads. We have added a temporary fix to this problem. For more information please see the iOS_Readme.txt file in the GameAnalytics > Plugins > iOS folder.
- Greatly improved the Android setup process (GameAnalytics now works out-of-the-box with Android, requiring no additional setup).
- Minor bug fixes and improvements.

##### v.0.5.7:

- Added support for the Facebook SDK plugin (see GA documentation for setup information).
- Improved automatic tracking for Web Player builds.
- Android integration process greatly improved.
- Fixed a few minor issues.

##### v.0.5.6:

- The SDK will now indicate when a new version is available for download.
- Improved support for Heatmaps in the Unity editor with the new Unity 2D sprites.
- Setting up the Android ID plugin is now required when building for Android (see the readme in the Plugins/Android folder).
- Fixed an issue in the editor where the GA_SystemTracker would throw an exception after recompiling code in play mode.
- Minor changes to the way automatic user information is submitted.

##### v.0.5.4:

- Fixed a UI display error for the GA_Settings Advanced tab in Unity 4.3
- Added a new GA_Error.cs (message category); exceptions, errors, log info, etc., should use this class. Automatic error handling with the GA_SystemTracker will also use the new GA_Error class.

##### v.0.5.3:

- Added an option to toggle automatic tracking of user info (enabled by default). See the Advanced tab under GA_Settings.
- Minor tweaks and improvements.

##### v.0.5.2:

- Added new function to stops GA from sending data: GA_Queue.EndSubmit(). Can be used to allow users to opt out of tracking.
- Minor bug fixes.

##### v.0.5.1:

- Minor fixes and improvements.

##### v.0.5.0:

- Windows Phone 8 and Windows Store Apps support.
- Webplayer builds now automatically determine whether to use http or https, when sending data, based on webplayer url.
- Fixed an url encoding issue with heatmap mesh uploads.
- Fixed an issue with iOS identifiers on devices running an older OS version than iOS 6.
- Minor improvements to the implementation process for iOS and Android identifiers.

##### v.0.4.9:

- Ironed out some minor issues with the v.0.4.8 quick fix.

##### v.0.4.8:

- Fixed an issue with user IDs on iOS 7. Note: no data will be tracked on iOS if not set up correctly (please read the iOS_Reame in the GameAnalytics > Plugins > iOS folder for details).

##### v.0.4.7:

- Fixed an iOS bug with a value name in GA_Settings

##### v.0.4.6:

- Added an option under GA_Settings > Debug for sending data from the Example Tutorial Game to your own game.
- Made it possible for users to resize the GA Setup Wizard and GA Example Tutorial windows.
- Added additional options for identifying user on Android devices (see readme in GameAnalytics > Plugins > Android folder).
- Additional user and device information is automatically tracked at the beginning of each session.

##### v.0.4.5:

- Fixed a bug with creating new GA prefabs after changing folder structure.
- Fixed a reference exception with the GA logo texture.
- Fixed a JSON formatting error that would occur with exceptions containing ", \n, or \r symbols.

##### v.0.4.4:

- New menu options to upload / delete mesh AssetBundles for use with the new browser heatmap tool.
- New menu option to update folder structure for compatibility with UnityScript (JavaScript) and Boo (menu: GameAnalytics > Folder Structure > Switch to JS).
- New menu option to revert to original folder structure (menu: GameAnalytics > Folder Structure > Revert to original).
- Added build option to heatmaps.
- Added "Select for all builds" option to heatmaps.
- Fixed some minor issues with the heatmap histogram display for heatmaps with negative values.
- Fixed a minor encoding issue with message authorization.
- Changed Average FPS and Critical FPS events to Design events (instead of Quality events). This will allow you to view the average values in our online tool.
- Changed the class name of our MiniJson implementation to GA_MiniJson, to avoid conflicts with other plugins.
- Due to a bug with the Solid render model currently not supporting negative values, it has been removed as an option from heatmaps for now.

##### v.0.4.2:

- Average FPS (frames per second) events are now sent on every data submit interval (set under the Advanced tap of GA_Settings), instead of when the scene changes.
- Added an option for starting a new session on mobile games (iOS and Android), when the game is paused (minimized) and resumed.
- Minor improvements to the way exceptions are submitted.
- Minor changes to the file and folder structure of the GA Unity SDK package.
- Clarified some pop-up help text.
- Added support for iOS advertiser ID (see GameAnalytics > Plugins > iOS > iOS_Readme.txt).
- A few additional bug fixes and minor tweaks.

##### v.0.4.1:

- Fixed a bug with user ID generation in v.0.4.0

##### v.0.4.0:

- Added Flash Player support. As a result many code optimisations have been made, which should also improve performance even more on other platforms.
- Added GameAnalytics gizmos and logos to GA objects, for easier identification in the hierarchy and scene view.
- Fixed an issue with building to iOS with the Stripping Level "Use micro mscorlib". Please see the iOS considerations here: https://gameanalytics.zendesk.com/entries/23064016-Tips#player
- GA_HeatMap: Added a grid size for heatmaps under the advanced tab of GA_Settings. Data must be visualised with the same grid size as is used during collection.
- GA_HeatMap: Fixed an issue where the download button would not be re-enabled if the download failed.
- GA_HeatMap: Fixed an issue where heatmap histograms with too low sample count would look weird.
- GA_Tracker: Added custom interval to BreadCrumb event

##### v.0.3.7:

- Minor bug fixes.

##### v.0.3.5:

- New heatmap features, such as: add/subtract heatmaps, and color presets.
- Heatmap download indicator.
- Custom area.
- A ton of small fixes and improvements.

##### v.0.3.2:

- Fixed an issue with building projects on certain platforms.

##### v.0.3.1:

Complete revamp of the GA Unity Package, including:
- Huge performance boost.
- Completely new structure (no longer requires a GA prefab).
- 3D Heatmaps.
- Setup Wizard, Example game + Exampleg game tutorial.
- Status Window.
- System Tracker + Object Tracker.
- And lots more!

##### v.0.2.2:

- Fixed a performance issue with checking for network connectivity.

##### v.0.2.1:

- Restructuring of the inspector view.
- Added Drag'n'Drop event tracking for basic events.
- Improved QA functions, including error handling and tracking.
- Lots of minor tweaks, improvements and bug fixes.

# Game Analytics Unity3D Wrapper

The Game Analytics Unity3D wrapper is a plugin for Unity which makes it easy to send game event data to the Game Analytics service for visualization. By collecting data from players playing your game you will be able to identify bugs and balance issues, track purchases, and determine how your players really play your game!

##### Some key features:

- Helps you track user, game design, quality assurance, and business events in your game.
- Options for automatically tracking level transitions, errors and exceptions, and system specifications.
- Option for archiving data when the user is playing offline. Archived data will be sent next time the user plays with an internet connection.

The code for the Game Analytics Unity3D wrapper is open source - feel free to create your own fork, or use the code to develop your own wrapper.

### Game Analytics Full Documentation

You can find the [full documentation](http://beta.gameanalytics.com/docs) on the Game Analytics website for wrappers, and RESTful API, as well as information about how to collect useful data for your game.

### Game Analytics Website

The Game Analytics website can be found [here](http://beta.gameanalytics.com/). To use the Unity3D wrapper you will have to create an account on the website, and add your new game.
