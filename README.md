## Two-Factor Authentication with Google Authenticator App using JAVA
Two-Factor Authentication (TFA or 2FA) is a second step in login sequence that asks you to enter 6-digits code sent 
to you by email, text message or Google Authenticator app and this code expires 
in 30 or 60 seconds. This second step of authentication makes your account more 
secure, because even if someone knows your login and password, they still need 
your physical mobile device to see 2FA code sent to you.

This code example demonstrates how to use TFA with Google Authenticator App.

 ### Prerequisites
 * Java 8+
 * Maven ^3.6.0
 * Google Authenticator App. Can be downloaded on [App Store](https://apps.apple.com/ru/app/google-authenticator/id388497605)
 and [Google Play](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=uk)

### How to Run & Use
1. Install **Google Authenticator app** on your mobile phone.
2. Run the **__MainApplication.class__** in you IDE.
3. You should see the generated **'QRCode.png'** image in your project root folder.
4. Now open your Google Authenticator app. Press ‘*plus*’ button to add a new entry and select ‘Scan Barcode’.
5. Open the generated **'QRCode.png'** image and scan it.
6. After scanning this QR code you should see a new entry in Google Authenticator entry list 
with 6-digits being regenerated every 30 seconds.
7. In the project console that is still running you can see the text `Please enter 2fA code here ->`. So you need to enter 6-digits code from your Google Authenticator App.

### Results
If you did everything correctly then after entering 2fa code to the console you should see the following text message:

`Logged in successfully`

Or if 2FA code is already expired or invalid:

`Invalid 2FA Code`

### Notes & Tips
To generate new **__secret key__** for each user for example just use `generateSecretKey()` method from `Utils.class`.

Height and Width of the QR image can be changed by passing them to this method `Utils.createQRCode()`.

Email and Company name (which are just any string) can be also changed in order to display different name 
for each user in their Google Authenticator entry list.


### Community
* Please send us your suggestions on how we make this code even more useful for the development community or contribute to this repo!
* Check out our [blog article](https://oril.co/blog/two-factor-authentication-with-java-and-google-authenticator/) with more details!
