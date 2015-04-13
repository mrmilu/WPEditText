#WPEditText
===

Material design inspired EditText

###USAGE:

1. Gradle

	````
	dependencies {
    	compile org.webpartners.wpedittext:WPEditText:1.0.0
    }
    ````
    
2. Add the new xmls to your layout parent widget

	````
	xmlns:wp="http://schemas.android.com/apk/res-auto"
	````


3. Add WPEdittext to your layout and configure it

	````
	<org.werpartners.wpedittext.WPEditText
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

