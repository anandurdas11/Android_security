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
