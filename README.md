# Ex.No:4 Design an android application Send SMS using Intent.

## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio App

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.
Step 2: Then type the Application name as “ex04″ and click Next. 
Step 3: Then select the Empty Activity and click Next. Finally click Finish.
Step 4: Design layout in activity_main.xml.
Step 5: Send SMS and Display details give in MainActivity file.
Step 6: Launch an emulator and run the application.

# PROGRAM:
## Program to create and design an android application Send SMS using Intent.
## Developed by: P.Sanjay
## Registeration Number : 212220230042
### MainActivity.java
```
package com.example.expno4;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button mButton= (Button) findViewById(R.id.send_sms);
        mButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(Intent.ACTION_VIEW,
                        Uri.fromParts("sms","6303583708",null));
                intent.putExtra("sms_body","Welcome to Android Studio");
                startActivity(intent);
            }
        });
    }
}
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="16dp"
    android:paddingRight="16dp"
    android:paddingBottom="16dp"
    android:paddingTop="16dp"
    tools:context=".MainActivity">
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/send_sms"
        android:text="click_here_to_send_sms"/>
</RelativeLayout>
```

## OUTPUT:

![4](https://user-images.githubusercontent.com/75235426/168459881-4138fb9a-e55b-47bd-91f9-d12944aeb1b2.jpg)
![5](https://user-images.githubusercontent.com/75235426/168459883-eb30faa7-3807-43b3-bdba-40a6ccb67b43.jpg)
![6](https://user-images.githubusercontent.com/75235426/168459888-5ba59847-0146-4d33-8bae-bb0292fc1e9f.jpg)

## RESULT:

Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is designed and executed successfully.
