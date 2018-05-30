
a) What is the difference between Internal Storage & External Storage?


When building an app that uses the internal storage, the Android OS creates a unique folder, which will only be accessible from the app, so no other app, or even the user, can see what's in the folder.

The external storage is more like a public storage, so for now, it's the sdcard, but could become any other type of storage (remote hard drive, or anything else).

The internal storage should only be used for application data, (preferences files and settings, sound or image media for the app to work). If you intent to download many mp3s, i'd reccomend saving them to external storage, as the external storage is often bigger. Besides, storing data on the internal storage may prevent the user to install other applications.


b) For how long the data resides in the cache?

As long as user doesnt clear cache manually from system settings.



c) What are the critical Permissions and Normal Permissions? What are the
examples of each?

Normal permissions cover areas where your app needs to access data or resources outside the app's sandbox, but where there's very little risk to the user's privacy or the operation of other apps. For example, permission to set the time zone is a normal permission.

If an app declares in its manifest that it needs a normal permission, the system automatically grants the app that permission at install time. The system doesn't prompt the user to grant normal permissions, and users cannot revoke these permissions.

Ex :
ACCESS_LOCATION_EXTRA_COMMANDS
ACCESS_NETWORK_STATE
ACCESS_NOTIFICATION_POLICY
ACCESS_WIFI_STATE
BLUETOOTH
BLUETOOTH_ADMIN
BROADCAST_STICKY
CHANGE_NETWORK_STATE

Critical permissions cover areas where the app wants data or resources that involve the user's private information, or could potentially affect the user's stored data or the operation of other apps. For example, the ability to read the user's contacts is a Critical permission. If an app declares that it needs a Critical permission, the user has to explicitly grant the permission to the app. Until the user approves the permission, your app cannot provide functionality that depends on that permission.

To use a Critical permission, your app must prompt the user to grant permission at runtime. For more details about how the user is prompted.

Ex: 
Read Write calender
Camera
Read Write Contacts
Location Access
