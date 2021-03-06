Version 1.8.1

- Added iRateDidOpenAppStore delegate method
- Language selection now works correctly if the user has an unsupported language
- Removed all support for StoreKit, as Apple have disabled the StoreKit rating panel
- Calling openRatingsPageInAppStore will now look up appStoreID automatically if not already known
- Improved error messaging when using iRate on the iOS Simulator
- Added Greek and Slovenian localizations

Version 1.8

- App store link works on iOS 7 (had to link to app home page instead of directly to reviews page for now - hopefully an alternative direct link can be found)
- Now uses NSJSONSerializer if available (iOS 4.x will still use the old parser)
- No longer requires StoreKit by default (see README for details)
- Fixed Czech and Austrian German locales for iOS 7
- Removed disableAlertViewResizing property (no longer needed)
- Improved Czech translation
- Improved French translation
- Urdu support
- Fixed bug in alertview resizing for iOS 6 and below
- Now complies with the -Wextra warning level

Version 1.7.5

- Improved Arabic translation
- Improved podspec file
- Removed .DS_Store file

Version 1.7.4

- Added Arabic translation
- Improved French translation
- Added delegate method for tracking when prompt gets shown

Version 1.7.3

- Added Slovak, Czech and Austrian translations
- Fixed some bugs in Cancel/Remind button disabling logic
- Added podspec file

Version 1.7.2

- Added dutch translation
- iRate now displays the StoreKit product view controller correctly even if a modally presented view controller has been displayed

Version 1.7.1

- Fixed deprecation warning when targeting iOS6 as the base target
- Added iRateDidPresentStoreKitModal and iRateDidDismissStoreKitModal delegate methods
- Added additional error logging if StoreKit fails to load product info
- Added Ukranian translation

Version 1.7

- On iOS 6, iRate can now use the StoreKit APIs to display the product page directly within the app.
- iRate now requires the StoreKit framework on iOS
- iRate now requires ARC. To use iRate in a non-ARC project, follow the instructions in the README file.
- Dropped support for 32-bit Macs running Snow Leopard
- Added Swedish translation

Version 1.6.2

- Fixed broken ratings URL (Apple changed it)
- Added Danish translation

Version 1.6.1

- Fixed typo in Italian strings file

Version 1.6

- Added new localisation system (see README for details)
- Added usesPerWeekForPrompt setting
- Fixed deprecation warning in iOS 6
- Improved Spanish translation
- Improved German translation

Version 1.5.3

- Corrected minor spelling mistake in German translation

Version 1.5.2

- Restored App Store deep link on iOS6 (didn't work in beta, but now does)
- Added promptAgainForEachNewVersion option to enable/disable prompting each time the app is updated
- Added verboseLogging option to make it easier to diagnose why a new version isn't being correctly detected
- Renamed debug property to previewMode as this better describes its function
- Add Simplified Chinese localisation

Version 1.5.1

- Fixed crash on iOS 4.x and Mac OS 10.6.x when compiled using Xcode 4.4

Version 1.5

- Added support for iOS6. Currently it does not appear to be possible to take users directly to the ratings page on iOS6, but iRate will now at least open the app store on the app page without an error.
- Fixed bug in the app store country selection logic
- Changed appStoreGenre to appStoreGenreID, as this is not locale-specific

Version 1.4.9

- Added support for sandboxed Mac App Store apps with no network access
- Updated ARC Helper library

Version 1.4.8

- Added explicit 60-second timeout for connectivity check
- iRate will now no longer spawn multiple download threads if closed and re-opened whilst performing a check
- Added Portuguese translation

Version 1.4.7

- Fixed a bug where advanced properties set in the delegate methods might be subsequently overridden by iRate
- Added Events Demo example

Version 1.4.6

- Fixed odd glitch where shaking device would cause UIAlertview to slowly shrink
- Added disableAlertViewResizing option (see README for details)
- Added Resizing Disabled example project
- Added Korean translation

Version 1.4.5

- Improved German, Spanish, Japanese, Russian and Polish translations
- Added onlyPromptIfMainWindowIsAvailable option

Version 1.4.4

- Added Turkish localisation
- Improved German translation
- Fixed alert layout for long app names

Version 1.4.3

- It is now possible again to use debug to test the iRate message for apps that are not yet on the App Store. 

Version 1.4.2

- Added Hebrew localisation
- Fixed issue with UIAlertView label resizing
- Fixed some compiler warnings

Version 1.4.1

- Added logic to prevent UIAlertView collapsing in landscape mode
- Added Russian, Polish and Traditional Chinese localisations
- Improved Japanese localisation
- Now handles nil cancel button text correctly

Version 1.4

- Included localisation for French, German, Italian, Spanish and Japanese
- iRate is now *completely zero-config* in most cases!
- It is no longer necessary to set the app store ID in most cases
- iRate default text now uses "playing" instead of "using" for games
- iRate delegate now defaults to App Delegate unless otherwise specified
- By default, iRate no longer prompts the user to rate the app unless they are running the latest version

Version 1.3.5

- Fixed bug introduced in 1.3.4 where remind button would not appear on iOS

Version 1.3.4

- Fixed compiler warning
- Added `iRateDidDetectAppUpdate` delegate method
- Added ARC Test example

Version 1.3.3

- Added missing ivar required for 32-bit Mac OS builds.

Version 1.3.2

- Added logic to prevent multiple prompts from being displayed if user fails to close one prompt before the next is due to be opened.
- Added workaround for change in UIApplicationWillEnterForegroundNotification implementation in iOS5

Version 1.3.1

- Added automatic support for ARC compile targets
- Now requires Apple LLVM 3.0 compiler target

Version 1.3

- Added additional delegate methods to facilitate logging
- Renamed disabled property to promptAtLaunch for clarity

Version 1.2.3

- iRate now uses CFBundleDisplayName for the application name (if available) 
- Reorganised examples

Version 1.2.2

- Fixed misspelled delegate method
- Fixed bug in advanced Mac project where rating prompt was displayed automatically even if button was not pressed
- Removed unneeded project files

Version 1.2.1

- Exposed the shouldPromptForRating method to make it easier to control when rating prompt is displayed
- Increased `MAC_APP_STORE_REFRESH_DELAY` to 5 seconds to support older machines

Version 1.2

- Added delegate and additional accessor properties for custom behaviour
- Added advanced example project to demonstrate use of the delegate protocol

Version 1.1

- Now compatible with iOS 3.x
- Fixed incorrect iPhone review URL

Version 1.0

- Initial release.