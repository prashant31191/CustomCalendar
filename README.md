# Custom Android Calendar

![gif](http://riontech.com/library/calendar/calendar.gif)

#Usage
---
Maven repo
```
maven {
    url "https://dl.bintray.com/riontech/maven"
}
```
Add the dependency to your build.gradle.
```
dependencies {
    compile 'com.riontech:calendar:1.0'
}
```
Add the indicator to your layout.

```
<com.riontech.calendar.CustomCalendar
        android:id="@+id/customCalendar"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:endMonth="07"
        app:endYear="2016"
        app:startMonth="01"
        app:startYear="2016" />
```

Create object of CustomCalendar in your activity
```
private CustomCalendar customCalendar;
```

In your acitivty onCreate initialize the object and set eventDate with count.
And add it to customCalendar object by using addAnEvent method.
```
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        customCalendar = (CustomCalendar) findViewById(R.id.customCalendar);

        String[] arr = {"2016-06-10", "2016-06-11", "2016-06-15", "2016-06-16", "2016-06-25"};
        for (int i = 0; i < 5; i++) {
            int eventCount = 3;
            customCalendar.addAnEvent(arr[i], eventCount, getEventDataList(eventCount));
        }
    }
```

# TODOs
* Add Event with Plus button
* Adding Reminders for Event, Birthday, etc
* Awesome UI-UX

Developed By
---
 * Keyur - <keyuraashra@gmail.com>
 * G+ [Keyur Ashra](https://plus.google.com/u/0/+KeyurAshra)
 * LinkedIn [Keyur Ashra](https://www.linkedin.com/in/keyurashra)

License
---

    Copyright 2016 Riontech

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


