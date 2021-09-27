
## Example

Bitmap image:

**copy from system-**

![image](https://user-images.githubusercontent.com/70523057/134815113-4d258e41-5bf1-4c4f-9f1f-89f110dcd049.png)

**paste-**
![image](https://user-images.githubusercontent.com/70523057/134814909-9a76c86d-8e50-4260-b14d-c1ce23a651ef.png)
**add to drawable folder-**
![image](https://user-images.githubusercontent.com/70523057/134815138-e2a5eb98-f4d1-4544-a20d-8de428b9c64d.png)
**give any name to the image-**
here it is android_image.png
![image](https://user-images.githubusercontent.com/70523057/134815201-22d49228-daf2-4663-a84d-d5a95a21fb70.png)
**Inside the xml activity page add ImageView widget-**

```bash
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

   <ImageView
       android:id="@+id/image"
       android:layout_width="150dp"
       android:layout_height="150dp"
       android:src="@drawable/android_image"/>

</LinearLayout>
```
here, src is an attribute used to set a source file or you can say image in your imageview

**Drawable Image on Android Screen-**

![image](https://user-images.githubusercontent.com/70523057/134815393-abddfb19-6d6b-4a4e-8856-ca1f046601e6.png)

