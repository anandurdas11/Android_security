
# LECTURE 2


Android Debug Bridge (adb) is a versatile command-line tool that enables communication with an Android device. The adb command facilitates a variety of device actions, such as installing and debugging apps. It also provides access to a Unix shell that you can use to run a variety of commands on a device.

adb is a client-server program that includes three components:

1. **Client**: Sends commands from your development machine. You can invoke a client from a command-line terminal by issuing an adb command.
2. **Daemon (adbd)**: Runs commands on a device as a background process. The daemon on the Android device connects with the server on the host PC over USB or TCP, which connects to the client used by the end-user over TCP.
3. **Server**: Manages communication between the client and the daemon. The server runs as a background process on your development machine and uses the default port number 5037.


``` 
adb devices
```

The `adb devices` command is used to list all connected Android devices and emulators that are recognized by the adb server. When you run this command, it outputs a list of device identifiers along with their connection status. This command is helpful for verifying that your device is properly connected and recognized by adb.

![Screenshot 2024-05-27 151106](https://github.com/anandurdas11/Android_security/assets/83402050/6a1a7546-1496-4058-835b-c474acd839c7)


```
 emulator -list-avds
```

![Screenshot 2024-05-27 151803](https://github.com/anandurdas11/Android_security/assets/83402050/11b4450d-2478-4d4e-9dbc-da7dc0f673eb)

When we run this command it list the emulators that are running

## Basic ADB Commands


```
 adb devices
 adb -s emulator-5554 shell
```

![Screenshot 2024-05-27 152320](https://github.com/anandurdas11/Android_security/assets/83402050/8492f79a-f0fe-4aec-bc7a-4532fc924780)


```
	id
```

![Screenshot 2024-05-27 152409](https://github.com/anandurdas11/Android_security/assets/83402050/a6ef5a06-26c9-4a0c-a289-a068eec7ce6f)



```
	ls
```

![Screenshot 2024-05-27 152507](https://github.com/anandurdas11/Android_security/assets/83402050/d5ba31ee-7199-4c28-aac4-8eb9f1f88ee6)


```
 cd sdcard
```


![Screenshot 2024-05-27 153345](https://github.com/anandurdas11/Android_security/assets/83402050/695b4900-8f21-4379-aa67-5c6612fca019)



```
pm list packages
```

pm (Package Manager) is an utility program for retrieving various kinds of information related to the application packages that are currently installed on the device.

![Screenshot 2024-05-27 153908](https://github.com/anandurdas11/Android_security/assets/83402050/475d58af-954b-480b-80d0-d501e97a4102)

![Screenshot 2024-05-27 212432](https://github.com/anandurdas11/Android_security/assets/83402050/786340d2-b18b-4acd-906b-8d2eb195510e)


```
pm list packages -3
```

So this command list the all the 3 party packages

```
ps -A | grep myapplication 
```

![Screenshot 2024-05-27 213238](https://github.com/anandurdas11/Android_security/assets/83402050/da6215d4-4ce0-4779-9c1d-2a65956392ad)


This command will give the process id of the specified 3rd party application


```
pm path com.example.myapplication
```
![Screenshot 2024-05-27 213627](https://github.com/anandurdas11/Android_security/assets/83402050/d2ab0477-f094-44a5-b00a-8467494b331d)

This command will give the path where the apk is installed


![Screenshot 2024-05-27 214248](https://github.com/anandurdas11/Android_security/assets/83402050/2d3795c0-3f62-46b0-882f-b094190c811f)


```
adb pull "/data/app/com.example.myapplication-zlEH9mpwrqoT4DWZ4iBFVw==/base.apk" .
```

So this command can be used get the app apk and we can save it 


