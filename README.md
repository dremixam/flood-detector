# flood-detector
Javascript detection of repetitive strings usine the LZ algorithm

## Node.js
    npm install flood-detector

then :
    FloodDetector = require('flood-detector');
    if (FloodDetector.evaluate(string)) {
      console.log('probably not flood');
    } else {
      console.log('probably flood');
    }


## bower
    bower install flood-detector

    

Yeah, that's a damn small package