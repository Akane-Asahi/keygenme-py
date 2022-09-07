# keygenme-py
PicoCTF picoGym Practice Challenges | keygenme-py


PicoCTF picoGym Practice Challenges | keygenme-py
![Thumbnail](https://user-images.githubusercontent.com/111799231/188763360-4fc2dedc-f451-4faa-be98-959ff663a919.jpg)


WHAT?
Now this problem is interesting! For my account, the flag was below,
picoCTF{1n_7h3_|<3y_of_ac73dc29}
For your account, the flag will be different, but only those last 8 characters of the flag would vary. Let's help you out to find your flag!

HOW?
Download the file,
<img width="910" alt="wget" src="https://user-images.githubusercontent.com/111799231/188763224-e673efae-a6e1-482f-a6f5-de1816a2be1f.png">

Make a python file to crack the flag, I named it crack.py
<img width="323" alt="crack" src="https://user-images.githubusercontent.com/111799231/188763284-59e990f5-1548-4c90-ba96-dd17112cd4b6.png">

nano crack.py
It will open up a text editor. Then code the following
import hashlib
import base64
hash = hashlib.sha256(b"FRASER").hexdigest()
key_list = [4,5,3,6,2,7,1,8]
print("picoCTF{1n_7h3_|<3y_of_", end = '')
for i in key_list:
  print(hash[i], end = '')
print("}")
<img width="889" alt="code crack" src="https://user-images.githubusercontent.com/111799231/188763328-9f5dea13-50a7-437e-ae52-7bd6ee5eda6f.png">

Awesome! We have now built our very own crack for the software. Now press ctrl+x to Exit, ctrl+y to say yes to save the changes we made and finally press Enter .
Now run the python file typing below command and get the flag,
python ./crack.py

Disclaimer: As I said this flag is only for my account. For your account you just have to find the username in your keygenme-trial.py file.
Type cat keygenme-trial.py to view the code inside of this python file.
In this result you can see username_trial stores a name "FRASER" 
In your file it may be different. Just copy your userameand replace FRASERwith it in the crack.py file. I'm talking about the below line to be specific,
hash = hashlib.sha256(b"FRASER").hexdigest()
WHY
1. To learn reverse engineering
2. To introduce hashlib, sha256, b'' strings in python, hexdigest
