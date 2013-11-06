# Manual QA testing for iOS apps 

## Functional testing
* What functions is the app supposed to have? Please list all, inclusing possible outcomes
* Does the app indeed support these functions? Please check off all functional requirements listed

## Hardware
Which of the following hardware models does the app support?

1. iPhone 3g, iPhone 3gs, iPhone 4 (Retina), iPhone 4s, iPhone 5 (4-inch)
2. iPad, iPad 2, iPad 3 (alias new, Retina), iPad 4, iPad Mini (not Retina, smaller 7.9’’ screen)
3. iPod Touch 4, iPod Touch 5 (4-inch Retina)

You might consider iPhone 3G, 3GS and iPad obsolete.

## Operating system
Which of the following hardware models does the app support?

1. iOS 5.x
2. iOS 6.x
3. iOS 7.x

You might deem iOS 5.x obsolete, supporting the curent plus previous main release will in general give you 95%+ coverage.

## Device orientation and rotation
1. Does the app support both landscape and portrait orientation?
2. Any particular views (UIViewControllers) that support different orientations?

## Network
How does the app behave under these network circumstances:

1. No network at all/Airplane mode
2. Intermittent network
3. Cellular slow: 2G (Edge)
4. Cellular medium: 3G (UTMS, CDMA) 
5. Cellular fast: 4G(LTE)
6. Wifi
7. Public wifi with HTTP authentication (e.g. Starbucks)

Testing with a proxy like [Charles](http://www.charlesproxy.com/) that allows for throttling helps simulating.

Other network questions:

1. Is your app tested on all carriers in your target market?
2. Is offline access to (part of) data required?
3. Does the app make sense for wifi-only devices?
4. Does the app resume sending/downloading data after a connection has been reestablished?

## Security
1. Is confidential data sent over unsecured HTTP?
2. Are user credentials like username/password sent over unsecured HTTP?
3. Are sensitive files stored unencrypted on the device?
4. Would a pin code on the app (e.g. like DropBox) be advisable?
5. What happens if a device is stolen? Should the app be remotely wiped?


## Memory
How does the app behave under low memory circumstances:

1. Open up lots of Mobile Safari windows and go back to the app
2. Use an old model device like the original iPad (maybe even not supported model anymore)

Trigger memory warnings in the Simulator.

## Local data and caching
1. Is local data stored? Is it backed up to iCloud or not?
2. What happens when the OS deciced to whipe out temp files, e.g. when not enough disk space is available?

## Battery
1. Does the app drain the battery extensive?
2. Does the app use background processes like fine grained location services that require a lot of resources?

## Text input
1. Can a very large text be entered?
2. What happens on suspend and resume? Can I continue entering text where I left off?

## Input
1. How do gestures work?
2. Is tilting one of the input ways? How does it work? Does it interfere with other input methods?

## Location
1. Does the app use location? What level is required?
2. What happens if the location is off, e.g. when a user is indoors with no GPS and unknown wifi?

## Accessability
1. Are controls accessible? 
2. Are accessibility labels set on all controls?

## Crash logs
Use one of the following services to collect and analyse crash logs:

1. [Crashlytics](http://www.crashlytics.com)
2. [Crittercism](http://www.crittercism.com/)
3. [iTunes Connect](https://developer.apple.com/library/ios/#technotes/tn2008/tn2151.html)

## Installation
1. What is the size of the initial download, is it too big for cellular downloads (> 50mb)?

## Updates
1. What is the size of the updated app, is it too big for cellular downloads (> 50mb)?
2. Are there database updates? Have they been tested with multiple previous releases?
3. Is CoreData used for database migrations?
4. Are there other persistent data/settings that should be tested with updates?
5. Did you update the version number in a consistent way?
6. Are updates forces to keep up with an updated server environment?

## Guidelines
1. Are the [Apple App Review Guidelines](https://developer.apple.com/appstore/guidelines.html) followed?
2. Are the [iOS HIG (Human Interface Guidelines)](http://developer.apple.com/library/ios/#documentation/UserExperience/Conceptual/MobileHIG/Introduction/Introduction.html) followed?
3. Are all trademarks and copyrights covered?

## In-app purchases
1. Can a user download past purchases (e.g. after a reinstall)?
2. Are purchased items available on all of the user's devices?
3. What happens if halfway through the processing process your backend servers are not available?
4. Are children a target market? Do you present in-app purchases in a child-friendly way?
5. What happens if someone uses a different Apple account (Apple ID) than the one with which the original app was downloaded?
6. What happens if a user turned off in-app purchases for the whole device?
7. Can the process be hacked?
8. What happens if Apples sends you inconsistent info, is the data validated?

## Push notifications
1. Can a user turn off push notifications?
2. What happens when a user uninstalls the app? 
3. Is your link between all their different devices and a user consistent?
4. Does push work both in development environment as production environment?
5. Do the messages appear in the notification center?
6. Is the correct sound played?
7. How consistent is the user experience if after a time of no connectivity only the last push notification arrives at the phone?
8. How consistent is the user experience with delays on notifications (wifi only means a check every 15 minutes)
9. How do you deal with push notifications when users are behind a firewall that blocks port 5223, on which the push notification process runs?
10. What does the user see in Do-not-disturb mode?

## Consistent data
1. Do various ways of displaying information do this consistently? As in unread icon, and then the list of unread messages?
2. Is your app's badge updated consistently?
3. What happens on a crash while information is processed, is there a repair process or a consistency check?
4. What happens if the server returns inconsisstent data?
5. What happens if a user sets the time of their device incorrect?

## Interrupts
1. How does the app deal with interrupts like incoming calls, push notifications?
2. After returning to the app, is it in a consistent state?

## Animations & concurrency
1. Are all animations smooth?
2. Can multiple animations be triggered at the same time?
3. What happens if an animation is started and the user rotates the app? 
4. Are buttons disabled after an initial touch and before results returned?
5. Does the app show activity indicators while a process is running, e.g. a network call lasting several seconds?
5. What happens if a user initiates a process, and then quickly navigates away before the process is finished?

## Localisation and time
1. Are multiple time formats (12-24h) supported?
2. What happens in other timezones?
3. What languages are supported?
4. Do all text snippets and labels fit in all languages
5. Is the translation correct?
6. Are graphics with text also translated?

## Custom Url schemes
1. What url schemes are supported?
2. Any conflict with an existing scheme? Check [handleOpenURL](http://handleopenurl.com/)

#Copyright and license
Copyright 2013 Mobtest, Inc.

See [http://github.com/mobtest](http://github.com/mobtest) for most current version

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this work except in compliance with the License. You may obtain a copy of the License in the LICENSE file, or at:

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
