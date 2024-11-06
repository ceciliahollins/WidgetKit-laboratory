# WidgetKit-laboratory
A project to explore and experiment with WidgetKit frameworks

## Description

This project is intended to be used to explore the iOS WidgetKit framework and experiment with functionality for iOS widgets. To do this, a time widget to show the current time in an asethetically pleasing way on the home screen is developed. This allows for exploration into widget view content development, intent configurations, and timeline providers. 

![NatureTimeDemo](https://github.com/ceciliahollins/ios-widgets-tutorial/blob/main/NatureTimeDemo.gif)

![NatureTimeWidgetDemo](https://github.com/ceciliahollins/ios-widgets-tutorial/blob/main/NatureTimeWidgetDemo.gif)

## Learning Objectives

### WidgetKit

WidgetKit is an extension framework allowing for glanceable views of your app to be provided on the iPhone lock screen, home screen, and more. The framework is extremely powerful and provides a range of extension options for your app, but this tutorial begins with the basics of adding a simple widget on the home screen. View WidgetKit documentation [here](https://developer.apple.com/documentation/widgetkit).

### TimelineProvider/IntentTimelineProvider

The timeline provider constructs and timeline and tells the widget when to update its content. TimelineProvider is the protocol that should be used for non-configurable widgets, while the IntentTimelineProvider incorporates user-configurable details. The getTimeline method constructs an array of entries as well as a policy that informs the widget when to update with new information. This app uses IntentTimelineProvider to create an array of NatureTimeEntry that will be updated every minute

### StaticConfiguration/IntentConfiguration

The WidgetConfiguration must define if the widget will have user configurable properties to customize the widget. StaticConfiguration provides no user configurable properties, while IntentConfiguration will. In this app, IntentConfiguration is used to provide customization on the theme of the view. This can be updated by long pressing the widget, edit widget, and then selecting the desired theme. 

### Intent

The Intent is the configurable settings of the widget. These configrations are defined through a custom SiriKit Intent Defintion file. the NatureThemeSelection.intentdefintion file defines a very basic Intent to update the theme of the widget, which is then passed to the IntentConfiguration.

### supportedFamilies

The supportedFamilies is key to define when creating a widget, telling the os which sizes of widgets are allowed to be presented. While there are an array of WidgetFamily options that can be supported, this app focuses on home screen families of systemSmall, systemMedium, and systemLarge.

## Getting Started

### Requirements

* iOS17+

### Executing program

* Download or clone the project
* Run the project on a simulator or a device
* Go into your home screen, hold down on any space that is not an app, and click the plus button
* Search widget-tutorial and add any size
* Press and hold the widget and click on 'edit'
* View and select a different theme to change the configuration of the widget

## Help

If the project is running but the simulator or device is not showing the widget, change the scheme to directly run the target.

## Authors

Cecilia Hollins 
hollins.cecilia@gmail.com

## Version History

* 0.1
    * Initial release
    * Adding basic widget functionality
* 0.2 
    * Cleaning up broken code
    * Bumping minimum requirement to iOS17 and refactoring for needed updates
    * Adding more detailed documentation
* 1.0
    * Migrating the repository
    


## Acknowledgments

* [Apple WidgetKit documentation](https://developer.apple.com/documentation/widgetkit)

