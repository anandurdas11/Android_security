# Lecture 11 

1.Installing Mobsf Tool in Kali Linux VM

```

git clone https://github.com/MobSF/Mobile-Security-Framework-MobSF.git

```

![image](https://github.com/anandurdas11/Android_security/assets/83402050/5f3be1ee-a8d0-4db0-996a-b70919952a86)

Goto directory and create a python virtual enviroment using the command 

```
python3 -m venv venv

```
Then run `./setup.sh` to install all the dependencies before that activate the enviroment using the command 

```
source venv/bin/activate

```

![image](https://github.com/anandurdas11/Android_security/assets/83402050/6dbba0fa-55b4-4551-b4c5-ecb6b1d355f5)

![image](https://github.com/anandurdas11/Android_security/assets/83402050/00ea58d8-b4fd-40e0-813a-362a6ec57999)

The installation is succesful
use the command 
```
./run.sh
```
To run mobsf tool

![image](https://github.com/anandurdas11/Android_security/assets/83402050/d5a4d1cc-bfac-4e43-a107-d72b886a39da)

The mobsf tool will be running on `127.0.0.1:8000` 

![image](https://github.com/anandurdas11/Android_security/assets/83402050/1a8fab07-4bd8-4081-86c1-86a0a3b8121a)

![image](https://github.com/anandurdas11/Android_security/assets/83402050/6e08ed35-eead-4cf9-ad3d-b7172a99b09d)

> Now we can upload the apk to analyze

![image](https://github.com/anandurdas11/Android_security/assets/83402050/1d72dee7-1436-4ac9-a2d2-b94d6fda4852)

> We can see that various permisions that are used

![image](https://github.com/anandurdas11/Android_security/assets/83402050/91eaf5b1-3c9c-4635-819c-092ba960e38c)

> We can see the list of activities

![image](https://github.com/anandurdas11/Android_security/assets/83402050/9a81fe15-64be-4a33-9687-82313c3dd730)

> We can also analyze the shared libaries

![image](https://github.com/anandurdas11/Android_security/assets/83402050/5d6fd7e6-f084-474a-9b37-1b86ca333f01)

> Manifest Analysis (Android): Analyzes the Android manifest file for permissions, activities, services, and other components to identify potential security misconfigurations.

![image](https://github.com/anandurdas11/Android_security/assets/83402050/8966ad5a-a0da-432f-acb2-b6e6312831cf)

> Code analysis :

![image](https://github.com/anandurdas11/Android_security/assets/83402050/6c5f521b-ab13-4ae2-9424-055be9b4712a)

> We can how much mobsf given the mark to this application

![image](https://github.com/anandurdas11/Android_security/assets/83402050/75344508-20dc-4aaf-a5e2-ef47b8ec0e06)



