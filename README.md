# FonPT Library
This library uses Fon credentials to perform authorization on FON routers related to NOS ISP in Portugal using ESP8266 Arduino Library. For now doesn't work with NOS accounts, only works with Fon accounts.

## Example

```
#include <Arduino.h>
#include <FonPT.h>

FonPT fon;

void setup(){

  Serial.begin(115200);
	if (fon.auth("jonh@doe.com", "12345")){
   		Serial.println("You are Logged In");
  	}

}

void loop(){
  delay (200);
}

```

### Requirements
[ESP8266 Arduino Library](https://github.com/esp8266/Arduino)


-
###Functions
Authorize:

```
bool auth(fonUser,fonPass);
```
```
bool auth(fonUser,fonPass,fonSSID);
```

Get Router IP:

```
String getIntIP();
```

Get Internet IP

```
String getExtIP();
```
###Note
Serial port 0 is mandatory because debug is enabled by default on Serial port 0, if you want to disable debugging just comment the line in FonPT.h:

// #define DEBUG_FON