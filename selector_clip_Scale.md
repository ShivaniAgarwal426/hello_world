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


-------------
#clip
create xml file
![image](https://user-images.githubusercontent.com/70523057/134941927-60cd1b0e-10bf-46b6-9c64-0061346ea6a3.png)

clip.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<clip xmlns:android="http://schemas.android.com/apk/res/android"
    android:drawable="@drawable/flower2"
    android:clipOrientation="vertical"
    android:gravity="bottom"
    />
```
activity_main.xml

```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:background="@color/black">

           <ImageView
               android:id="@+id/clipping_image"
               android:layout_width="200dp"
               android:layout_height="200dp"
               android:src="@drawable/clip"
               android:layout_centerInParent="true"/>

</RelativeLayout>
```
 java
 ```bash
        ImageView imageview = (ImageView) findViewById(R.id.clipping_image);
        Drawable drawable = imageview.getBackground();
        if (drawable instanceof ClipDrawable) {
            ((ClipDrawable)drawable).setLevel(drawable.getLevel() + 5000);
        }
```

output

![image](https://user-images.githubusercontent.com/70523057/134943050-ebb6a6e1-88c2-404c-8378-06981b6cb9ab.png)


-----------
#scale

create xml file
![image](https://user-images.githubusercontent.com/70523057/134942442-d8fcb786-e826-4f03-b3c4-58cbf9f9261d.png)

scale.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<scale xmlns:android="http://schemas.android.com/apk/res/android"
    android:drawable="@drawable/flower3"
    android:scaleGravity="center"
    android:scaleHeight="50%"
    android:scaleWidth="50%"
    />
```
activity_main.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

           <ImageView
               android:id="@+id/scaling_image"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:src="@drawable/scale"
               android:layout_centerInParent="true"/>

</RelativeLayout>
```
 output

------------------------------------------------------------------------------------------------------------------------------




