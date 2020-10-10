# Any file to QR
This is script that can convert any file to splited QR codes

**Try also another branch [ascii85](https://github.com/BxOxSxS/Any-file-to-QR/tree/ascii85) witch is more effective**
## How it works
* Encode:
     1. Converts file to base64 text file
     2. Splits text file to many files with the maximum size of QR code (2953 bytes)
     3. Creates QR code from each file
* Decode
     1. Converts QR to splitted text files
     2. Connects files into one
     3. Decodes file using base64

## Requirement
* bash
* base64
* [GNU Coreutils](https://www.gnu.org/software/coreutils/)
* [qrencode](https://github.com/fukuchi/libqrencode) (for encode QR)
* [zbar](https://github.com/mchehab/zbar) (also know as zbar-tools) (for decode QR)

## How to use
Script have two parametrs
* `create [file]` it will create QR codes in [file]_qr
* `convert [qr codes dir]` it will convert file from QR codes in the given dir to `[file]_converted` **Warning! Script will try to convert all `.png` files from that dir so make sure it only has appropriate files**

Example of usage: `bash qr.sh create file.zip`, `bash qr.sh convert file.zip_qr`

## But Why?
I really don't know. The process takes an unprofitable amount of memory and time:
1 Mib encode to 3,8Mib in 480 png files in about 5 seconds and decodes in about 1 minute but I have done it. You can now convert your favorite song into QR codes and hang it on the wall
