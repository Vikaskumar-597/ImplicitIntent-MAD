# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1:Start the application.

Step 2:Create the user interface using XML layout.

Step 3:Create an EditText to enter the URL.

Step 4:Create a Button to perform the search operation.

Step 5:Initialize the EditText and Button using findViewById().

Step 6:Set an OnClickListener() for the Button.

Step 7:Get the URL entered by the user using getText().toString().

Step 8:Create an implicit Intent using Intent.ACTION_VIEW.

Step 9:Convert the entered URL into a URI using Uri.parse().

Step 10:Pass the Intent to startActivity() to open the appropriate application.

Step 11:Android identifies a suitable application, such as a web browser, to handle the request.

Step 12:Stop


## PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by: Vikaskumar M
Registeration Number : 212224220122
*/
```
## MainActivity.java
```python
package com.example.exp_02;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.btn);
        editText = (EditText) findViewById(R.id.editText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```
## activity_main.xml
```python
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/editText"
        android:layout_width="374dp"
        android:layout_height="60dp"
        android:layout_marginTop="252dp"
        android:background="@android:drawable/edit_text"
        android:backgroundTint="#95D3FD"
        android:hint="Enter the URL...."
        android:inputType="text"
        android:padding="15dp"
        android:singleLine="true"
        android:textAlignment="center"
        android:textColor="#000000"
        android:textColorHint="#000000"
        android:textSize="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.567"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/btn"
        android:layout_width="288dp"
        android:layout_height="48dp"
        android:layout_marginTop="20dp"
        android:backgroundTint="#5146E5"
        android:text="SEARCH"
        android:textColor="#FFFFFF"
        android:textSize="16sp"
        android:textStyle="bold"
        app:cornerRadius="14dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.495"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/editText"
        app:layout_constraintVertical_bias="0.26" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

## OUTPUT
<img width="1247" height="690" alt="Screenshot 2026-11-01 192352" src="https://github.com/user-attachments/assets/303d5b66-f906-46a6-8a9f-3f8e8f6d70af" />

<img width="1248" height="688" alt="Screenshot 2026-11-01 192403" src="https://github.com/user-attachments/assets/6a073cad-6985-44f6-8819-ef3dec25b5a0" />

<img width="340" height="638" alt="Screenshot 2026-11-01 193539" src="https://github.com/user-attachments/assets/dc41d679-cbc6-4420-9d93-6ab7bc5f4500" />
<img width="356" height="647" alt="Screenshot 2026-11-01 193553" src="https://github.com/user-attachments/assets/6372f6b4-f880-4319-8b83-d08ae8966aff" />


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


