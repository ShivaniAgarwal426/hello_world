# Android-Java: Drawable Resource Overview




A drawable resource is a concept for a graphic that is to be displayed on the screen and which can be retrieved by applying to another XML resource with attributes such as android:drawable and android:icon or with APIs such as `getDrawable(int)`. 
- **Drawable resource file can be refered as:**
   > _In Java:_ R.drawable.filename
   >
   > _In XML:_ @drawable/filename

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
- **file location:**
   > res/drawable/filename.png (.png, .jpg, or .gif) 
- **syntax:**
   > With an image saved at res/drawable/myimage.png, this layout XML applies the image to a View as:
   ```bash
   <ImageView
       android:layout_height="wrap_content"
       android:layout_width="wrap_content"
       android:src="@drawable/myimage" />
   ```
- **Example:**



## 2. Create an XML resource file that defines the drawable properties:

### 2.1. Create Custom Resource files. 
- **file location:**
   > res/drawable/filename.xml 
> _STEPS_ <br>
1. 
2.
3.


<br><br>

#### 2.1.1 Layer List 
> A Layer list is a drawable object that manages an array of other drawables. These are drawn in array order, so the element of the larger index will  be drawn first i.e. the last drawable in the list is drawn on top.
- Elements `<layer-list>`  must be the root element. Contains one or more `<item>` elements.
- Each drawable is represented by an `<item>` element inside a single `<layer-list>` element.
- **syntax:**
  ```bash
   <?xml version="1.0" encoding="utf-8"?>
   <layer-list
       xmlns:android="http://schemas.android.com/apk/res/android" >
      <item
        android:drawable="@drawable/drawable_resource"
        android:id="@+id/resource_name"
        android:top="dimension"
        android:right="dimension"
        android:bottom="dimension"
        android:left="dimension" />
   </layer-list>
  ```
- **Example:**
   
   
----------------------------------------------------------------------------------------------------------------------------------------
` #NOTE ` 
 - All drawable items are scaled to fit the size of the containing View, by default. Thus, placing images in a layer list at different positions might increase the size of the View and some images scale as appropriate. 
   > Example,  scales fit its container View using item element:
   ```bash
   <item android:drawable="@drawable/image" />
   ```

- To avoid scaling items in the list, use a `<bitmap>` element inside the `<item>` element to specify the drawable and define the gravity.
  > For example:
   ```bash
   <item>
      <bitmap android:src="@drawable/image"
          android:gravity="center" />
   </item>
   ```
----------------------------------------------------------------------------------------------------------------------------------------
   
   
   
#### 2.1.2 State List (Selector)
> A StateList is a drawable object defined in XML that uses several different images to represent the bitmap graphic, depending on the state of the drawable. 
   - For example, a Button widget can exist in one of several different states (pressed, focused, or neither) and, using a state list drawable, you can provide a different background for each state.
   - Another example is, to use a different image when a button is pressed.

   >  Elements `<selector>` must be the root element. Contains one or more `<item>` elements. Each graphic is represented by an `<item>` element inside a single `<selector>` element. `<item>` uses various attributes to describe the state to used as the graphic for the drawable.

   > During each state change, the state list is traversed top to bottom and the first item that matches the current state is used—the selection is not based on the "best match," but simply the first item that meets the minimum criteria of the state.

- **syntax:**
  ```bash
   <?xml version="1.0" encoding="utf-8"?>
   <selector xmlns:android="http://schemas.android.com/apk/res/android"
       android:constantSize=["true" | "false"]
       android:dither=["true" | "false"]
       android:variablePadding=["true" | "false"] >
       <item
           android:drawable="@[package:]drawable/drawable_resource"
           android:state_pressed=["true" | "false"]
           android:state_focused=["true" | "false"]
           android:state_hovered=["true" | "false"]
           android:state_selected=["true" | "false"]
           android:state_checkable=["true" | "false"]
           android:state_checked=["true" | "false"]
           android:state_enabled=["true" | "false"]
           android:state_activated=["true" | "false"]
           android:state_window_focused=["true" | "false"] />
   </selector>
  ```
- **Example:**
 
   
      
#### 2.1.3 Level List
> A Level list is a drawable that manages a number of alternate Drawables, each assigned a maximum numerical value. Setting the level value of the drawable with `setLevel()` loads the drawable resource in the level list that has a `android:maxLevel` value greater than or equal to the value passed to the method. 

> Elements `<level-list>` is always the root element. Contains one or more `<item>` elements.

- **syntax:**
  ```bash
   <?xml version="1.0" encoding="utf-8"?>
   <level-list
       xmlns:android="http://schemas.android.com/apk/res/android" >
       <item
           android:drawable="@drawable/drawable_resource"
           android:maxLevel="integer"
           android:minLevel="integer" />
   </level-list>
  ```
- **Example:**

#### 2.1.4 Shape Drawable
> An XML file that defines a geometric shape, including colors and gradients. Creates a GradientDrawable by customising.

> Here, elements `<shape>` drawable is always the root element.

- **syntax:**
  ```bash
   <?xml version="1.0" encoding="utf-8"?>
   <shape
       xmlns:android="http://schemas.android.com/apk/res/android"
       android:shape=["rectangle" | "oval" | "line" | "ring"] >
       <corners
           android:radius="integer"
           android:topLeftRadius="integer"
           android:topRightRadius="integer"
           android:bottomLeftRadius="integer"
           android:bottomRightRadius="integer" />
       <gradient
           android:angle="integer"
           android:centerX="float"
           android:centerY="float"
           android:centerColor="integer"
           android:endColor="color"
           android:gradientRadius="integer"
           android:startColor="color"
           android:type=["linear" | "radial" | "sweep"]
           android:useLevel=["true" | "false"] />
       <padding
           android:left="integer"
           android:top="integer"
           android:right="integer"
           android:bottom="integer" />
       <size
           android:width="integer"
           android:height="integer" />
       <solid
           android:color="color" />
       <stroke
           android:width="integer"
           android:color="color"
           android:dashWidth="integer"
           android:dashGap="integer" />
   </shape>
  ```
- **Example:**

#### 2.1.5 Scale Drawable
> An XML file that defines a drawable which can  changes the size of another Drawable based on its current level value. 

> Here, elements `<scale>` is the root element.

- **syntax:**
  ```bash
   <?xml version="1.0" encoding="utf-8"?>
   <scale
       xmlns:android="http://schemas.android.com/apk/res/android"
       android:drawable="@drawable/drawable_resource"
       android:scaleGravity=["top" | "bottom" | "left" | "right" | "center_vertical" |
                             "fill_vertical" | "center_horizontal" | "fill_horizontal" |
                             "center" | "fill" | "clip_vertical" | "clip_horizontal"]
       android:scaleHeight="percentage"
       android:scaleWidth="percentage" />
  ```
- **Example:**


#### 2.1.6 Clip Drawable
> An XML file that defines a drawable that clips another Drawable based on this Drawable's current level value. 

> You can control how much the child drawable gets clipped in width and height based on the level, as well as a gravity. 

> Most often used to implement things like progress bars.

- **syntax:**
  ```bash
   <?xml version="1.0" encoding="utf-8"?>
   <clip
       xmlns:android="http://schemas.android.com/apk/res/android"
       android:drawable="@drawable/drawable_resource"
       android:clipOrientation=["horizontal" | "vertical"]
       android:gravity=["top" | "bottom" | "left" | "right" | "center_vertical" |
                        "fill_vertical" | "center_horizontal" | "fill_horizontal" |
                        "center" | "fill" | "clip_vertical" | "clip_horizontal"] />
  ```
- **Example:**


#### 2.1.7 Transition/ Animated Drawable
> A TransitionDrawable is a drawable object that can cross-fade between the two drawable resources.

> Each drawable is represented by an `<item>` element inside a single `<transition>` element. 
Only  two items are supported. 

> To transition forward, call `startTransition()`. 
> To transition backward, call `reverseTransition()`.

- **syntax:**
  ```bash
   <?xml version="1.0" encoding="utf-8"?>
   <transition
   xmlns:android="http://schemas.android.com/apk/res/android" >
       <item
           android:drawable="@[package:]drawable/drawable_resource"
           android:id="@[+][package:]id/resource_name"
           android:top="dimension"
           android:right="dimension"
           android:bottom="dimension"
           android:left="dimension" />
   </transition>
  ```
- **Example:**



### 2.2. Create Image Assets.
> The drawable folder contains the different types of images used for the development of the application. So we need images in android applications to provide more user-friendly behavior & functionality. 

> Here, we are going to discuss how to add an image to the drawable folder with Image Asset method.

> _Steps_
  1. <br>
  2. <br>
  3. <br>


### 2.3. Create Vector Assets.
> Vector Assets in Android Studio helps to add material icons and import Scalable Vector Graphics files into your project as vector drawable resources.

> **Image scalability is the major advantage of using the vector drawable.** 
> The same file can be resized for different screen sizes without loss of image quality which results in smaller APK files and less developer maintenance. We can also use vector images for animation. 

> _Steps_
  1. <br>
  2. <br>
  3. <br>
  
