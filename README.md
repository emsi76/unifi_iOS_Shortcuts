# unifi_iOS_Shortcuts
iOS Shortcuts for Unifi gears

## "Unifi WLAN Users" - Create ad Share (Radius) User Account from iOS Contacts
The following modular Shortcuts make it possible to create and Share Unifi WLAN User Access (Radius Users) for __WPA3 Enterprise Wlan__ on the Unifi Dream Machine (UDM Pro) by simply choosing an iOS Contact. With the mobileconfig option it's a one click profile install without the need to enter any password on the moble device.
* Creates the Username (FirstName + First Letter of Last Name)
* Generates a "random" password based on a hash of all data of the iOS contact with a configured password length
* Checks if radius user exists and creates it if not existing
* Lets you decide if you want to share the account data via text or mobileconfig
* Creates mobileconfig (if chosen)
* Adds the radius cert (if configured)
* Signs the profile with your s/mime cert (if configured)
* Shares the result (User Account as Plain Text or Mobileconfig)

For on-device signature of the mobileconfig on your iOS device (iPhone / iPAD) the AppStore App [Scriptable](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://apps.apple.com/de/app/scriptable/id1405459188&ved=2ahUKEwjUk-uHyNGTAxWxbvEDHS8YPAAQFnoECB8QAQ&usg=AOvVaw2WNuxj6WeSo4Wv4KW4j5Kp) is required, which will run the required JavaSCript code.

### Start Point with iOS Contact to create Account for as Input Parameter

* __Unifi WLAN Users__
https://www.icloud.com/shortcuts/5e638f2a93a54884b3ca6f41e696429a

* Config File (__Put YOUR Config first__)
Unifi Public Config
https://www.icloud.com/shortcuts/179f8461bba34e61bed6ebd94951c2e5

* Start Execution Flow
Unifi Public Config Execute
https://www.icloud.com/shortcuts/49b8063fb143453e9fc0f30c98f205ed

### Define User/Pass and Create Radius User if required
* Unifi Web Login
https://www.icloud.com/shortcuts/5a4aeba29f60464d96a543f17a871e91

* Unifi LoginName
https://www.icloud.com/shortcuts/b05372b6fa76419f85dd23e1ea2bac8a

* Unifi Password
https://www.icloud.com/shortcuts/fdfe1433c6974ef4afa375411dbc23d9

* Unifi Web Account
https://www.icloud.com/shortcuts/b111bd6777e542668b812082b808b7ce

### Create Mobile Config and sign (if configured such)
* Unifi Create FullMobileconfig
https://www.icloud.com/shortcuts/cc13e7e77ccf4cb798f03a8e59da8615

* Radius Cert base64
https://www.icloud.com/shortcuts/77d0393257284b1fafbd898287600f1e

* Unifi Sign Mobileconfig
https://www.icloud.com/shortcuts/2c2a62d3b35d4eec83448435356d47db

### Show result (Plain Text User Account or Mobileconfig)
* Unifi show result
https://www.icloud.com/shortcuts/dd49fc5aa7e140178a31ffaecb689a2d



