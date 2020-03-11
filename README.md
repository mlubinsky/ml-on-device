# ml-on-device

Based on https://github.com/BlackstoneEngineering/aiot-workshop
add-machine-learning branch

```
docker run  -i -t mbedos/mbed-os-env

mbed import https://github.com/mlubinsky/ml-on-device
cd ml-on-device
mbed deploy
mbed config -G CLOUD_SDK_API_KEY ak_1MDE3MDNhZDMwZDJkOGFlZGE2MWYxMzRjMDAwMDAwMDA017040793c538aeda61f134c00000000IQBgqsHL7r63RXOEXAEiz2YxB5kIgujJ
mbed dm init -d "arm.com" --model-name "mbed" -q --force
mbed compile -m NUCLEO_H743ZI2 -t GCC_ARM
mbed dm update device -D 0170a6e08345000000000001001a30be -m NUCLEO_H743ZI2 --no-cleanup
```
