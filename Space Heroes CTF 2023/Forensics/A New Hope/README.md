### description
-----------------------------
Princess Leia has been kidnapped! She managed to send a message to this droid we have recovered. It was damaged while we were recovering it however. It seems that sometimes you have to tear something down, in order to build them back up.

Can you recover the message?
File: A_New_Hope.pptx
### solve
-----------------------------
* Unzip the powerpoint file, there will be a jpeg file that can't be opened.
* Edit the first two bytes to the correct format for a jpeg file. 
```bash
xxd -ps image1.png > image1.dat
vim image1.dat
xxd -r -p image1.dat > image1.jpeg
```

Flag:
![](../_images/Pasted%20image%2020230424000850.png)
