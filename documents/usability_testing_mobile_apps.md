# Usability testing mobile apps

The goal of usability testing is to see how efficiently and succesfully someone can use your app, while having an enjoyable experience

## Testing plan
1. What are the main use cases? Describe them for yourself, and give the end state as a taks to users: buy a car, book a room etc.
2. For quantive research, track each step that a user takes with software, use heatmap technology to see what buttons and areas are touched

## Conventions
1. Are there several apps that offer similar functionality? Think refresh of table data, browse through photo's or pages, etc.
2. Is this functionality implemented in the most standard way?
3. Are the [iOS HIG (Human Interface Guidelines)](http://developer.apple.com/library/ios/#documentation/UserExperience/Conceptual/MobileHIG/Introduction/Introduction.html) followed?

## Context and environment
1. In what context is the app used? Is this a peaceful environment (e.g. home, office) or busy (street, public transportation). With or without cell phone reception/wifi?
2. Is the app tested and optimised for the most common tasks & environments?
3. How does the app support the user flow?
4. How is it to use the app outdoors with lots of light?
5. Does a busy/distracting surrounding make the app significantly harder to use?
6. Will the app be used in a nonoptimal way, like walking/running, attached to arm with an armband, one hand iPad usage?

## Clarity
1. How many call to actions are there on a screen? Can this be limited?
2. Are the main buttons or texts clearly visible and outstanding?

## Discoverability/learnability
1. Is it easy for a user to figure out how the app works?
2. Are there hidden functionalities unlocked by swiping, tilting, tap-and-hold-down?
3. Would a walk through/tutorial be needed to explain the app? Preferably not but maybe unavoidable 

## Speed 
1. How much time does it cost the app to become interactive? Is this less than 10 seconds? 
2. Is the number of steps, number of input fields to be filled out minimised?

## Network
1. In case of no network, does the app retry by itself when network has been restored?

## Error messages
1. Are all error messages clear?
2. Is there no technical jargon used that only engineers understand?
3. In case of user errors, is the explanation what the user should do clear?

## Buttons
1. Are buttons and clickable areas big enough?
2. Do buttons have a highlight state?
3. Are buttons disabled when the started process takes a long time (say more than .2 seconds)?

## iPad-specific issues
1. Does the app work as well on an iPad as on an iPad Mini? Are buttons big enough
2. Are both portrait and landscape mode supported?
3. Is the app really optimised for the iPad, and not just a blown up version of the iPhone app?

## Pleasant experience
1. What happens if there is no network? Can the app still be used to browse offline content?
2. Is the interface responsive under all circumstances, including when long running processes are busy (e.g. network calls)
3. Does the app have personality that creates a memorable and pleasant memory?

## Sign in/registration
1. Sign up: is Facebook and Twitter supported? Also standard email/password?
2. If also Facebook is supported, how do you deal with iOS 5 users? Only iOS 6 has built in support for Facebook

#Copyright and license
Copyright 2013 Mobtest, Inc. 

See [http://github.com/mobtest](http://github.com/mobtest) for most current version

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this work except in compliance with the License. You may obtain a copy of the License in the LICENSE file, or at:

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.