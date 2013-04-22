# ds18b20

Get sensor data from ds18b20 connected to the Raspberry (GPIO w1 pin).

## Usage

### Drivers

1-Wire drivers need to be loaded in order to create the connection between the physical sensor and the rPI.
You can load them from the terminal:

    sudo modprobe wire
    sudo modprobe w1-gpio
    sudo modprobe w1-therm

### Code

    var sense = require('ds18b20');
    sense.sensors(function(err, ids) {
      // got sensor IDs ...
    });

    // ...

    sense.temperature('123456789', function(err, value) {
      console.log('Current temperature is', value);
    });

## License

(The MIT License)

Copyright (c) 2013 Christophe Hamerling &lt;christophe.hamerling@gmail.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
