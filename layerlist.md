**Layer list**

create resource xml file-

![image](https://user-images.githubusercontent.com/70523057/134816211-bb12e446-553e-48e3-832f-5d820054ff4e.png)


Select the root element of xml and name the file-

![image](https://user-images.githubusercontent.com/70523057/134816287-9fc0490e-2a8b-473b-94ef-a64b43b08b78.png)
Added 3 drawable images of flowers in png format


layers.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <bitmap android:src="@drawable/flower1"
            android:gravity="center" />
    </item>
    <item android:top="100dp" android:left="100dp">
        <bitmap android:src="@drawable/flower2"
            android:gravity="center" />
    </item>
    <item android:top="200dp" android:left="200dp">
        <bitmap android:src="@drawable/flower3"
            android:gravity="center" />
    </item>
</layer-list>
```

activity_maim.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
   
       <ImageView
           android:id="@+id/image"
           android:layout_width="match_parent"
           android:layout_height="match_parent"
           android:src="@drawable/layers" />
  
</RelativeLayout>
```
Output in Screen-
![image](https://user-images.githubusercontent.com/70523057/134816702-ec6a38fd-ea17-4003-9cc6-190d072454a3.png)



--------------------------------------------------------------------------------------------------------------------------------------------
**SELECTOR**
![image](https://user-images.githubusercontent.com/70523057/134817156-170bf398-fb8e-47d2-88fa-d9c908b2173e.png)

```bash
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">

    <corners android:radius="4dp"/>
    <stroke android:color="@color/teal_700" android:width="2dp"/>
    <solid android:color="@color/purple_200"/>
</shape>
```

activity_maim.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
   
   <TextView
       android:layout_width="wrap_content"
       android:layout_height="wrap_content"
       android:layout_centerInParent="true"
       android:padding="10dp"
      android:text="@android:string/selectAll"
      android:background="@drawable/shape1"/>
      
</RelativeLayout>
```

output-

![image](https://user-images.githubusercontent.com/70523057/134817141-3e6bfb60-2561-4f3f-9ea4-1695fa3bb440.png)

