MMFontLib
=========

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.mmaug.mmfont/library/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.mmaug.mmfont/library/badge.svg)

By - [MMAUG ](https://github.com/MMAUG)

[Click Here For Lib](https://github.com/MMAUG/MMFontLib)

Myanmar font embedded TextViews. Currently, it supports
- Myanmar 3
- Masterpiece
- MyMyanmar
- Yunghkio
- Zawgyi One
- NotoSans Myanmar Regular
- NotoSans Myanmar Bold

Sample
------
Checkout [sample app](https://github.com/MMAUG/MMFontLib/blob/master/sample).

<img src="https://cloud.githubusercontent.com/assets/275120/3637479/248483ea-100c-11e4-9a1a-0cb9412a3d16.png" alt="Screenshot 1" width="300px" height="500px"/>
<img src="https://cloud.githubusercontent.com/assets/275120/3637480/288b5c02-100c-11e4-881e-145234009cec.png" alt="Screenshot 2" width="300px" height="500px"/>


Quick Start
-----------
MMFont Lib is pushed to Maven Central as an AAR, so you just need to add the following dependency to your build.gradle.

```Groovy
dependencies {
    compile 'org.mmaug.mmfont:library:1.3.0'
}
```

Replace your `TextView` with embedded view.


#### Using the custom TextViews in the XML

```xml
<!-- Myanmar3 Font -->
<org.mmaug.mmfont.MM3
    android:id="@+id/tv_mm3"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="25sp" />

<!-- Masterpiece Uni Round Font -->
<org.mmaug.mmfont.MSP
    android:id="@+id/tv_msp"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="25sp" />

<!-- MyMyanmar Universal Font -->
<org.mmaug.mmfont.MyMM
    android:id="@+id/tv_mymm"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="25sp" />

<!-- Noto Sans Myanmar Regular Font -->
<org.mmaug.mmfont.Noto
    android:id="@+id/tv_noto"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="25sp" />

<!-- Noto Sans Myanmar Bold Font -->
<org.mmaug.mmfont.NotoBold
    android:id="@+id/tv_noto_bold"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="25sp" />

<!-- Yunghkio Font -->
<org.mmaug.mmfont.YGK
    android:id="@+id/tv_ygk"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="25sp" />

<!-- Zawgyi-One Font -->
<org.mmaug.mmfont.ZG
    android:id="@+id/tv_zg"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="25sp" />
```

#### Setting Custom Typeface to a TextView
```java
    // TextView you want to set typeface
    TextView uniTextView = (TextView) findViewById(R.id.custom_uni_text);
    // Create a FontUtils instance. The Argument is a Context
    FontUtils fontUtils = new FontUtils(this);
    // Set Text to your TextView either here or in XML
    uniTextView.setText("သီဟိုဠ်မှ ဉာဏ်ကြီးရှင်သည် အာယုဝဍ္ဎနဆေးညွှန်းစာကို ဇလွန်ဈေးဘေးဗာဒံပင်ထက်
                             အဓိဋ္ဌာန်လျက် ဂဃနဏဖတ်ခဲ့သည်");
                             
    // Set Typeface to your TextView by choosing the font name
    fontUtils.setTypeFace(Fonts.ZG, zgTextView);
    
    // You can set Typeface to several TextViews    
    fontUtils.setTypeFace(Fonts.ZG, TextView1, TextView2, TextView3);
```

You can see the list of available fonts [here](https://github.com/MMAUG/MMFontLib/blob/master/library%2Fsrc%2Fmain%2Fjava%2Forg%2Fmmaug%2Fmmfont%2Futils%2FFonts.java).

Contributing
------------

 1. Fork it
 2. Create your feature branch (`git checkout -b my-new-feature`)
 3. Commit your changes (`git commit -am 'Added some feature'`)
 4. Push to the branch (`git push origin my-new-feature`)
 5. Create new Pull Request

License
--------

    Copyright 2014 Myanmar Android User Group(MMAUG)

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


Fonts are respectively copyrighted by font owners.
