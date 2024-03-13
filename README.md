# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.geeksforgeeks.org” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as ImplicitIntent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: KARTHICK K
Registeration Number : 212222040070
*/
```
## ACTIVITY_MAIN.XML:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:autofillHints="enterlink"
        android:id="@+id/editTextText"
        android:layout_width="290dp"
        android:layout_height="48dp"
        android:hint="@string/hint_web"
        android:inputType="text"
        android:textAlignment="center"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.495"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.935" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="324dp"
        android:text="@string/search_btn"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## MAINACTIVITY.JAVA:
```
package com.example.implicitintent;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.EditText;
import android.widget.Button;
import android.net.Uri;
import android.content.Intent;
import android.view.View;

public class MainActivity extends AppCompatActivity {
    EditText editText;
    Button button;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }

        });
    }
}
```

## OUTPUT
![Screenshot 2024-03-09 114335](https://github.com/karthick960/ImplicitIntent-MAD/assets/121215938/31f4d42c-1569-4827-bc38-72d1907d5663)

![Screenshot 2024-03-09 114347](https://github.com/karthick960/ImplicitIntent-MAD/assets/121215938/135214b0-3168-4631-a54a-9d4071425772)

![Screenshot 2024-03-09 115425](https://github.com/karthick960/ImplicitIntent-MAD/assets/121215938/d55b4f70-f9b7-4e9c-8a0e-900121b5a1f5)



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
