#Apple iOS Development
Step-by-step procedure on how to create certificates to install project to iPhone or archive project for Ad Hoc or Enterprise distribution.

##Certificates (code signing certificate)
1. Keychain Access > Certificate Assistant > Request for a Certificate from a Certificate Authority
2. Member Center > Certificates > Add > Add AdHoc
3. Download newly created Certificate 
4. Double click the downloaded certificate to add it to Keychain Access

##App ID

1. iOS App IDs (click +)
2. Register iOS App ID (fill out form) > Continue
3. Submit

##Devices

1. iOS Devices (click +) 
2. Register devices for testing (Name and UDID) > Continue
3. Save

##Provisioning Profile

1. Member Center > Provisioning Profile > Add iOS Provisioning Profile (click +) > Ad Hoc (select radio button) > Continue
2. Select App ID > Continue
3. Select certificates (added to Keychain) > Continue
4. Select devices
5. Profile Name > Generate
6. Download
7. Done
8. Double click the .mobileprovision file to install the Provisioning Profile in Xcode

##Xcode

1. General > Select Team
2. Build Settings > Select the Provisioning Profile installed
3. General > Fix Issue (click)
4. Certificate Not Found > Request (click)

	NOTE: This will automatically create a certificate for developer in the Apple Member Center and install the signing certificate in the Keychain

##Push Notification 

1. Identifiers > App IDs
2. Create Certificate for Parse > Continue
3. Choose file > Generate
4. Download (click) > Double click the .cer file to be added to your Keychain
5. Export the Push Notifications certificate from Keychain (.p12)

##Parse

1. Upload the .p12 file
2. Client push enabled? (click button)

##Archive Project

1. Product > Archive
2. Organizer - Archives > Export (click)
3. Save for Ad Hoc  Deployment > Next
4. Choose deployment team
5. Keychain access permission modal > Always Allow


	NOTE: This happens when the provisioning profile and certificates are first time to use

6. Export (click) > Name your .ipa file (include version and build number as post fix example: AppName-v1.0.0-b1)
