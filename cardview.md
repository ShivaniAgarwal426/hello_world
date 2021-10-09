# Android-Development-Java 2.1.7 CardView in Android

<br><br>

## CardView Widget
CardView is a new widget in Android that can be used to display any sort of data by providing a rounded corner layout along with an elevation.    <br>
CardView is the view that can display views on top of other.     <br>
The main usage of CardView is that it helps to give a amazing outlook to the UI design.     <br>
This widget can be easily seen in many different Android Apps.     <br>
CardView can be used for creating items in **listview** or inside **Recycler View**.     <br>
The best part about CardView is that it extends Framelayout and it can be displayed on all platforms of Android.     <br>
Cards provide an easy way to contain a group of views while providing a consistent style for the container.

> Now we will see the simple example of CardView implementation. 

<br><br>

## Add dependency for CardView
Before we get started, you have to add the CardView dependency in build.gradle file and sync the project.
```bash
dependencies {
    implementation "androidx.cardview:cardview:1.0.0"
}
```
[Check the updated version of CardView](https://developer.android.com/guide/topics/ui/layout/cardview)

<br><br>

## Create Cards with different attributes
In order to use the `CardView` you need to add it to your layout file. Use it as a view group to contain other views. 

Use these properties to customize the appearance of the `CardView` widget:
- Set corner radius - use the `card_view:cardCornerRadius` attribute.
- Set the elevation by customization - use the `card_view:cardElevation` attribute.
- Set corner radius - use the `CardView.setRadius` method.
- Set background color - use the `card_view:cardBackgroundColor` attribute.

<br><br>

## Implementation of CardView
- After adding dependencies, now we will will create a simple CardView.    <br>
  Navigate to **app>res>layout>activity_main.xml** then create new CardView widget to it. 
  ```bash
  
  ```
  
- Run your app on your Emulator or Android device
   <div align="center"><table><tr><td>
      <img src="https://user-images.githubusercontent.com/70523057/135032021-dfc62b6e-4cdd-470f-8c45-edb972a5f442.jpg" width="240" >
   </td></tr></table></div> 

<br><br>

## Applications
- Use in the list layout item of RecyclerView
- Use inside the ViewPager
- Use in layout without creating resource drawable file. 


