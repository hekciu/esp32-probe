## Playing aroung with ESP32-S3
# OS: Debian 12

# In examples below PORT should be replaced with actual system device eg. /dev/ttyUSB0 or /dev/ttyACM0

# First time:

- source ./setup.sh
- source ./init.sh
- idf.py set-target esp32s3
- idf.py menuconfig
- idf.py build
- sudo usermod -a -G dialout $USER
- sudo chmod a+rw PORT

# Next times:
- source ./init.sh
- idf.py build
- idf.py -p PORT flash 

# To monitor output:
- idf.py -p PORT monitor
