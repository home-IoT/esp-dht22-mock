# DHT22 Mock Server

| `master`   | `develop`     |
| ---------- | --------------|
| [![Build Status](https://travis-ci.org/home-IoT/esp-dht22-mock.svg?branch=master)](https://travis-ci.org/home-IoT/esp-dht22-mock) | [![Build Status](https://travis-ci.org/home-IoT/esp-dht22-mock.svg?branch=develop)](https://travis-ci.org/home-IoT/esp-dht22-mock) |
   
This is a mock service for simulating temperature and humidity sensor boards programmed with  
[home-IoT/esp-dht22](https://github.com/home-IoT/esp-dht22). 

## API 
The service offers a very simple API which is specified in the [swagger.yml](api/esp-dht22.yml) file:

### Reading
**`GET /`** provides the current (imaginary) reading of the sensor. 

Example response:
```
{
    "deltaTime": 0,
    "device": "dht22-03",
    "dht22": {
        "heatIndex": 25.59,
        "humidity": 96.62,
        "temperature": 25.05
    },
"stale": 0
}
```
See [home-IoT/esp-dht22](https://github.com/home-IoT/esp-dht22) for details.

#### WiFi Configuration

**`GET /config?ssid=<SSID>&password=<PASSWORD>`**
fakes configuration of the board with a new SSID and an *optional* password. See [home-IoT/esp-dht22](https://github.com/home-IoT/esp-dht22) for details.

## License
The code is published under an [MIT license](LICENSE.md). 

## Contributions
Please report issues or feature requests using Github issues. Code contributions can be done using pull requests. 
