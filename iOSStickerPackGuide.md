# A Guide to iOS Sticker Packs: From Planning to Publishing

## Creating the Sticker Pack

> This section will outline the process of uploading stickers and app icons to XCode, testing your sticker pack, and preparing your app for publication.

### Stickers

1. **Save Artwork:** Once you've designed your stickers, you should save them into an easily accessible folder. Your artwork should be saved as a PNG, JPEG, GIF, or APNG, as these are the only file types the App Store will allow.

2. **Upload Artwork:** Next, you need to upload your stickers into Xcode. The following steps outline how to do so:
    * Open your iMessage sticker pack project in Xcode.
    * Under `Stickers.xcstickers > Sticker Pack`, upload your stickers.

### App Icons

1. **Create App Icon:** Following Apple's [app icon design guidelines](https://developer.apple.com/design/human-interface-guidelines/ios/icons-and-images/app-icon/), you should design a simple, recognizable icon for your app. Try to use minimal words, keep the background simple, and don't include comlex design elements.

2. **Export App Icons:** Xcode requires a variety of iMessage app icon sizes, so it can be very tedious to create the different files by hand. I've found Adobe Illustrator to be a great tool for creating and exporting app icons. There are some template designs, where you can upload your artwork onto one artboard, and it will be copied onto other artboards of varying sizes. Simply export your work as a PNG, and you have all the necesarry sizes.

3. **Upload App Icons:** Next, you need to upload your app icons into Xcode. The following steps outline how to do so:
    * Open your iMessage sticker pack project in Xcode.
    * Under `Stickers.xcstickers > iMessage App Icon`, upload your artwork into the corresponding file sizes.

### Testing the Sticker Pack

1. **Testing in Simulator:** Once you have uploaded your stickers and app icons into your project, I recommend testing your code to make sure everything works as intended. The following steps outline how to do so:
    * In the upper lefthand corner of Xcode, select your desired iOS simulator device.
    * Press the `Run ▶` button, or `(⌘R)`, and you will see the app open in the simulator app.
    * Test your app in iMessage.

2. **Testing on iPhone:** I also recommend testing on your own iPhone, making sure evrything runs smoothly, and that there aren't any unforseen problems. The following steps outline how to do so:
    * Plug your iPhone into your computer.
    * In the upper lefthand corner of Xcode, under the simulator devices, select your iPhone. Your device is usually at the top of the list.
    * Unlock your device and `Run ▶ (⌘R)` the application. You’ll see Xcode install the app and then attach the debugger. The application should pop up on your phone in iMessage.
    * Test your app in iMessage.

3. **Testing in Dark Mode:** Finally, I recommend testing your sticker pack in Dark Mode. Some dark colors, like black, may not show up when being used in Dark Mode, and you want to make sure your app is as user-friendly as possible. The following steps outline how to put your device or iOS simulator into Dark Mode:
    * Option 1: Settings
        * Go to `Settings > Display & Brightness`.
        * Select `Dark` to turn on Dark Mode.
    * Option 2: Control Center
        * Pull down from the top-right corner of your device.
        * Touch and hold the brightness control.
        * Tap  `Dark Mode On`.

### Taking Screen Shots

1. **Requirements:** The App Store requires iPad and iPhone screenshots (up to 10 total, in JPEG or PNG, and RGB color space) to submit the app for review. The following steps outline how to take screenshots in the iOS simulator:
    * Open your iMessage sticker pack project in Xcode.
    * In the upper lefthand corner of Xcode, select your desired iOS simulator device.
        * If you don't know what iOS device to use for each display size, you can use the information in this [App Store Connect Help Guide](https://help.apple.com/app-store-connect/#/devd274dd925).
    * Press the `Run ▶` button, or `(⌘R)`, and you will see the app open in the simulator app.
    * Take desired screenshots.
        * One helpful terminal command I use when taking screenshots is: `xcrun simctl status_bar "iOS DEVICE NAME" override --time "TIME"`. It allows you to manually override the time on the iOS device, replacing it with a time of your choice. This ensures that all of your screenshots are consistent.
    * Repeat the process for each display size required by App Store Connect.

## Publishing the Sticker Pack

> This section will outline the process of uploading your app onto App Store Connect, submitting your app for review, and publishing it in the app store.

1. **Register an App ID:** Before you link your app to App Store Connect, you have to register an App ID. The following steps outline how to register a bundle ID:
    * First, navigate to [Apple Developer](https://developer.apple.com/account/#/overview/B59PGVARAP) and log in with your credentials.
    * Click on `Certificates, Identifiers & Profiles`.
    * Click on the Identifiers section in the left menu.
    * Click the `+ button` that's above the list and to the right of the Identifiers title.
    * Next, you will see a screen that says `Register a new Identifier`. Select the button next to App IDs, and continue to the next screen.
    * Now, you will see a form to register a new App ID. Make sure the "iOS, tvOS, watchOS" radio button is selected, type the name of the app in the Description field, fill in a unique Bundle ID, and check the capabilities your app includes. Continue to the next screen.
    * You should see an overview of the data you have entered. If it is correct, click `Register`.

2. **Add to App Store Connect:** You need to add your app to App Store connect in order to publish it on the app store. The following steps outline the process of adding the app to App Store Connect:
    * Go to [App Store Connect](https://appstoreconnect.apple.com) and log in with your credentials. 
    * Select `My Apps`
    * Click the `+ button` in the upper lefthand corner of the screen, and select`New App`.
    * Enter the required information about your app.
        * Check the platform for your app. Because you are publishing an iOS iMessage sticker pack, you will select `iOS`. 
        * Enter the name of your app.
        * Choose your app's primary language.
        * Choose your app's Bundle ID. This is the same Bundle ID that you created when registering your App ID.
        * Create a SKU number for your app. This is a unique ID for your app that is only visible to you, and will not be shown on the App Store.
        * Finally, you can limit which users see this app in App Store connect. Decide if you would like to give `Limited Access` or `Full Access`, and choose accordingly. 
        * Click `Complete`.

3. **Creating, Validating, & Distributing an Archive:** Before you can upload the app to App Store Connect, you need to create an archive. The following steps outline the process of creating and validating an archive:
    * Open your iMessage sticker pack project in Xcode. 
    * In the upper lefthand corner of Xcode, change the iOS simulator device to `Generic iOS Device`. You cannot create an archive if you have another device selected.
    * In the menu bar, choose `Product > Archive`. This will run through the archiving process, and if the archive builds successfully, it appears in the Archives Organizer.
    * After creating an archive, you must validate it. Open `Window > Organizer > Archives`. Select the archive you would like to validate and then click `Validate`. This will run through the validation process, and if it is successful, a green checkmark will appear next to the archive.
    * Finally, you want to upload the archive to App Store Connect. Open `Window > Organizer > Archives`. Select the archive you would like to upload and then click `Distribute App`.

4. **Configuring App:**  This is the step where you will add information about your application, including its title, category, pricing, and more. The following steps outline the necesarry information you will need to fill out.
    * App Information
        * Title: The name of your app as it will appear on the App Store. This can't be longer than 30 characters.
        * Subtitle: A summary of your app that appears below your app name throughout the App Store in iOS 11 or later and the Mac App Store in macOS Mojave or later.
        * Privacy Policy URL: A URL that links to your privacy policy. A privacy policy is required for all apps.
        * Category: The category that best describes this app.
        * Primary Language: If localized app information isn’t available in an App Store country or region, the information from your primary language will be used instead.
        * Bundle ID: The bundle ID must match the one you used in Xcode. It can't be changed after you upload your first build.
        * SKU: A unique ID for your app that is not visible on the App Store.
        * Apple ID: An automatically generated ID assigned to your app.
        * Age Rating: This app’s age rating will appear on the App Store across all your platforms. It is based on the app's platform with the most mature rating.
    * Pricing & Availability
        * Price: Determine whether your app will be free or paid.
        * Availability: Where your app will be available for purchace.
        * Distribution for Business and Education: Decide whether your app is available for any special distributions.
    * Prepare for Submission
        * App Previews and Screenshots: Screenshots must be in q JPG or PNG format and in the RGB color space. App previews must be in the M4V, MP4, or MOV format and can’t exceed 500 MB.
            * You need to upload App Previews and Screenshots under the iMessage App tab, as well.
        * Promotional Text: Promotional text lets you inform your App Store visitors of any current app features without requiring an updated submission. This text will appear above your description on the App Store for customers with devices running iOS 11 or later, and macOS 10.13 or later.
        * Description: A description of your app, detailing features and functionality. It will also be used for your Apple Watch app.
        * Keywords: Include one or more keywords that describe your app. Keywords make App Store search results more accurate. Separate keywords with an English comma, Chinese comma, or a mix of both.
        * Support URL: A URL with support information for your app. This URL will be visible on the App Store.
        * Marketing URL: A URL with marketing information about your app. This URL will be visible on the App Store.
        * Build: Choose a build to upload to the App Store.
        * App Store Icon: This icon will be used on the App Store. For apps built with Xcode 9 or later, add this icon in the build. For apps built with earlier versions of Xcode, add the icon here.
        * Copyright: The name of the person or entity that owns the exclusive rights to your app, preceded by the year the rights were obtained. Do not provide a URL.
        * Contact Information: The person in your organization who should be contacted if the App Review team has any questions or needs additional information.
    * Finally, submit your app for review by selecting `Submit for Review`.
