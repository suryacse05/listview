
# Ex.No:7 Develop an android application to display the country name with image using list view in android studio.


## AIM:

To create and develop the application to display the place name with image using list view in android studio

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “listview″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the list of item.
Developed by:B.mothishkumar
Registeration Number :212221040027
*/
```
Activity_main.xml:
```
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent" tools:context=".MainActivity">

<ListView
    android:id="@+id/simpleListview"
    android:layout_width="409dp"
    android:layout_height="729dp"
    tools:layout_editor_absoluteX="1dp"
    tools:layout_editor_absoluteY="1dp" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
Activity_listview.xml:
```
<ImageView
    android:id="@+id/imageView2"
    android:layout_width="173dp"
    android:layout_height="95dp"
    android:layout_weight="1"
    tools:srcCompat="@tools:sample/avatars" />

<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_weight="1"
    android:text="TextView" />
```
CustomAdapter.java:
```
package com.example.imagelistview;

import android.content.Context; import android.view.LayoutInflater; import android.view.View; import android.view.ViewGroup; import android.widget.BaseAdapter; import android.widget.ImageView; import android.widget.TextView;

public class CustomAdapter extends BaseAdapter { Context context; String countryList[]; int flags[]; LayoutInflater inflter;

public CustomAdapter(Context applicationContext, String[] countryList, int[] flags) {
    this.context = context;
    this.countryList = countryList;
    this.flags = flags;
    inflter = (LayoutInflater.from(applicationContext));
}

@Override
public int getCount() {
    return countryList.length;
}

@Override
public Object getItem(int i) {
    return null;
}

@Override
public long getItemId(int i) {
    return 0;
}

@Override
public View getView(int i, View view, ViewGroup viewGroup) {
    view = inflter.inflate(R.layout.activity_listview, null);
    TextView country = (TextView) view.findViewById(R.id.textView);
    ImageView icon = (ImageView) view.findViewById(R.id.imageView2);
    country.setText(countryList[i]);
    icon.setImageResource(flags[i]);
    return view;
}
}
```
MainActivity.java:
```
package com.example.imagelistview;

import android.content.Context; import android.view.LayoutInflater; import android.view.View; import android.view.ViewGroup; import android.widget.BaseAdapter; import android.widget.ImageView; import android.widget.TextView;

public class CustomAdapter extends BaseAdapter { Context context; String countryList[]; int flags[]; LayoutInflater inflter;

public CustomAdapter(Context applicationContext, String[] countryList, int[] flags) {
    this.context = context;
    this.countryList = countryList;
    this.flags = flags;
    inflter = (LayoutInflater.from(applicationContext));
}

@Override
public int getCount() {
    return countryList.length;
}

@Override
public Object getItem(int i) {
    return null;
}

@Override
public long getItemId(int i) {
    return 0;
}

@Override
public View getView(int i, View view, ViewGroup viewGroup) {
    view = inflter.inflate(R.layout.activity_listview, null);
    TextView country = (TextView) view.findViewById(R.id.textView);
    ImageView icon = (ImageView) view.findViewById(R.id.imageView2);
    country.setText(countryList[i]);
    icon.setImageResource(flags[i]);
    return view;
}
}

```
## OUTPUT
![image](https://github.com/21005290/listview/assets/112933246/3a605b37-0b83-483b-9061-bd96d9d7c5e7)




## RESULT
Thus a Simple Android Application to create and develop the application to display the country name with image using list view in android studio is developed and executed successfully.
