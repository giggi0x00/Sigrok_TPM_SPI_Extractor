# Sigrok_TPM_SPI_Extractor
Short introduction to the topic here:<br><br>
https://github.com/giggi0x00/Bitlocker-SPI-TPM-Key-sniffing

<br>
<br>

Decoder for sigrok that while sniffing SPI protocol extract the VMK Key from TPM.

# HOW TO USE:

Create a directory under sigrok decoder named "tpm_key_sniffing" and add the files.

example from a previous capture: 

`sigrok-cli -i capture.vcd  -I vcd:numchannels=4 -P tpm_key_sniffing:wordsize=8:bitorder=msb-first:miso=Channel_1:mosi=Channel_0:clk=Channel_2:cs=Channel_3`

***Channels name can be identified using the following command:***

`sigrok-cli -i capture.vcd --show`

# OUTPUT:

 KEY: fffad34b5ac07c943a45780108883c9eb7a84009a4782459b12cae41230047df
