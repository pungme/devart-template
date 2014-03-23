Here we go ! Now let's talk about technical stuff, I can break down my project into 3 main task. 

First, Speech regcognition or text-to-speech. I'm using google text-to-speech api to handle all the magic happend under the hood (I hope google will keep it "free" for a while, right ?). My initial design is to have a simple circle on the center of the screen, and the size of the circle represent the volume of the voice. I'm using d3js to handle all the smooth animation. It looks okay now but still need a lot of work on design. You can see it in-action in the video below.

Here is the sample code for the google speech api

```javascript
  var recognition = new webkitSpeechRecognition();    
  recognition.continuous = true;
  recognition.interimResults = true;
```

The api is pretty neat and I'm very surprise how easy to implement this.

![prototype#1](../project_images/prototype1.png?raw=true "Prototype")

Also, the microphone stuff. here is the sample how can I get the rms value to calculate the decibel.

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

Second, Web-cam. I'll work on webcam tomorrow, to take a photo and store it to the server. This shouldn't be hard, based on what I've been googled around. There are plenty of example that I can follow.

Third, The Stranger Alogorithm. This will be the core part, the heart of application. At first it looks simple but turns out more complicate than I thought. I still have no idea yet, but I will update this very soon. 

Peace !

http://youtu.be/sLhcx1rZ76Q
