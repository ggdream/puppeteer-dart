# Changelog

## 2.12.0
- Update to Chromium 105

## 2.11.0
- Update to Chromium 104

## 2.10.0
- Update to Chromium 103
- Use dart enhanced `enums` for all enumerations in the protocol 

## 2.9.0
- Update to Chromium 102

## 2.8.0
- Update to Chromium 101

## 2.7.0
- Update to Chromium 100
- Resolving browser paths in windows

## 2.6.0
- Update to Chromium 99

## 2.5.0
- Add `BrowserPath` to have access to installed browser executable path.
```dart
var browser = await puppeteer.launch(executablePath: BrowserPath.chromeCanary);
```

- Fix bug to make current version work with chrome stable 96

## 2.4.0
- Update Chromium to version 97

## 2.3.0
- Update Chromium to version 93

## 2.2.1
- Make `defaultViewport` nullable in the `connect` method.

## 2.2.0
- Update Chromium to version 92
- Add drag-and-drop support

## 2.1.0
- Update Chromium to version 91

## 2.0.0
- Migrate to null-safety
- Update Chromium to version 90

## 1.22.0
- Update Chromium to version 87

## 1.21.0
- Update Chromium to version 87

## 1.20.1
- Fix `Browser.close()` error

## 1.20.0
- Update Chromium to version 86

## 1.19.0
- Update Chromium to version 85

## 1.18.0
- Update Chromium to version 84
- Add `Mouse.wheel`

## 1.17.0
- Update Chromium to version 81
- Revert change to `uploadFile` implementation.

## 1.16.1
- Fix a bug with the new `uploadFile` implementation.

## 1.16.0
- Update to chromium 722234

## 1.15.1
- Expose `ClientError` class
- (internal) Revert previous change in `jsHandle.uploadFile`

## 1.15.0
- Add element.select and element.evaluate for consistency
- Prepare jsHandle.uploadFile for CDP Page.handleFileChooser removal

## 1.14.1
- Export class `Target` in `puppeteer.dart`

## 1.14.0
- Update Chrome to version 79
- Add `Page.emulateTimezone` and `Page.emulateMediaFeatures`
- Deprecate `Page.emulateMedia` in profit of `Page.emulatedMediaType`
- Fix a "Concurrent modification error" when navigating from a page with iframes.

## 1.13.0
- Fix a NullPointerException in NetworkManager
- (internal) Add more tests for headful mode
- (internal) Remove all implicit casts (preparation for nnbd)

## 1.12.0
- Fix bug in `puppeteer.connect()`
- Add the same capabilities that pupeeteer Node.JS to `puppeteer.launch` for the management of the flags passed to Chromium.
- Add `userDataDir` to `puppeteer.launch` to allow managing the user data directory.
  By default, we now use a temporary data directory in the system temp folder.
- Add more tests for launching and connecting to chromium

## 1.11.0
- Update Chromium version to 686378

## 1.10.0
- Introduce file chooser interception
- Update Chromium version to 674921

## 1.9.0
- Update Chromium version to 672088
- Update dependencies
- Fixes for Dart 2.4.0

## 1.8.0+1
- Fix regression in `page.tracing`

## 1.8.0
- Update Chromium version to 669486
- Add an `IOSink` [output] parameter to [Page.pdf] as an alternative to returning the whole PDF bytes in memory.

## 1.7.3
- Update Chromium version to 666595
- Remove --disable-gpu flag passed to Chromium on Windows

## 1.7.2
- Update Chromium version to 662092

## 1.7.1
- Enable more Dart lints

## 1.7.0
- Add `page.ccessibility` feature
- Update default Chromium version to 662092

## 1.6.0
- Add `puppeteer.connect` to connect to an existing Chromium instance
- Add `slowMo` parameter for `puppeteer.launch` et `puppeteer.connect` to slow down communications with the browser.
- Create `Worker` from service_worker and shared_worker.
- Use a default viewport of 1280x1024 by default (allow to pass null to disable the default).
- Add a small "plugin" system
- Add the `StealthPlugin` to automatically applies various techniques to make detection of headless puppeteer harder.
- Add `Page.clickAndWaitForNavigation` for convenience.
- Add `Page.coverage` feature
- Add `Page.metrics` feature
- Add `Page.tracing` feature

## 1.5.0
- Rename classes `Frame`, `Request` & `Response` to match the puppeteer API
- Add Worker class
- Add more test for the network API

## 1.4.0
- Add more unit tests and more documentation
- Fix bugs in request interception

## 1.3.0
- Add more unit tests and more documentation
- Update default chromium
- Add example for screencast
- Fix bugs

## 1.2.1

- Add some documentation and examples in the source code (still work in
progress: not all classes are documented yet).

## 1.2.0

- Start a browser with `puppeteer.launch` instead of
`Browser.start` to align with the puppeteer API
- Add a list of all the devices from chrome:
Accessible with: `page.emulate(puppeteer.devices.iPhone6)`
- Add tests

## 1.1.0

- Add some unit tests from the Puppeteer/Node.JS project and fix some bugs.

## 1.0.0

- Initial port of Puppeteer in Dart
