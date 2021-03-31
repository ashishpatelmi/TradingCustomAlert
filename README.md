# Trending Custom Alert: You can use a custom trending alert for more better app UI. Very easy to use. ✓

<a href="https://docs.swift.org/swift-book/" rel="nofollow">
<img src="https://camo.githubusercontent.com/cb475f8dadad0c4288af40474eb0e17f948ef16d0b0ccedcd488e3f495467943/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f73776966742d352e302d79656c6c6f77677265656e" data-canonical-src="https://img.shields.io/badge/swift-5.0-yellowgreen" style="max-width:100%;">
</a>
<a href="#">
<img src="https://camo.githubusercontent.com/7a1635979240523def7c8b8a7475c21c8892e34656e81578fcee46d23c1d49a2/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f706c6174666f726d2d694f532d726564" data-canonical-src="https://img.shields.io/badge/platform-iOS-red" style="max-width:100%;">
</a>
<a href="https://github.com/ashishpatelmi/TrendingCustomAlert/blob/main/LICENSE">
<img src="https://camo.githubusercontent.com/7b232a0e05a8d73a46bad2e4748afd9e9d0ab04e217b38f03eede63b86da220a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6c6963656e63652d4d49542e2d6f72616e6765" data-canonical-src="https://img.shields.io/badge/licence-MIT.-orange" style="max-width:100%;">
</a>

# Description

This is a custom alert with different customization options which enhance the alert view with animation. User can add custom image at top, apply corner radius on alert view and buttons. User can able to apply custom colour and title for buttons. 

There is custom three button action sheet with Banner image and title name with icon. User can able to customise by their own requirements.

There are custom image as well as webView popup. In which user can able to open any image and web url. 

# Sample

![video](/Media/alert.gif)

<p align="center">
    <a href="https://www.mindinventory.com" style="pointer-events: stroke;" target="_blank">
        <img src="/Media/mi.png" width="210" height="70" title="MindInventory">
    </a>
</p>

# Table of content


- [Description](#description)
- [Sample](#sample)
- [UI Controls](#ui-controls)
- [Features](#features)
- [Usage](#usage)
- [By Apple](#by-apple)
- [License](#license)


# UI Controls

- Label
- Button
- ImageView
- WebView

# Features

  **Alert**

  - Add custom image at top with hide/show option.
  -	Custom corner radius for alert view and buttons.
  -	Custom colour and title for buttons.

  **ActionSheet**

  -	Custom Banner image on action sheet.
  -	Custom title with icon.
  -	Hide/show Cancel button as well as Banner.

  **PopupView**

  -	Custom Title with Image and WebView popup.

# Usage

- Download and run source in your Xcode.

- On action event implement `showCustomAlert()` which give you bunch of different customization option related to alert, whatever you want to customize just pass data in the method. You can also check different customization in the source.

```swift
showCustomAlert(title: "LogOut",
                message: "Are you sure you want to LogOut? ",
                alertType: .twoButton(title1: "No", title2: "Yes"),
                icon: "user",
                alertRadius: 70,
                btnRadius: 25,
                customCorners: [.layerMinXMinYCorner, .layerMaxXMaxYCorner])
```
- Here we have different options for Alert:
    - title: Custom title.
    - message: Custom message. 
    - alertType: We can choose oneButton or towButton alert, also we can apply custom button title and colour.
    - icon: We can add icon on top of the alert.
    - alertRadius: It will apply radius on main alertview.
    - btnRadius: It will apply radius on buttons.
    - customCorners: We can customize any corner of alertview. It will apply on alertview as well as on buttons.

- On action event implement `showThreeActionButtonPicker()` which provides you customization option related to actionsheet, in which you can add custom banner on the top of action sheet, whatever you want to customize just pass data in the method. You can also check different customization in the source.

```swift
showThreeActionButtonPicker(title1: "Help", btnIcon1: "ic_help_circle",
                            title2: "Info", btnIcon2: "ic_info", btnStyle2: .default,
                            title3: "Logout", btnIcon3: "ic_logout", btnStyle3: .destructive,
                            banner: "gender", isShowBanner: true,
                            isShowCancle: true, controller: self)
```
- Here we have different options for Actionsheet:
    - title: Custom title.
    - btnIcon: Custom icone for button.
    - btnStyle: We can give .default, .destructive style for button.
    - banner: We can add custom banner on actionsheet.
    - isShowBanner: Hide/Show banner.
    - isShowCancle: Hide/Show Cancle button.
    - controller: Need to pass self controller.

- For Custom popup, pass data title, image or web url to `ImageAlertVC`. As you can see in source.
 
- Web popup view: We can pass name and webUrl in the url, it will load in a popup view.
  
```Swift
if let popupViewController = UIStoryboard(name: "Main", bundle: nil).instantiateViewController(withIdentifier: "ImageAlertVC") as? ImageAlertVC {
            
    popupViewController.name = "Terms & Conditions"
    popupViewController.url = URL(string: "https://www.apple.com")
    self.present(popupViewController, animated: true)
}

```

- Image popup view: We can pass name and image in the imageName, it will load in a popup view.

```Swift
if let popupViewController = UIStoryboard(name: "Main", bundle: nil).instantiateViewController(withIdentifier: "ImageAlertVC") as? ImageAlertVC {
            
    popupViewController.name = "Burj Al Arab"
    popupViewController.imageName = "burj _al_arab"
    self.present(popupViewController, animated: true)
}

```

# By Apple

- Xcode 12
- iOS 11+

# LICENSE!

GenerateTrendingCustomAlert is [MIT-licensed](/LICENSE).
