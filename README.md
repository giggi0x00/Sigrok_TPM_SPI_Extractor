# Sigrok_TPM_SPI_Extractor

Decoder for sigrok that while sniffing SPI protocol extract the VMK Key from TPM.<br>

# HOW TO USE:

Create a directory under sigrok decoder named "tpm_key_sniffing" and add the files.

example from a previous capture: <br>

sigrok-cli -i untitled.vcd  -I vcd:numchannels=4 -P tpm:wordsize=8:miso=Channel_1:mosi=Channel_0:clk=Channel_2:cs=Channel_

# OUTPUT:

 KEY:  
['0xff', '0xfa', '0xd3', '0x4b', '0x5a', '0xc0', '0x7c', '0x94', '0x3a', '0x45', '0x78', '0x1', '0x8', '0x88', '0x3c', '0x9e', '0xb7', '0xa8', '0x40', '0x9', '0xa4', '0x78', '0x24', '0x59', '0xb1', '0x2c', '0xae', '0x41', '0x23', '0x0', '0x47', '0xdf']
