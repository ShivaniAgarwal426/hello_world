#animate

create
![image](https://user-images.githubusercontent.com/70523057/134929947-9cd81aa0-42dd-46ba-874c-34dfc7accdf5.png)
now create different vector assets to show the animation inside the res/drawable/ folder

animations.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<animation-list xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:drawable="@drawable/ic_baseline_looks_4_24" android:duration="100" />
    <item android:drawable="@drawable/ic_baseline_looks_3_24" android:duration="100" />
    <item android:drawable="@drawable/ic_baseline_looks_two_24" android:duration="100" />
    <item android:drawable="@drawable/ic_baseline_looks_one_24" android:duration="100" />
</animation-list>
```

main
```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

           <ImageView
               android:id="@+id/changing_numbers"
               android:layout_width="200dp"
               android:layout_height="200dp"
               android:src="@drawable/animations"
               android:layout_centerInParent="true"/>

</RelativeLayout>
```

java
> Here, we have load the ImageView which host the animation and set its background to our AnimationDrawable XML resource.
        
```bash
        ImageView img = (ImageView)findViewById(R.id.changing_numbers);
        img.setBackgroundResource(R.drawable.animations);
        // Get the background, which has been compiled to an AnimationDrawable object.
        AnimationDrawable frameAnimation = (AnimationDrawable) img.getBackground();
        // Start the animation.
        frameAnimation.start();
```










------------------------
#transit
create xml file
![image](https://user-images.githubusercontent.com/70523057/134930432-c9f24a72-c5d2-4ddb-b614-6f54c7bf8b41.png)
transitions.xml
```bash
<?xml version="1.0" encoding="utf-8"?>
<transition xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:drawable="@drawable/flower1"
        android:top="20dp"
        android:right="300dp"
        android:bottom="300dp"
        android:left="20dp" />
    <item android:drawable="@drawable/flower2"
        android:top="200dp"
        android:right="50dp"
        android:bottom="50dp"
        android:left="200dp" />
</transition>
```



main
```bash
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

           <ImageView
               android:id="@+id/transition"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:src="@drawable/transitions"
               android:layout_centerInParent="true"/>

</RelativeLayout>
```
java
```bash
ImageView transit = (ImageView) findViewById(R.id.transition);
        Drawable drawable = transit.getDrawable();
        if (drawable instanceof TransitionDrawable) {
            ((TransitionDrawable) drawable).startTransition(1000);
         } 
```
