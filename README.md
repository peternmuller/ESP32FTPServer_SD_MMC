# ESP32FTPServer
## Simple FTP Server for using ESP32 with SD_MMC 

### This is a fork of David Paiva's esp8266FTPServer designed to work with SD_MMC on a LILYGO T-SIM7080G S3 ESP32 board, but also works on regular ESP32.

I've modified a FTP server from arduino/wifi shield to work with ESP32....

This allows you to FTP into your ESP32 and access/modify the spiffs folder/data...it only allows one FTP connection at a time....very simple for now...

I've tested it with Filezilla, and the basics work (upload/download/rename/delete). There's no create/modify directory support.

You need to setup Filezilla (or other client) to only allow 1 connection.
To force FileZilla to use the primary connection for data transfers:
Go to File/Site Manager then select your site.
In Transfer Settings, check "Limit number of simultaneous connections" and set the maximum to 1

Only supports Passive FTP mode....

It does NOT support any encryption, so you'll have to disable any form of encryption...

Feel free to try it out (sample provided)... unzip into your arduino library directory (and restart arduino IDE).


This is the original project on GitHub I worked from: https://github.com/gallegojm/Arduino-Ftp-Server/tree/master/FtpServer