# raspberrypi


## Ubuntu Server setup
1. Download the following:
    - Ubuntu Server OS: https://ubuntu.com/download/raspberry-pi
    - Image writer: https://www.balena.io/etcher/
2. Burn the OS on the SD card:
    - SD card must be clean and well formatted to its default settings
    - OS extension file is .xz
3. Plug the SD card to raspberry pi
4. Power on the raspberry pi
    - Default username and password is ubuntu
6. Connect the raspberry pi on wifi using netplan
    - sudo vim /etc/netplan/50-cloud-init.yaml    # can be different config file
      ```
      wifis:
          wlan0:
              access-points:
                  "Wifi Name":
                      password: "wifi password"
              dhcp4: true
      ```

    - sudo netplan generate
    - sudo netplan apply
7. Test network connection
    ```
    ping www.google.com.ph
    ```
