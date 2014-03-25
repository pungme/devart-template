Here we go ! Now let's talk about technical stuff, I can break down my project into 3 main tasks. 

First, Speech regcognition or text-to-speech, I'm using google text-to-speech API to handle all the magic happened under the hood (I hope google will keep it "free" for a while, right ?). My initial design is to have a simple circle on the center of the screen, and the size of the circle represents the volume of the voice. I'm using d3js to handle all the smooth animation. It looks OK now but still need a lot of works on design (well, the dotted border is just for the development). You can see it in-action in the video below.

Here is the sample code for the google speech API

```javascript
  var recognition = new webkitSpeechRecognition();    
  recognition.continuous = true;
  recognition.interimResults = true;
```

The API is pretty neat and I'm very surprise how easy it is in order to implement this.

![prototype#1](../project_images/prototype1.png?raw=true "Prototype")

Also, the microphone stuff. here is the sample how I can get the rms value to calculate the decibel.

```javascript
  var buf = new Uint8Array(2048);
  
  analyser.getByteTimeDomainData(buf) 
  
  if (buf.length < (SIZE + MAX_SAMPLES - MIN_SAMPLES))
    return;  // Not enough data

  for (var i=0;i< SIZE;i++) {
    var val = (buf[i] - 128)/128;
    rms += val*val;
  }
  rms = Math.sqrt(rms/SIZE);
```

Second, Web-cam, I'll work on webcam tomorrow, to take a photo and store it into the server. This shouldn't be hard, based on what I've been googled around. There are plenty of examples that I can follow.

Third, the Stranger Alogorithm, this will be the core part and also the heart of application. At first, it looks simple but turns out more complicated than I thought. I still have no idea yet but I will update this very soon. 

Peace !

http://youtu.be/sLhcx1rZ76Q
