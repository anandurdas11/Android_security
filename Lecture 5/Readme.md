# Reverse Engineering of Android App #
1. APK TOOL

   ![image](https://github.com/anandurdas11/Android_security/assets/83402050/c2e0cc9c-25da-4a34-9c5d-4db42c8c2df7)

   Decomiplation: Trying to reach to Source Code From Executable File. Here .dex means Dalvik Executable Code Format

```
  apktool d .\sample.apk -o test
```


![image](https://github.com/anandurdas11/Android_security/assets/83402050/427b1121-c7ec-4b55-82d9-6b3ab14a8351)

We observe that the testsample directory does not contain the classes.dex and resources.arsc files previously present in the ZIP file. 
We observe that there is a apktool.yml file created in the directory. We also observe that there is another AndroidManifest.xml in a new directory called original.
We also observe that there is a new directory called smali which was decompiled from the classes.dex file present in the original APK ZIP archive.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/1c3b9dff-86f4-402b-96bc-1737c8cbebbb)

![image](https://github.com/anandurdas11/Android_security/assets/83402050/4a20dc01-b8a3-4dcb-9278-bdc4f9933804)

![image](https://github.com/anandurdas11/Android_security/assets/83402050/249db967-9354-43ce-b6c2-ec737cd92d4d)

Now Jadx Tool

jadx is a Dex to Java decompiler. It is a command line and GUI tools for producing Java source code from Android Dex and Apk files

![image](https://github.com/anandurdas11/Android_security/assets/83402050/3991cca9-f833-49b9-b924-a4ab047baf7f)

The decompiled JAVA source code is seen in the JADX window.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/573a8fbe-8250-4823-aac3-627c28948433)
