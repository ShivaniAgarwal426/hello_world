# Android-Java: Drawable Resource Overview




A drawable resource is a concept for a graphic that is to be displayed on the screen and which can be retrieved by applying to another XML resource with attributes such as android:drawable and android:icon or with APIs such as getDrawable(int). 

There are several different types of drawables:

1. Inflate/paste an image resource (bitmap Image or file) in your project.

2. Create an XML resource file that defines the drawable properties.

   2.1. Create Custom Resource files.

       2.1.1. shape.

       2.1.2. selector.

       2.1.3. layer-list.

   2.2. Create Image Assets.

   2.3. Create Vector Assets.




## 1. Inflate Image Resource file (Bitmap files):
- Android supports bitmap files in three formats: .png (preferred), .jpg (acceptable), .gif (discouraged).
- This is why, a bitmap file must be in .png, .jpg, or .gif extension.
- You can reference a bitmap file directly, using the filename as the resource ID, or create an alias resource ID in XML.
- Android creates a Drawable resource for any of these files when you save them in the res/drawable/ directory.
<br>
- **file location:**
res/drawable/filename.png (.png, .jpg, or .gif)
- **resource reference:**
**In Java:* R.drawable.filename
**In XML:* @drawable/filename
- **example:**
With an image saved at res/drawable/myimage.png, this layout XML applies the image to a View as:

```bash
<ImageView
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:src="@drawable/myimage" />
```


## 2. Create an XML resource file that defines the drawable properties:

### 2.1. Create Custom Resource files. 

_STEPS_ <br>
1.
2.
3.


<br><br>

#### 2.1.1 Layer List 
#### 2.1.2 State List (Selector)
#### 2.1.3 Level List
#### 2.1.4 Shape Drawable
#### 2.1.5 Scale Drawable
#### 2.1.6 Clip Drawable
#### 2.1.7 Animated Drawable

### 2.2. Create Image Assets.
### 2.3. Create Vector Assets.

  
