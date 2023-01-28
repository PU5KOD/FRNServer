# FRNServer
## Files for make a Free Radio Network Server/Client.
### **1. SERVER:**
### **1.1. AlterFRN server, revision 7348, 2022-10-13:**

* Linux-aarch64 (Linux/ARM 64bit) RaspberryPi, OrangePi, ... 64bit
  >http://alterfrn.ucoz.ru/S7348/FRNServerConsole.Linux-aarch64.7348r.tgz

* Linux-armhf (Linux/ARMv6 32bit) RaspberryPi, OrangePi, ... 32bit
  >http://alterfrn.ucoz.ru/S7348/FRNServerConsole.Linux-armhf.7348r.tgz

* Linux-armv7 (Linux/ARMv7 32bit) RaspberryPi, OrangePi, ... 32bit
  >http://alterfrn.ucoz.ru/S7348/FRNServerConsole.Linux-armv7.7348r.tgz



### **1.2. AlterFRN Server, revision 6584, 2021-01-22:**

* Linux-aarch64 (Linux/ARM 64bit) RaspberryPi, OrangePi, ... 64bit
  >http://alterfrn.ucoz.ru/S6584/FRNServerConsole.Linux-aarch64.6584r.tgz

* Linux-armhf (Linux/ARM 32bit) RaspberryPi, OrangePi, ... 32bit
  >http://alterfrn.ucoz.ru/S6584/FRNServerConsole.Linux-armhf.6584r.tgz


### **2. CLIENT:**
  ### **AlterFRN client, revision 7312, 2022-07-17:**

* Linux-aarch64 ARM64 RaspberryPi, OrangePi, ... 64bit
  >http://alterfrn.ucoz.ru/C7312/FRNClientConsole.Linux-aarch64.7312r.tgz

* Linux-armhf ARM32v6 RaspberryPi, OrangePi, ... 32bit
  >http://alterfrn.ucoz.ru/C7312/FRNClientConsole.Linux-armhf.7312r.tgz

* Linux-armv7 ARM32v7 RaspberryPi, OrangePi, ... 32bit
  >http://alterfrn.ucoz.ru/C7312/FRNClientConsole.Linux-armv7.7312r.tgz



### **To install the 64bit server as a service that starts automatically, follow the steps below:**

* Create directory and download the project files:
```
cd /usr/src/ && sudo wget https://github.com/PU5KOD/FRNServer/raw/main/Server/FRNServerConsole.Linux-aarch64.7348r.tgz
```
* Unzip the project files:
```
sudo tar -zxvf FRNServerConsole.Linux-aarch64.7348r.tgz
```
* Remove unnecessary file:
```
sudo rm FRNServerConsole.Linux-aarch64.7348r.tgz
```
* Change name go to new directory:
```
sudo mv FRNServerConsole.Linux-armhf.7348r FRNServer && cd FRNServer
```
* Change filename of the main file:
```
sudo mv FRNServerConsole.Linux-armhf.r7348 FRNServer
```
* Copy service file to system:
```
sudo cp frn.service /etc/systemd/system/
```
* Enable the service:
```
sudo systemctl enable frn.service
```

Once installed, the service can be modified by changing the above command parameters with `ENABLE`, `DISABLE`, `STATUS`, `START`, `RESTART` and `STOP`. For other versions of the server/client, simply substitute the location of the source file in the commands described above.
