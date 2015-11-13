#WPEditText [ ![Download](https://api.bintray.com/packages/firezenk/maven/WPEditText/images/download.svg) ](https://bintray.com/firezenk/maven/WPEditText/_latestVersion)

Material design inspired EditText with icon support and validation included

![wpedittext_demo](https://cloud.githubusercontent.com/assets/1595403/7198136/6cdac6ba-e4e9-11e4-8d70-45451cb45159.png)

Validation types:

````
TYPE_ALPHA
TYPE_ALPHANUMERIC
TYPE_EMAIL
TYPE_PASSWORD
````

Also supports minimum lenght restrinction for passwords

###USAGE:

1. Gradle

	````
	repositories {
		...
	        maven { url 'https://github.com/FireZenk/maven-repo/raw/master/'}
	}
	dependencies {
	    	...
	        compile 'org.webpartners:wpedittext:1.0.2.3@aar'
	}
	````
    
2. Add the new xmls to your layout parent widget

	````
	xmlns:wp="http://schemas.android.com/apk/res-auto"
	````


3. Add WPEdittext to your layout and configure it

	````
	<org.webpartners.wpedittext.WPEditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        wp:hint="@string/test_wpedittext_hint"
        wp:type="alpha"
        wp:min_length="8"
        wp:valid_message="@string/validation_valid_field"
        wp:invalid_message="@string/validation_invalid_field"
        wp:empty_message="@string/validation_empty_field"
        wp:text_color="@android:color/black"
        wp:hint_color="@android:color/darker_gray"
        wp:header_icon="@android:drawable/ic_dialog_info"/>
	````

4. Also you can configure WPEdittext by code

	````
	setupEditText(int hint, int type, int minLength)
	
	textColors(int textColor, int hintColor)
	
	validationText(int valid, int invalid, int empty)
	
	validationText(String valid, String invalid, String empty)
	
	icon(int drawable)
	
	underLine(int color)
	
	setText(String text)
	````

---


To get EditText's text


	String getText()
	
	
To get validation result
	
	boolean isOk()

---

###LICENSE

````
The MIT License (MIT)

Copyright (c) 2015 WebPartners

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
````
