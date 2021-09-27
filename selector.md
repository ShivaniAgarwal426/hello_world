![image](https://user-images.githubusercontent.com/70523057/134852542-6d4579ab-61a0-4a17-a72b-df3647c52311.png)
<br>
statelist.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<selector xmlns:android="http://schemas.android.com/apk/res/android">
        <item android:drawable="@color/teal_700" android:state_selected="true"></item>
        <item android:drawable="@color/purple_700" android:state_pressed="true"></item>
        <item android:drawable="@color/black"></item>
</selector>
```
<br>
activity_main.xml

```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

<androidx.appcompat.widget.AppCompatButton
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
   android:layout_margin="20dp"
   android:text="@android:string/ok"
   android:textColor="@color/white"
   android:background="@drawable/statelist"
    android:layout_centerInParent="true"/>

</RelativeLayout>
```
<br><br>
output-

screenrecording in phone.
















-----------------------------------------------------------------------------------------------------------------------------------





**LEVEL LIST**

![image](https://user-images.githubusercontent.com/70523057/134855267-fd0281ba-39ce-4699-a5f9-434b5fed5ea3.png)

