## Binwalk

Binwalk is a simple linux tool for analysing binary files for embedded files and executable code. It is mostly used to extract the content of firmware images. 

### Installation

On kali linux, binwalk is already installed. On ubuntu you can do apt-get install binwalk or you can go to https://github.com/devttys0/binwalk and follow the instructions. Sample binary file can be found [here](http://www.tp-link.com/resources/software/TL-WR841N_V8_130506.zip), it's a router firmware image.

### Usage

The first thing to do when you interact with a new linux tool is to read it's manual pages, this is done by issuing
the command man binwalk. The manual pages offers an overview of the commands supported by binwalk. 

![alt text](http://imgur.com/SIuVzBQ.jpg "Binwalk output")

Issuing `binwalk 'filename.bin'` results in binwalk showing the contents of the binary files, and the offset at which the file begins in hexadecimal and decimal. The offset is useful if you want to extract the contents of the file with a tool like `dd`.

Binwalk can also automatically extract all the files it finds within the firmware image, this is possible with the `-e` switch. Binwalk can also search for string in the binary files with the `-S` option. The `-M matryoshka` option instructs binwalk to recursively scan extracted files, the matroshka is a reference to Russian dolls that have other dolls inside them. 

![alt text](http://imgur.com/ZXrjxuU.jpg "Matryoshka doll")

### Conclusion
binwalk is an important tool for a forensic analyst. Coupled with other tools it can be an invaluable tool in an investigation. 
