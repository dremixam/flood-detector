# flood-detector
Javascript detection of repetitive strings usine the LZ algorithm

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


## bower

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