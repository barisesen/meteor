Meteor add platform Android

Following steps solved the permission issues I mentioned above for UBUNTU 14.04:
1. meteor remove-platform android
2. meteor remove-platform ios (if added)
3. sudo meteor add-platform android

Step 3 leads to:
Your system does not yet seem to fulfill all requirements to build apps for Android. 
But when I (4.) sudo meteor add-platform android again, the message changes to:
error: android: platform is already added

meteor run android-device then leads to permission issues. Solved this by:
5. sudo chown -R $(whoami) ~/.meteor
6. In your project folder sudo chown -R $(whoami) .meteor/
