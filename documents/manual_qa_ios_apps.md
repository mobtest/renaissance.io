# Manual QA testing for iOS apps 

## Functional testing
What functions is the app supposed to have?
Does the app indeed support these functions?

## Hardware

Which of the following hardware models does the app support?

1. iPhone 3g, iPhone 3gs, iPhone 4 (Retina), iPhone 4s, iPhone 5 (4-inch)
2. iPad, iPad 2, iPad 3 (alias new, Retina), iPad 4, iPad Mini (not Retina, smaller 7.9’’ screen)
3. iPod Touch 4, iPod Touch 5 (4-inch Retina)

You might consider iPhone 3G, 3GS and iPad obsolete.

## Operating system
Which of the following hardware models does the app support?

1. iOS 4.x
2. iOS 5.x
3. iOS 6.x

You might deem iOS 4.x obsolete

## Device Orientation and rotation

Does the app support both landscape and portrait orientation?
Any particular views (UIViewControllers) that support different orientations?

## Network
How does the app behave under these network circumstances:

1. no network at all
2. intermittent network
3. cellular slow: 2G (Edge)
4. cellular medium: 3G (UTMS, CDMA) 
5. cellular fast: 4G(LTE)
6. Wifi
7. Public wifi with HTTP authentication (e.g. Starbucks)

Other network questions:

1. Is your app tested on all carriers in your target market?
2. Is offline access to (part of)data required?
3. Does the app make sense for wifi-only devices?
4. Does the app resume sending/downloading data after a connection has been reestablished?

## Security
1. Is confidential data sent over unsecured HTTP?
2. Are user credentials like username/password sent over unsecured HTTP?
3. Are sensitive files stored unencrypted on the device?
4. Would a pin code on the app (e.g. DropBox) be advisable?
5. What happens if a device is stolen? Should the app be remotely wiped?


## Memory
How does the app behave under low memory circumstances:

1. Open up lots of Mobile Safari windows and go back to the app
2. Use an old model device like the original iPad (maybe even not supported model anymore)

Trigger memory warnings in the Simulator.

## Text input
1. Can a very large text be entered?
2. What happens on suspend and resume? Can I continue entering text where I left off?

## Context and environment
1. How is it to use the app outdoors with lots of light?
2. Does a busy surrounding make the app significantly harder to use?

## Accessability
Are controls accessible? Are accessibility labels set?

## Crash logs
Use one of the following services to collect and analyse crash logs:

1. Crashlytics
2. Crittercism
3. iTunes Connect

## Installation
1. What is the size of the initial download, is it too big for cellular downloads?
2. - size of the downloadable, too big for cellular?

## Updates
1. What is the size of the updated app, is it too big for cellular downloads?
2. Are there database updates? Have they been tested with multiple previous releases
3. Is CoreData used for database migrations?
4. Are there other persistent data/settings that should be tested with updates?

## Guidelines
1. are the Apple App Review Guidelines followed?
2. Are the iOS HIG (Human Interface Guidelines) followed?
3. Are all trademarks and copyrights covered?


