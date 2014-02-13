Android-Rate
============

Android-Rate is a library to help you promote your app by prompting users to rate the app after using it for a few days.

<<<<<<< HEAD
![Screen shot](https://raw.github.com/hotchemi/Android-Rate/master/documents/screenshot.png)
=======
<<<<<<< HEAD
Android-Rate is a library to help you promote your android app by prompting users to rate the app after using it for a few days.

![screen shot](https://raw2.github.com/hotchemi/Android-Rate/master/documents/screen_shot.png)
=======
![Screen shot](https://raw2.github.com/hotchemi/Android-Rate/master/documents/screen_shot.png)
>>>>>>> 28d7a9d... v0.0.3 release.
>>>>>>> 7adac95... v0.0.3 release.

## Download

Download from maven repository(GitHub) via gradle.

```groovy
repositories {
    mavenCentral()
    maven { url 'https://raw.github.com/hotchemi/Android-Rate/master/repository/' }
}
android {
    dependencies {
<<<<<<< HEAD
        compile 'hotchemi.android.rate:android-rate:0.0.2'
=======
<<<<<<< HEAD
<<<<<<< HEAD
        compile 'hotchemi.android.rate:android-rate:0.0.3'
=======
        compile 'hotchemi.android.rate:android-rate:0.0.2'
>>>>>>> 3876ba2... v0.0.2
=======
        compile 'hotchemi.android.rate:android-rate:0.0.3'
>>>>>>> 28d7a9d... v0.0.3 release.
>>>>>>> 7adac95... v0.0.3 release.
    }
}
```

## Demo

<<<<<<< HEAD
Please try to move the [sample module](https://github.com/hotchemi/Android-Rate/tree/master/sample)！
=======
<<<<<<< HEAD
<<<<<<< HEAD
Please try to move the [sample module](https://github.com/hotchemi/Android-Rate/tree/master/sample/).
=======
Please try to move the [sample module](https://github.com/hotchemi/Android-Rate/tree/master/sample)！
>>>>>>> 3876ba2... v0.0.2
=======
Please try to move the [sample module](https://github.com/hotchemi/Android-Rate/tree/master/sample/).
>>>>>>> 28d7a9d... v0.0.3 release.
>>>>>>> 7adac95... v0.0.3 release.

## How to use

### Implementation

Call `AppRate.monitor(Context)` and `AppRate.showRateDialogIfMeetsConditions(Context)` in your launcher activity.

```java
@Override
protected void onStart() {
    super.onStart();
    // Monitor launch times and duration of feeding period from installation
    AppRate.monitor(this);
    // call this method whenever event you want to trigger showing rate dialog
    AppRate.showRateDialogIfMeetsConditions(this);
}
```

### Custom conditions

The default condition to show rate dialog is as below:

* App is launched more than 10 times
* App is launched more than 10 days later than installation.

If you want to use your own condition, please call `AppRate.setLaunchTimes(int)` and `AppRate.setInstallDays(int)`.

```java
@Override
protected void onStart() {
    super.onStart();
    // method chain
<<<<<<< HEAD
    AppRate.setInstallDays(0) // default 10
<<<<<<< HEAD
=======
>>>>>>> 3876ba2... v0.0.2
=======
    AppRate.setInstallDays(0) // default 10, 0 means install day.
>>>>>>> 28d7a9d... v0.0.3 release.
>>>>>>> 7adac95... v0.0.3 release.
           .setLaunchTimes(3) // default 10
           .monitor(this);
}
```

### Custom rate dialog

If you want to use your own dialog labels, override string xml resources  your application.

```xml
<resources>
    <string name="rate_dialog_title">Rate this app</string>
    <string name="rate_dialog_message">If you enjoy playing this app, would you mind taking a moment to rate it? It won\'t take more than a minute. Thanks for your support!</string>
    <string name="rate_dialog_ok">Rate It Now</string>
    <string name="rate_dialog_cancel">Remind Me Later</string>
    <string name="rate_dialog_no">No, Thanks</string>
</resources>
```
<<<<<<< HEAD
=======
<<<<<<< HEAD
<<<<<<< HEAD
And if you want to decide whether neutral button is appeared, please call `AppRate.setShowNeutralButton(boolean)`.

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    // method chain
    AppRate.setInstallDays(0)
           .setShowNeutralButton(false) // default true
=======
>>>>>>> 7adac95... v0.0.3 release.
And if you want to decide whether neutral button is appeared, please call `AppRate.setIsShowNeutralButton(boolean)`.
=======
And if you want to decide whether neutral button is appeared, please call `AppRate.setShowNeutralButton(boolean)`.
>>>>>>> 28d7a9d... v0.0.3 release.

```java
@Override
protected void onStart() {
    super.onStart();
    // method chain
    AppRate.setInstallDays(0)
<<<<<<< HEAD
           .setIsShowNeutralButton(false) // default true
<<<<<<< HEAD
=======
>>>>>>> 3876ba2... v0.0.2
=======
           .setShowNeutralButton(false) // default true
>>>>>>> 28d7a9d... v0.0.3 release.
>>>>>>> 7adac95... v0.0.3 release.
           .monitor(this);
}
```

## Localization

Android-Rate currently supports the following languages:

 * English
 * Japanese
 * French
 * Spanish
 * Chinese
 * Korean

## Requirements

Supports Android 2.2 or greater.

## Build

```sh
$ ./gradlew uploadArchives
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## ToDo

- Add unit test.
<<<<<<< HEAD
- Add travis badge.
<<<<<<< HEAD
=======
>>>>>>> 3876ba2... v0.0.2
=======
- Add travis or wercker badge.
>>>>>>> 28d7a9d... v0.0.3 release.
>>>>>>> 7adac95... v0.0.3 release.
- Support event counts condition.
- Support uses per week condition.

## ChangeLog

<<<<<<< HEAD
2014/02/12 v0.0.2 release.

## License

This software is licensed under [MIT Licence](http://opensource.org/licenses/MIT).
=======
<<<<<<< HEAD
<<<<<<< HEAD
- 2014/02/12 v0.0.2 release.
- 2014/02/13 v0.0.3 release.
=======
2014/02/12 v0.0.2 release.
>>>>>>> 3876ba2... v0.0.2
=======
- 2014/02/12 v0.0.2 release.
- 2014/02/13 v0.0.3 release.
>>>>>>> 28d7a9d... v0.0.3 release.

## License

```
The MIT License (MIT)

Copyright (c) 2014 Shintaro Katafuchi

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
<<<<<<< HEAD
```
=======
```
>>>>>>> 28d7a9d... v0.0.3 release.
>>>>>>> 7adac95... v0.0.3 release.