# unifi_iOS_Shortcuts
iOS Shortcuts for Unifi gears
<br/>

## "Unifi WLAN Users" <br> Create ad Share (Radius) User Accounts from iOS Contacts as text or Apple Mobileconfig

<br/>
<p>
<img src="https://github.com/user-attachments/assets/97d2e06d-06c2-451a-a665-2ffdb712b19c" width="56">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &#8618; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://github.com/user-attachments/assets/150fbc7b-bc97-4601-8953-0b453c44c9c7" width="56">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &#8618; &nbsp;&nbsp;&nbsp;&nbsp;<img width="56" alt="mobileconfig" src="https://github.com/user-attachments/assets/7cd4d8ec-8c9d-401e-a24a-e4324d3523d1"/>
</p>

iOS Contact &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp;Unifi Radius &nbsp; &nbsp; &nbsp;  &nbsp; Mobileconfig (or user/pass as txt)
<br/>&nbsp;<br/>
The following modular Shortcuts make it possible to create and share Unifi WLAN User Access (Radius Users) for __WPA3 Enterprise Wlan__ on the Unifi Dream Machine (UDM Pro) by simply choosing an iOS [Contact](https://apps.apple.com/de/app/kontakte/id1069512615&ved=2ahUKEwibvJOVqtKTAxVnk_0HHVdzEesQFnoECB0QAQ&usg=AOvVaw1Qs6n_VmzjWESGfwz8_NBL). With the option to create and share via AirDrop an [Apple configuration profile](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://support.apple.com/guide/apple-configurator-mac/create-and-edit-configuration-profiles-pmd85719196/mac&ved=2ahUKEwiprP_tqdKTAxUShv0HHTG7DKIQFnoECBwQAQ&usg=AOvVaw2x7peiDG4veEG8vEDxAXkS) __(Mobileconfig)__, it's then a __one click install__ without the need to enter any password on the moble device.

* Creates the Username (FirstName + First Letter of Last Name)
* Generates a "random" password based on a hash of all data of the iOS contact with a configured password length
* Checks if radius user exists and creates it if not existing
* Lets you decide if you want to share the account data via text or mobileconfig
* Creates mobileconfig (if chosen)
* Adds your radius cert to the mobileconfig (if configured)
* Signs the mobileconfig with your s/mime cert (if configured)
* Shares the result (User Account as Plain Text or Mobileconfig)

&nbsp;<br/>
> [!NOTE]
>Add the URL of your Radius Certificate in the config, if you want to avoid any user ask to trust the wlan when installing the mobileconfig on the device

> [!NOTE]
>Add the Url of your s/mime PKCS12 if you want that the mobileconfig to be digitally signed, so that it is shown as trusted during installation on the device

> [!IMPORTANT]
>For on-device signature of the mobileconfig on your iOS device (iPhone / iPAD) the free AppStore App [Scriptable](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://apps.apple.com/de/app/scriptable/id1405459188&ved=2ahUKEwjUk-uHyNGTAxWxbvEDHS8YPAAQFnoECB8QAQ&usg=AOvVaw2WNuxj6WeSo4Wv4KW4j5Kp) is required, which will run the required JavaSCript code.

### Start Point with iOS Contact to create Account for as Input Parameter

* __Unifi WLAN Users__
https://www.icloud.com/shortcuts/5e638f2a93a54884b3ca6f41e696429a
<br/>Initial ShortCut. This Shortcut can be put on your homescreen / added in your ShareSheet

* Config File (__Put YOUR Config first__)
Unifi Public Config
https://www.icloud.com/shortcuts/179f8461bba34e61bed6ebd94951c2e5
<br/>Centralized Config as shortcut. Resulting Data Dictionary is propagated to the other shortcuts

* Start Execution Flow
Unifi Public Config Execute
https://www.icloud.com/shortcuts/49b8063fb143453e9fc0f30c98f205ed
<br/>Starts the steps as single shortcuts

### Define User/Pass and Create Radius User if required
* Unifi Web Login
https://www.icloud.com/shortcuts/5a4aeba29f60464d96a543f17a871e91
<br/>Logins to your unifi UDM network app and stores the token.

* Unifi LoginName
https://www.icloud.com/shortcuts/b05372b6fa76419f85dd23e1ea2bac8a
<br/>Creates a Login Name for the User Account to create based on iOS contact (taking: FirstName + First Letter of Last Name)

* Unifi Password
https://www.icloud.com/shortcuts/fdfe1433c6974ef4afa375411dbc23d9
<br/>Generates a Password with configured length from iOS Contact hash to have an individual pass

* Unifi Web Account
https://www.icloud.com/shortcuts/b111bd6777e542668b812082b808b7ce
<br/>Creates the Radius User in your network app (if not existing)

### Create Mobile Config and sign (if configured such)
* Unifi Create FullMobileconfig
https://www.icloud.com/shortcuts/cc13e7e77ccf4cb798f03a8e59da8615
<br/>Creates the Apple profile (mobileconfig) for given user account

* Radius Cert base64
https://www.icloud.com/shortcuts/77d0393257284b1fafbd898287600f1e
<br/>Fetches the radius cert to insert into the mobileconfig

* Unifi Sign Mobileconfig
https://www.icloud.com/shortcuts/2c2a62d3b35d4eec83448435356d47db
<br/>Digitally signs the profile with your PKCS12 s/mime cert
<br/>(Requires App [Scriptable](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://apps.apple.com/de/app/scriptable/id1405459188&ved=2ahUKEwjUk-uHyNGTAxWxbvEDHS8YPAAQFnoECB8QAQ&usg=AOvVaw2WNuxj6WeSo4Wv4KW4j5Kp))

### Show result (Plain Text User Account or Mobileconfig)
* Unifi show result
https://www.icloud.com/shortcuts/dd49fc5aa7e140178a31ffaecb689a2d
<br>Shows the result of the created user account (as plain text or mobileconfig)



