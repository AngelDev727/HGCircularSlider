# HGCircularSlider

[![Backers on Open Collective](https://opencollective.com/HGCircularSlider/backers/badge.svg)](#backers) [![Sponsors on Open Collective](https://opencollective.com/HGCircularSlider/sponsors/badge.svg)](#sponsors) [![Twitter: @GhazouaniHamza](https://img.shields.io/badge/contact-@GhazouaniHamza-blue.svg?style=flat)](https://twitter.com/GhazouaniHamza)
[![CI Status](http://img.shields.io/travis/HamzaGhazouani/HGCircularSlider.svg?style=flat)](https://travis-ci.org/HamzaGhazouani/HGCircularSlider)
[![Version](https://img.shields.io/cocoapods/v/HGCircularSlider.svg?style=flat)](http://cocoapods.org/pods/HGCircularSlider)
[![License](https://img.shields.io/cocoapods/l/HGCircularSlider.svg?style=flat)](http://cocoapods.org/pods/HGCircularSlider)
[![Language](https://img.shields.io/badge/language-Swift-orange.svg?style=flat)]()
[![Platform](https://img.shields.io/cocoapods/p/HGCircularSlider.svg?style=flat)](http://cocoapods.org/pods/HGCircularSlider)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
<br />

[![codebeat badge](https://codebeat.co/badges/c4db03f5-903a-4b0e-84bb-98362fc5bd7a)](https://codebeat.co/projects/github-com-hamzaghazouani-hgcircularslider)
[![Documentation](https://img.shields.io/cocoapods/metrics/doc-percent/HGCircularSlider.svg)](http://cocoadocs.org/docsets/HGCircularSlider/)
[![Readme Score](http://readme-score-api.herokuapp.com/score.svg?url=https://github.com/hamzaghazouani/hgcircularslider/)](http://clayallsopp.github.io/readme-score?url=https://github.com/hamzaghazouani/hgcircularslider/tree/develop)

## Example

![](/Screenshots/Bedtime.gif) ![](/Screenshots/Player.gif) ![](/Screenshots/OClock.gif) ![](/Screenshots/Other.gif) ![](/Screenshots/Circular.gif)

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## You also may like

* **[HGPlaceholders](https://github.com/HamzaGhazouani/HGPlaceholders)** - Nice library to show placeholders for any UITableView in your project
* **[HGRippleRadarView](https://github.com/HamzaGhazouani/HGRippleRadarView)** - A beautiful radar view to show nearby users with ripple animation, fully customizable

## Requirements

- iOS 9.0+
- Xcode 11.4

## Installation

HGCircularSlider is also available through [Swift Package Manager](https://swift.org/package-manager/)

Follow this [doc](https://developer.apple.com/documentation/xcode/adding_package_dependencies_to_your_app?language=swift).

HGCircularSlider is also available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

``` ruby
pod 'HGCircularSlider', '~> 2.2.1'
```

HGCircularSlider is also available through [Carthage](https://github.com/Carthage/Carthage). To install
it, simply add the following line to your Cartfile:


``` ruby
github "HamzaGhazouani/HGCircularSlider"
```

## Usage

1. Change the class of a view from UIView to CircularSlider, RangeCircularSlider or MidPointCircularSlider
2. Programmatically:

```swift
let circularSlider = CircularSlider(frame: myFrame)
circularSlider.minimumValue = 0.0
circularSlider.maximumValue = 1.0
circularSlider.endPointValue = 0.2
```
OR
```swift
let circularSlider = RangeCircularSlider(frame: myFrame)
circularSlider.startThumbImage = UIImage(named: "Bedtime")
circularSlider.endThumbImage = UIImage(named: "Wake")

let dayInSeconds = 24 * 60 * 60
circularSlider.maximumValue = CGFloat(dayInSeconds)

circularSlider.startPointValue = 1 * 60 * 60
circularSlider.endPointValue = 8 * 60 * 60
circularSlider.numberOfRounds = 2 // Two rotations for full 24h range
```
OR
```swift
let circularSlider = MidPointCircularSlider(frame: myFrame)
circularSlider.minimumValue = 0.0
circularSlider.maximumValue = 10.0
circularSlider.distance = 1.0
circularSlider.midPointValue = 5.0
```
##### If you would like to use it like a progress view 
```
let progressView = CircularSlider(frame: myFrame)
progressView.minimumValue = 0.0
progressView.maximumValue = 1.0
progressView.endPointValue = 0.2 // the progress 
progressView.userInteractionEnabled = false 
// to remove padding, for more details see issue #25
progressView.thumbLineWidth = 0.0
progressView.thumbRadius = 0.0
```

## Documentation
Full documentation is available on [CocoaDocs](http://cocoadocs.org/docsets/HGCircularSlider/).<br/>
You can also install documentation locally using [jazzy](https://github.com/realm/jazzy).

## References
The UI examples of the demo project inspired from [Dribbble](https://dribbble.com).

[Player](https://dribbble.com/shots/3062636-Countdown-Timer-Daily-UI-014) <br/>
[BasicExample](https://dribbble.com/shots/2153963-Dompet-Wallet-App)<br/>
[OClock](https://dribbble.com/shots/2671286-Clock-Alarm-app)<br/>

The project is Inspired by [UICircularSlider](https://github.com/Zedenem/UICircularSlider)

## License

HGCircularSlider is available under the MIT license. See the LICENSE file for more info.
