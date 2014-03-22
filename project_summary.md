# You as a Stranger

## Authors

[https://github.com/pungme](https://github.com/pungme)

## Description
Coming soon...

## Link to Prototype
Coming soon...

## Example Code
Coming soon... 
```
  var buf = new Uint8Array(2048);
  analyser.getByteTimeDomainData(buf) //get buf 
	if (buf.length < (SIZE + MAX_SAMPLES - MIN_SAMPLES))
		return;  // Not enough data

	for (var i=0;i<SIZE;i++) {
		var val = (buf[i] - 128)/128;
		rms += val*val;
	}
	rms = Math.sqrt(rms/SIZE);
```
## Links to External Libraries
Coming soon...

## Images & Videos
Coming soon...

