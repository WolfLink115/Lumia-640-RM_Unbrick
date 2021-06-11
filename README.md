# Lumia 640 RM-1073 Unbrick Guide.
Files and guide to unbrick the Microsoft Lumia 640 LTE (RM-1073)

Download the RM-1113 Emergency files: https://www.lumiafirmware.com/model/RM-1113/hwid/059X0Z0 // (Will be linked in the releases page)

Download the RM-1073 FFU: https://www.lumiafirmware.com/model/RM-1073

Download and install WDRT: http://go.microsoft.com/fwlink/p/?LinkId=522381

Download Windows Phone Internals: // (Will be linked in releases page)

Put the ffufile and emergency files in a folder.
Rename the ffufile to ffufile.ffu

Copy and paste thor2.exe from "C:\Program Files (x86)\Microsoft Care Suite\Windows Device Recovery Tool" // If on 64-bit Windows
                              "C:\Program Files\Microsoft Care Suite\Windows Device Recovery Tool" // If on 32-bit Windows
To the folder with the files.

Now open cmd as admin and run:

thor2 -mode emergency -hexfile MPRG8x26_fh.ede -edfile RM1113_fh.edp -ffufile ffufile.ffu

And wait for it to flash the bootloader and ffu.

When it is finished, run:

thor2 -mode rnd -bootnormalmode

If your device goes back to flash mode, Use Windows Phone Internals to flash the ffu again.
