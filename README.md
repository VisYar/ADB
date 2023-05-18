# ADB
1. Отобразить подключённый девайс в консоли.

`./adb devices`

 2. Установить .apk файл приложениия todolist на телефон с компьютера через ADB/
 
 
`./adb install C:\Users\...... .apk`

 3. Вывести адрес приложения todolist в системе Android
 
`./adb shell "pm list packages -f | grep todolist"`

 4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.
 

`.\adb shell screencap /storage/emulated/0/DCIM/123.png | ./adb pull /storage/emulated/0/DCIM/123.png  C:\Users\38066\Desktop\new\001_ToDoList-master\app\build\outputs\apk\debug\123.png`

или разными командами:

`./adb shell screencap /storage/emulated/0/DCIM/123.png`

`./adb pull  /storage/emulated/0/DCIM/123.png  C:\Users\38066\Desktop\new\001_ToDoList-master\app\build\outputs\apk\debug\123.png`

 5. Вывести в консоль логи приложения todolist
 

`./adb shell "logcat | grep -nw com.android.todolist"`

 6. Скопировать логи приложения todolist на компьютер.
 

`./adb shell "logcat | grep -nw com.android.todolist" > C:\Users\38066\Desktop\new\001_ToDoList-master\app\build\outputs\apk\debug\log_todolist.log`

закончить запись логов ctl + c

 7. Удалить приложение todolist с телефона через ADB


`./adb uninstall com.android.todolist`
