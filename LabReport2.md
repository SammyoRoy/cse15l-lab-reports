# Lab Report 2
### Part 1
![Image](StringServerCodeSS.png)
![Image](HelloCommandSS.png)

The method ```handleRequest(URI url)``` is called, and relative URL ```/add-message?s=Hello``` is passed in as the URI argument. As for relevant fields in the method, ```url.getPath()``` checks if ```/add-message``` is in the path. In this case, the path is indeed ```/add-message```. The query is ```s=Hello```, and ```parameters[0]``` is set to ```s``` while ```parameters[1]``` is set to ```Hello```. ```Parameters[1]``` is then added to ```output```, and ```output``` is returned, which displays ```Hello on the screen```.
![Image](HowAreYouSS.png)
The method ```handleRequest(URI url)``` is called, and relative URL ```/add-message?s=How are you``` is passed in as the URI argument. As for relevant fields in the method, ```url.getPath()``` checks if ```/add-message``` is in the path. In this case, the path is indeed ```/add-message```. The query is ```s=How are you```, and ```parameters[0]``` is set to ```s``` while ```parameters[1]``` is set to ```How are you```. ```Parameters[1]``` is then added to ```output```, and ```output``` is returned, which displays:
```
Hello
How are you
```



