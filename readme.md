# Sidebar-Drawer-Nav

Sidebar-Drawer-Nav is a library build on [Android DrawerLayout Support library](https://https://developer.android.com/training/implementing-navigation/nav-drawer) as Parent Class, to provide animations, transitions, and custom behavior.

If you are using native navigation drawer component you can easily switch to use Sidebar-Drawer_Nav library by just changing the layout's parent Tags and call the necessary method for animations/effects.

[![](https://jitpack.io/v/aasif1297/sidebardrawernav.svg)](https://jitpack.io/#aasif1297/sidebardrawernav)


#

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/K3K41KCLB)

![](images/demo.gif)

# Add in your project
Add it in your root build.gradle at the end of repositories:


## Gradle
Step 1. Add the JitPack repository to your build file

```bash
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
Step 2. Add the dependency

```bash
dependencies {
    implementation 'com.github.aasif1297:sidebardrawernav:1.0'
}
```
## Maven
Step 1. Add the JitPack repository to your build file

```bash
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
```
Step 2. Add the dependency
```bash
<dependency>
    <groupId>com.github.aasif1297</groupId>
    <artifactId>sidebardrawernav</artifactId>
    <version>1.0</version>
</dependency>
```

## Usage

### Step 1 - Create Layout

```xml
<?xml version="1.0" encoding="utf-8"?>
<com.cicadalabs.sidebardrawernav.SidebarDrawerLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/drawer_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/yellow"
    android:fitsSystemWindows="true"
    tools:openDrawer="start">

    <include
        layout="@layout/app_bar_main"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />


    <com.google.android.material.navigation.NavigationView
        android:id="@+id/nav_view"
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:layout_gravity="start"
        android:background="@android:color/transparent"
        android:fitsSystemWindows="false"
        app:headerLayout="@layout/nav_header_main"
        app:itemIconTint="@android:color/white"
        app:itemTextColor="@android:color/white"
        app:menu="@menu/activity_main_drawer">

        <include layout="@layout/nav_content"/>

    </com.google.android.material.navigation.NavigationView>
    
</com.cicadalabs.sidebardrawernav.SidebarDrawerLayout>
```

### Step 2 - Initialize component

```java
val drawerLayout: SidebarDrawerLayout = findViewById(R.id.drawer_layout)

```

### Step 3 - Use methods
```java
drawerLayout.useCustomBehavior(Gravity.START)
drawerLayout.setViewScale(Gravity.START, 0.9f)
drawerLayout.setRadius(Gravity.START, 35.0F)
drawerLayout.setElevation(Gravity.START, 20.0F)
drawerLayout.setBackgroundImage(resources.getDrawable(R.drawable.drawer_bg))
```

### More customization
```xml
drawer.setViewScale(Gravity.START, 0.9f); //set height scale for main view (0f to 1f)
drawer.setViewElevation(Gravity.START, 20); //set main view elevation when drawer open (dimension)
drawer.setViewScrimColor(Gravity.START, Color.TRANSPARENT); //set drawer overlay color (color)
drawer.setDrawerElevation(Gravity.START, 20); //set drawer elevation (dimension)
drawer.setContrastThreshold(3); //set maximum of contrast ratio between white text and background color.
drawer.setRadius(Gravity.START, 25); //set end container's corner radius (dimension)
```
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## Contact
For any inquiries, please send an email to [aasif1297@gmail.com](aasif1297@gmail.com)


