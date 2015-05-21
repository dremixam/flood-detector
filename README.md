# flood-detector
Javascript detection of repetitive strings using the LZ algorithm

How it works ?

When people type garbage messages in order to be annoying, they tend to repeat word or letters or to use specific patterns which will allow a better compression of the string.
By LZ-compressing the string and looking how much we were able to reduce its size, we can estimate if the text is garbage or real text.

This is not perfect and I think maybe there is a better solution for this. Don't hesitate to [tell me](https://twitter.com/dremixam) if you know a better way.

This is currently active on https://fr.lou.lt/ to avoid annoying floods.
Short demo can be found [here](http://storage.melinon.com/flood/).

## Node.js

    npm install flood-detector

then:

    FloodDetector = require('flood-detector');
    if (FloodDetector.evaluate(string)) {
      console.log('probably not flood');
    } else {
      console.log('probably flood');
    }
    

There is an optional parameter to change the trigger value (default value is 30) :

    // This will return true only if the compressed string has more than 40% of the size of the original string
    FloodDetector.evaluate(string, 40); 

## Bower

    bower install flood-detector

then:

    <script src="bower_components/lz-string/libs/lz-string.min.js"></script>
    <script src="bower_components/flood-detector/flood-detector.js"></script>
    <script>
      if (FloodDetector.evaluate(string)) {
        console.log('probably not flood');
      } else {
        console.log('probably flood');
      }
    </script>

Yeah, that's a damn small package but very useful for me.

# License

    DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE 
                      Version 2, December 2004 

    Copyright (C) 2004 Sam Hocevar <sam@hocevar.net> 

    Everyone is permitted to copy and distribute verbatim or modified 
    copies of this license document, and changing it is allowed as long 
    as the name is changed. 

              DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE 
     TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION 

    0. You just DO WHAT THE FUCK YOU WANT TO.
