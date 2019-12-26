# รายงานผลการทดลอง

<นาย ปิยทัศน์ นวกิจวัฒนา> <รหัสนักศึกษา 603410208-8>
# รายงานผลการทดลอง

## Relative Layout

แสดง Control `title` และ `Detail`

```<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".RelativeActivity">

    <EditText
        android:id="@+id/editText5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <EditText
        android:id="@+id/editText6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:layout_below="@id/editText5"
        android:text="Name" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/editText6"
        android:text="Button" />
</RelativeLayout>

```

แอดทริบิ้วที่แสดงความสัมพันธ์ระหว่าง control ทั้งสอง

``` 

    <EditText
        android:id="@+id/editText6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:layout_below="@id/editText5"
        android:text="Name" />


โค้ด
   android:layout_below="@id/editText5"   
คือคำสั่งที่ให้ @+id/editText6 อยู่ใต้ @id/editText5


```

## Linear Layout

แสดง Control `to`, `subject`, `tag` และ `message`

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".LinearActivity">


    <EditText
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_weight="1"
        android:orientation="horizontal">

        <EditText
            android:id="@+id/editText3"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name" />

        <EditText
            android:id="@+id/editText2"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name" />
    </LinearLayout>

    <EditText
        android:id="@+id/editText4"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:gravity="start|top"
        android:inputType="textMultiLine" />

    <Button
        android:id="@+id/button"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Button" />

</LinearLayout>

```

อธิบายความแตกต่างระหว่าง vertical และ horizontal orientation

```
vertical เลื่อนเป็นเส้นตรงจากบนลงล่าง
horizontal orientation เลื่อนเป็นเส้นตรงจากซ้ายไปขวา
```

## Constrant Layout

จงออกแบบและสร้างหน้า Constrant layout สำหรับแสดงข้อมูลนักศึกษา ประกอบไปด้วย รูปโปรไฟล์ รูปพื้นหลัง ชื่อ-นามสกุล รหัสนักศึกษา และเกรดเฉลี่ยรวม

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".Main3Activity">

    <TextView
        android:id="@+id/textView2"
        android:layout_width="200dp"
        android:layout_height="40dp"
        android:text="เกรดเฉลี่ย 3.02"
        android:textSize="30sp"
        tools:layout_editor_absoluteX="105dp"
        tools:layout_editor_absoluteY="500dp" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="356dp"
        android:layout_height="39dp"
        android:text="รหัสนักศึกษา 603410208-8"
        android:textSize="30sp"
        tools:layout_editor_absoluteX="27dp"
        tools:layout_editor_absoluteY="461dp" />

    <TextView
        android:id="@+id/fullname"
        android:layout_width="314dp"
        android:layout_height="44dp"
        android:text="นาย ปิยทัศน์ นวกิจวัฒนา"
        android:textSize="30sp"
        tools:layout_editor_absoluteX="49dp"
        tools:layout_editor_absoluteY="417dp" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="284dp"
        android:layout_height="284dp"
        app:srcCompat="@drawable/PicInfo"
        tools:layout_editor_absoluteX="63dp"
        tools:layout_editor_absoluteY="89dp" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
