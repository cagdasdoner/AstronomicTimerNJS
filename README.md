# AstronomicTimerNJS
An Astronomic Timer implementation for NodeJS

This timer is implemented to be an alternative of it's hardwared versions. 
An astronomic timer fetchs sunrise and sunset time data from an embedded flash or like we do in our module; fetchs from network. 
Using API for sun properties is api.sunrise-sunset.org. 

USAGE

1. Modify your local time and zone settings which stored under astro_info.js.

  It is important to set Latitude, Longitude and UTC offset of your location. 
  
2. You need to install "moment" module via npm. 

  npm install moment
  
3. Import timer from your app. 

   var astronomic = require('./astronomic/astro_module');

4. Start your astronomic timer wherever you want. 
   astronomic.start();

5. Astronomic module is able to cover himself on such error conditions. So do not worry about it.

6. Latest one; you need to listen an event that triggered from module, called "astronomicEvent". It carries a data beyond him. If the data is equal to "on", that means it is time to prepare to night watch. If it is "off", daylight gonna be with us.  
