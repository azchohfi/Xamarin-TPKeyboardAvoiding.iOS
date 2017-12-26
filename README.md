# MonoTouch (Xamarin.iOS) bindings for TPKeyboardAvoiding

These are MonoTouch (Xamarin.iOS) bindings for [TPKeyboardAvoiding](https://github.com/michaeltyson/TPKeyboardAvoiding)

## Download

NuGet: [![NuGet Badge](https://chohfi.visualstudio.com/_apis/public/build/definitions/5b5d5fff-9579-4b1f-bf21-d91546af9f53/15/badge)](https://www.nuget.org/packages/TPKeyboardAvoiding.Binding/)

MyGet: [https://www.myget.org/F/azchohfi/api/v3/index.json](https://www.myget.org/F/azchohfi/api/v3/index.json)

## Requirements

* iOS SDK
* [Xamarin Studio](https://xamarin.com/studio)
* Cocoapods
* Make
* NuGet (optional for packaging)

## Building the bindings

Just run

	make

This downloads sources via CocoaPods, creates the static objective-c library and finally links all into a .dll-file. 

## Creating the NuGet package

Run

	make package

## Pushing the NuGet package to a private feed

Setup a private NuGet feed, for example on [myget](https://www.myget.org/).
Push the package to the feed source:

	nuget push TPKeyboardAvoiding.$(version).nupkg -Source "$(source_url)" -ApiKey "$(api_key)"
