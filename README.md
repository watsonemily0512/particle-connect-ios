# Particle Connect iOS
[![Swift](https://img.shields.io/badge/Swift-5-orange)](https://img.shields.io/badge/Swift-5-orange)
[![Platforms](https://img.shields.io/badge/Platforms-iOS-yellowgreen)](https://img.shields.io/badge/Platforms-iOS-Green)
[![CocoaPods Compatible](https://img.shields.io/cocoapods/v/ParticleConnect.svg)](https://img.shields.io/cocoapods/v/Alamofire.svg)
[![License](https://img.shields.io/github/license/Particle-Network/particle-ios)](https://github.com/Particle-Network/particle-connect-ios/blob/main/LICENSE.txt)


<img width="420" src="https://static.particle.network/docs-images/add-wallet.png"></img>
<img width="420" src="https://static.particle.network/docs-images/import-private-key.png"></img>    

## Summary

Modular Swift wallet adapters and components for EVM & Solana chains. Manage wallet and custom RPC request.

![Particle Connect](https://static.particle.network/docs-images/particle-connect.jpeg)

# Prerequisites
Install the following:

Xcode 13.3.1

Make sure that your project meets the following requirements:

Your project must target these platform versions or later:

iOS 13


## Getting Started

* Clone the repo.
* Replace ParticelNetwork.info with your project info in the [Dashboard](https://dashboard.particle.network/#/login).
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>PROJECT_UUID</key>
	<string>YOUR_PROJECT_UUID</string>
	<key>PROJECT_CLIENT_KEY</key>
	<string>YOUR_PROJECT_CLIENT_KEY</string>
	<key>PROJECT_APP_UUID</key>
	<string>YOUR_PROJECT_APP_UUID</string>
</dict>
</plist>

```
* Config your app scheme url, select your app target, in the info section, click add URL Type, past your scheme in URL Schemes. 
your scheme url should be "pn" + your project app id.

    for example, if you project app id is "63bfa427-cf5f-4742-9ff1-e8f5a1b9826f", you scheme url is "pn63bfa427-cf5f-4742-9ff1-e8f5a1b9826f".
![image](https://user-images.githubusercontent.com/18244874/168455432-f25796b0-3a6a-4fa7-8ec6-adc5f8a0c46e.png)

* Add Privacy - Camera Usage Description in your info.plist file

## Build
```
pod install --repo-update
```


## Docs
1. https://docs.particle.network/connect-service/sdks/ios


## ARM64 Simulator support
For everyone with an M1 (Silicon) device who want run their projects on a simulator, There are two solutions.
1. Set arm64 as excluding architecture for Any iOS Simulator SDK. add the following to Podfile
```ruby
post_install do |installer|
  installer.pods_project.build_configurations.each do |config|
    config.build_settings["EXCLUDED_ARCHS[sdk=iphonesimulator*]"] = "arm64"
    config.build_settings["ARCHS[sdk=iphonesimulator*]"] = "x86_64"
    config.build_settings["ARCHS[sdk=iphoneos*]"] = "arm64"
  end
end
```

2. Run Xcode with Rosetta.

## Give Feedback
Please report bugs or issues to [particle-connect-ios/issues](https://github.com/Particle-Network/particle-connect-ios/issues)

You can also join our [Discord](https://discord.gg/2y44qr6CR2).





