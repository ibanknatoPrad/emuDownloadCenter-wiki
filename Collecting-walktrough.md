## 1) Create downloadhook

First you need to create a downloadhook for the emulator, you do this by:

### 1.1)
Creating a folder in the downloadhooks folder, like: `downloadhooks\[emulatorfoldername]`

**Specifications:**
* **`emulatorfoldername`** has to be lowercase, no spaces or non-ascii characters (may only contain a 'minus' -)

### 1.2)
Create a **INI** file in the `emulatorfoldername` wich contains basic information about the emulator.

The name of the INI file is: **`[emulatorfoldername]_info.ini`**

**Specifications:**
* **`emulatorfoldername`** has to be lowercase, no spaces or non-ascii characters (may only contain a 'minus' -)

So, for example you have a emulator called `johndoe` it is `downloadhooks\johndoe\johndoe_info.ini`
