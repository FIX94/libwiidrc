# libwiidrc
This is only usable with a sepcial patched fw.img and homebrew injected into a wiiu vc title, details on the patches are below.  
The usage is quite simple, call WiiDRC_Init on boot and after that call WiiDRC_ScanPads every time you update your pad inputs.  
See the "demo" folder for an example on how to use it in a bit more detail.  
Both compiled Library and Demo can be grabbed from the Releases tab.    

# Patches
Right now the only patches that'll make it work are for the fw.img r590 (crc32 e2f27e9b) and are as follows:  
offset 0x1478A from 0x6818 to 0x2000 (wiimote passthrough)  
offset 0x115C2 from 2800D00349022209F004FF1D to F004FF2148022109F004FEF9 (custom function)  
offset 0x14E92 from F001FAB9 to F7FCFB95 (jump to custom function)  
offset 0x17A880 from 0x2000 to 0x2001 (to disable ahbprot)  
offset 0x17E81C from 0x2201 to 0x2200 (to disable memprot)  
