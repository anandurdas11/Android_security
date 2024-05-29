# Lecture 6

We install the APK to the emulator by typing the below command.
```
adb install diva-beta.apk
```
![image](https://github.com/anandurdas11/Android_security/assets/83402050/f2b87dbc-0d1c-47eb-afd6-13002ba11c25)

![image](https://github.com/anandurdas11/Android_security/assets/83402050/218178da-97f0-4614-80a6-cc62240b43b5)

1. Insecure Logging
We type adb logcat in the terminal window.
```
adb logcat | grep -i "credit card"
```
We click on the Insecure Logging button.
We type a number in the EditText field and click on the Check Out button.
We observe that An error occurred toast message is shown, and that the logcat has logged the input that
was entered.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/35a54edb-f146-4a54-bbcf-dacb63412d4a)

We open JADX and open the diva-beta.apk file.
We observe the decompiled source code and open the LogActivity in the JADX.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/bd43eda0-d19d-4709-8353-487e764d48e1)

2. Hardcoding Issues - Part 1
We observe the decompiled source code and open the HardcodeActivity in the JADX.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/b91b3c63-6fa6-44c8-9cd7-e5ec880fc467)

We type the hardcoded vendor key in the EditText field.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/20732843-b78e-43b7-a1cc-dba402d02823)

3. Insecure Data Storage - Part 1
We explore the application by entering username and password in the EditText field.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/c5983a15-3f1a-42bf-9e06-11959f182eb2)

We use adb shell to explore the file system used by the application.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/5e72dab7-e908-494e-a82a-9434ac5a1c4a)

Inside the /data/data/jakhar.aseem.diva directory, we notice the databases and shared_prefs directory.
We type cat shared_prefs/jakhar.aseem.diva_preferences.xml to see the username and password that
were saved by the application

![image](https://github.com/anandurdas11/Android_security/assets/83402050/a201b0a8-4d1e-46d1-bdd6-67f40cea85d3)

We observe the decompiled source code and open the InsecureDataStorage1Activity in the JADX

![image](https://github.com/anandurdas11/Android_security/assets/83402050/43afd186-7845-4039-91d6-e45ffe1f1c49)

4. Insecure Data Storage - Part 2
We explore the application by entering username and password in the EditText field.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/945701d2-b64b-49ee-8f59-45286c307763)

We use adb shell to explore the file system used by the application.
Inside the /data/data/jakhar.aseem.diva directory, we notice the databases and shared_prefs directory.
We observe that there is a new file inside the databases directory.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/5a916bd9-2d14-460a-bf5c-1d8eb1fc2fda)

We open the ids2 database using the sqlite3 program, and enter select * from myuser; to view the
saved username and password.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/d3e14cce-6456-4708-8aa6-b7c664a165d1)

We observe the decompiled source code and open the InsecureDataStorage2Activity in the JADX.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/80ec5639-0cd0-4d5d-bea8-a97313edb9bf)

5. Insecure Data Storage - Part 3
We explore the application by entering username and password in the EditText field.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/a33475e0-5501-4b3b-96c1-f5f2dd98eb1a)

We use adb shell to explore the file system used by the application.
Inside the /data/data/jakhar.aseem.diva directory, we observe that there is a new file with the name
uinfo-1455578291tmp. We display the contents of the file using the cat uinfo-1455578291tmp command.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/5fb8680b-80ba-4aab-8767-513bc651a9d2)

We observe the decompiled source code and open the InsecureDataStorage3Activity in the JADX.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/579fe9a3-de43-4da3-872f-5f1946d6123c)

6. Insecure Data Storage - Part 4
We explore the application by entering username and password in the EditText field.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/60abe35d-ef27-41d7-9d65-2192125e220e)

We observe the decompiled source code and open the InsecureDataStorage4Activity in the JADX.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/42e1b509-0076-42d9-be3c-6885b84573e4)

In the adb shell, we navigate to cd /sdcard and type the commands: ls -a and cat .uinfo.txt to view
the contents of the file.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/9d7efd7c-a919-49d1-a04d-6a389b050dfc)


