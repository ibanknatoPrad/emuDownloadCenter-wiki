## 1) Create downloadhook

First you need to create a downloadhook for the emulator, you do this by:

### 1.1)
Creating a folder in the downloadhooks folder, like: `downloadhooks\[emulatorfoldername]`

**Specifications:**
* **`emulatorfoldername`** has to be lowercase, no spaces or non-ascii characters (may only contain a 'minus' -)

### 1.2)
Create a **INFO INI** file in the `emulatorfoldername` wich contains basic information about the emulator.

The name of the INI file is: **`[emulatorfoldername]_info.ini`**

**Specifications:**
* **`emulatorfoldername`** has to be lowercase, no spaces or non-ascii characters (may only contain a 'minus' -)

So, for example you have a emulator called `johndoe` it is `downloadhooks\johndoe\johndoe_info.ini`

Ps. You can find templates over [here](https://github.com/PhoenixInteractiveNL/edc-masterhook/tree/master/downloadhooks/0_templates)

Contents of the INFO INI file:

    [INFO]
    InfoVersion	        = Version of the INI file layout.

    [EMULATOR]
    Author              = Author of the emulator.
    Contact             = Possible E-mail of the Author.
    License             = The License of the Emulator (Freeware/Shareware/Open Source/GPL).
    BiosNeeded          = Does the Emulator need BIOS ROMS to run?
    Website             = Website where the emulator can be found.
    Notes               = Small description of the emulator.

Example Contents (Emulator Potator for Watara Supervision):

    [INFO]
    InfoVersion         = 1.0.0.0

    [EMULATOR]
    Author              = David Raingeard
    Contact             = david*raingeard#laposte*net
    License             = Freeware
    BiosNeeded          = 0
    Website             = 
    Notes               = This appears to be the first Watara Supervision emulator for Windows. It uses the SDL library and has good compatibility.

Please note the Email is masked to prevent spamming (*=. | #=@)

### 1.3)
Create a **DOWNLOADS INI** file in the `emulatorfoldername` wich contains information about the emulator version(s).

The name of the INI file is: **`[emulatorfoldername]_downloads.ini`**

**Specifications:**
* **`emulatorfoldername`** has to be lowercase, no spaces or non-ascii characters (may only contain a 'minus' -)

So, for example you have a emulator called `johndoe` it is `downloadhooks\johndoe\johndoe_downlaods.ini`

Ps. You can find templates over [here](https://github.com/PhoenixInteractiveNL/edc-masterhook/tree/master/downloadhooks/0_templates)

Contents of the DOWNLOADS INI file:

    [0.7]
    EMU_Download                = The online location of the 7Z archive file (with ending slash /)
    EMU_ReleaseDate             = The releasedate of the emulator (if you cannot find it, use the date on the executable file)
    EMU_Notes                   = Some small emulator notes (Working / Not working)
    EMU_ExecutableFile          = Executable file to start the emulator (EXE/COM), please no CMD/BAT files.
    EMU_ExecutableFolder        = Path inside archive where executable file is located.
    EMU_OS                      = Operating system.
    EMU_OSVersion               = Version of the operating system, comma seperated. (example: XP,Vista,7,8,10)
    EMU_OSArchitecture          = Operating system architecture, comma seperated. (example: x86,x64)
    CFG_ECCParameter            = ECC parameter line.
    CFG_escape                  = Does the emulator needs the path in escapes? "" (default 1)
    CFG_win8char                = Does the emulator need old 8.3 dosnames to work? (1 for yes, otherwise leave blank)
    CFG_useCueFile              = Does the emulator needs a CUE file (possible in combination with script) to run? (1 for yes, otherwise leave blank)
    CFG_filenameOnly            = Does the emulator only needs the filename to run? (1 for yes, otherwise leave blank)
    CFG_noExtension             = Does the emulator only needs the filename to run without extension? (1 for yes, otherwise leave blank)
    CFG_executeInEmuFolder      = Does the emulator needs to be executed from withing the emulator folder? (1 for yes, otherwise leave blank)
    CFG_enableEccScript         = Does the emulator need a ECC script to start and run a ROM? (1 for yes, otherwise leave blank)
    CFG_enableZipUnpackActive   = Does the ROM archive need to be extracted first? (1 for yes, otherwise leave blank)
    CFG_enableZipUnpackSkip     = Skip already unpacked files (faster). (1 for yes, otherwise leave blank)
    INFO_PackedSize             = Packed size of the archive contents.
    INFO_UnpackedSize           = Unpacked size of the archive contents.
    INFO_CRC32Executable        = CRC32 of the executable to start the emulator.
    INFO_CRC32Archive           = CRC32 of the emulator archive.

Example Contents (Emulator Potator for Watara Supervision):

    [0.7]
    EMU_Download                = https://github.com/PhoenixInteractiveNL/edc-repo0001/raw/master/potator/
    EMU_ReleaseDate             = 2004-10-19
    EMU_Notes                   = Has a commandline parameter to start roms.
    EMU_ExecutableFile          = Potator.exe
    EMU_ExecutableFolder        =
    EMU_OS                      = Windows
    EMU_OSVersion               = XP,Vista,7,8,10
    EMU_OSArchitecture          = x86,x64
    CFG_ECCParameter            = %ROM%
    CFG_escape                  = 1
    CFG_win8char                =
    CFG_useCueFile              =
    CFG_filenameOnly            =
    CFG_noExtension             =
    CFG_executeInEmuFolder      =
    CFG_enableEccScript         = 
    CFG_enableZipUnpackActive   =
    CFG_enableZipUnpackSkip     =
    INFO_PackedSize             = 179 
    INFO_UnpackedSize           = 192 
    INFO_CRC32Executable        = 6C059FFB 
    INFO_CRC32Archive           = A8E52604

