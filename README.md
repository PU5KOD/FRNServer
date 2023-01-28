# FRNServer
Files for make a Free Radio Network Server/Client
Below the instalation instruction.

AlterFRN server, revision 7348, 2022-10-13:

• Linux-aarch64 (Linux/ARM 64bit) RaspberryPi, OrangePi, ...

64bit http://alterfrn.ucoz.ru/S7348/FRNServerConsole.Linux-aarch64.7348r.tgz

• Linux-armhf (Linux/ARMv6 32bit) RaspberryPi, OrangePi, ...

32bit http://alterfrn.ucoz.ru/S7348/FRNServerConsole.Linux-armhf.7348r.tgz

• Linux-armv7 (Linux/ARMv7 32bit) RaspberryPi, OrangePi, ...

32bit http://alterfrn.ucoz.ru/S7348/FRNServerConsole.Linux-armv7.7348r.tgz

AlterFRN Server, revision 6584, 2021-01-22:

• Linux-aarch64 (Linux/ARM 64bit) RaspberryPi, OrangePi, ...

64bit http://alterfrn.ucoz.ru/S6584/FRNServerConsole.Linux-aarch64.6584r.tgz

• Linux-armhf (Linux/ARM 32bit) RaspberryPi, OrangePi, ...

32bit http://alterfrn.ucoz.ru/S6584/FRNServerConsole.Linux-armhf.6584r.tgz

AlterFRN client, revision 7312, 2022-07-17:

• Linux-aarch64 ARM64 RaspberryPi, OrangePi, ...

64bit http://alterfrn.ucoz.ru/C7312/FRNClientConsole.Linux-aarch64.7312r.tgz

• Linux-armhf ARM32v6 RaspberryPi, OrangePi, ...

32bit http://alterfrn.ucoz.ru/C7312/FRNClientConsole.Linux-armhf.7312r.tgz

• Linux-armv7 ARM32v7 RaspberryPi, OrangePi, ...

32bit http://alterfrn.ucoz.ru/C7312/FRNClientConsole.Linux-armv7.7312r.tgz

To install the 32bit server as a service that starts automatically, follow the steps below:

cd /usr/src/ && sudo wget https://github.com/PU5KOD/FRNServer/blob/main/Server/FRNServerConsole.Linux-armhf.7348r.tgz

sudo tar -zxvf FRNServerConsole.Linux-armhf.7348r.tgz

sudo rm FRNServerConsole.Linux-armhf.7348r.tgz

sudo mv FRNServerConsole.Linux-armhf.7348r FRNServer && cd FRNServer

sudo mv FRNServerConsole.Linux-armhf.r7348 FRNServer

sudo cp frn.service /etc/systemd/system/

sudo systemctl enable frn.service

Once installed, the service can be modified by changing the above command parameters with ENABLE, DISABLE, STATUS, START, RESTART and STOP.
For other versions of the server, simply substitute the location of the source file in the commands described above.
