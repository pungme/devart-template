Hello everybody.

Just get back from my workplace and have a short look on other's project. Dude, thst's make me freak out already LOL, you guys are such a magician! But life goes on, let's talk about my today's progress. :) 

Now I've got everything running on my private server, get the camera working with a pretty simple interface. also successfully push the base64data png to my private server. I will deploy as a prototype soon. Here are some sample code for the camera canvas.

```javascript
    var video = document.getElementById("video");
    navigator.webkitGetUserMedia(videoObj, function(stream){
        video.src = window.webkitURL.createObjectURL(stream);
        video.play();
    }, errBack);
```

and for the base64decode

```php
    $filepath = "../img/" . uniqid() . '.png';
    $success = file_put_contents($filepath, base64_decode($imgsrc));
```

I know, I know, it's not the most complicate code in the world, but yeah, that's what I've got so far for the camera. pretty simple eh ?

In my local machine everything is kind of works fine with some bug. I've realized taht the technical stuff of my project is pretty simple, maybe too simple... , but I think for the concept is quite strong. About the stranger algorithm, I'm just random it for now, just hope I'll figure something out before this friday. I've push all work-in-progress source over here you guys can check it out here 

[https://github.com/pungme/codeart](https://github.com/pungme/codeart)


See you tmr !
