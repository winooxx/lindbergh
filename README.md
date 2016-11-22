# lindbergh
Tool collection for the Lindbergh arcade

# Getting the inqury bytes

The extended inquiry 0xEC reply is required to create the keys.
The easiest way is to use plscsi the exists for windows and linux and is very easy to use.
Just send the following command to get the required bytes: 

plscsi -v -p -x "85 08 0E 00 00 00 01 00 00 00 00 00 00 00 EC 00" -i x200 -t inq.bin

# Unlocking Commands

Each devices uses a slightly different unlock command again using plscsi will simplfiy things:

Unlock Maxtor HDDs:

plscsi -v -p -x "85 0A 06 00 00 00 01 00 00 00 00 00 00 40 F2 00" -o x200 -f key.bin

Unlock ADTec CF cards:

plscsi -v -p -x "85 0A 06 00 03 00 01 00 AB 00 00 00 00 00 82 00" -o x200 -f key.bin

Unlock SanDisk:

The tool will create the bytes for you simply insert them between the ""s

plscsi -v -p -x ""

# BIOS password

mssvhy