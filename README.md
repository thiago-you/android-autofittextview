# AutoFitTextView

[Updated SDK 14~33] A TextView that automatically resizes text to fit perfectly within its bounds.

![Example Image](/website/static/autofittextview.gif?raw=true)

## Dependency

Add this in your root `build.gradle` file (**not** your module `build.gradle` file):

```gradle
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```

Then, add the library to your module `build.gradle`

```gradle
dependencies {
    implementation 'com.github.thiago-you:autofittextview:1.0.0'
}
```

## Usage
Enable any View extending TextView in code:

```java
AutofitHelper.create(textView);
```

Enable any View extending TextView in XML:

```xml
<you.thiago.autofittextview.AutofitTextView
    android:layout_width="match_parent"
    android:layout_height="wrap_content">
    
    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:singleLine="true" />
    
</you.thiago.autofittextview.AutofitTextView>
```

Use the built in Widget in code or XML:

```xml
<RootElement
    xmlns:autofit="http://schemas.android.com/apk/res-auto"
    ...
```   

```xml
<you.thiago.autofittextview.AutofitTextView
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:singleLine="true"
    android:maxLines="2"
    android:textSize="40sp"
    autofit:minTextSize="16sp" />
```


## License

    Copyright 2014 Grantland Chew

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
