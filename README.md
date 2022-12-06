# Not needed for current versions!

The most recent versions do not require this patch and the program starts fine without IBS instructions.

This project is therefore archived.


# ryzen-master-vbs-patch

AMD Ryzen Master VBS patcher allows AMD Ryzen Master to run while Hyper-V Virtualization is enabled.


Thanks to [@TOM_RUS](https://twitter.com/TOM_RUS/status/1204867886197755904) for finding this.

This patch disables the VBS check on startup. It does NOT fix what might be the cause of this being disabled.

This MAY break functionality and it MAY stop working on future versions.

This has been confirmed to work on the versions listed below so versions inbetween are likely fine as well. 
The exact version does not have to match, but if AMD changes the code for detection it will likely break.

Confirmed versions:

 * v2.1.0.1424 (2019)
 * v2.1.1.1472 (2020)
 * v2.2.0.1543 (2020)
 * v2.3.0.1591 (2020)
 * v2.6.0.1692 (2020)
 * v2.6.2.1818 (2021)
 * v2.8.0.1937 (2021)

Threadripper patch was supplied by [@neoKushan](https://github.com/neoKushan).
Ryzen 1000 series patch was supplied by [@kaelanduck](https://github.com/kaelanduck).

# Running

Various parts of this will require administrator access.

* Download and unzip binary from [releases](https://github.com/klauspost/ryzen-master-vbs-patch/releases).
* Copy `AMD Ryzen Master.exe` from `c:\Program Files\AMD\RyzenMaster\bin\` or where your software is installed.
* In Explorer Drag & Drop `AMD Ryzen Master.exe` to the same location as the unzipped`ryzen-master-vbs-patch.exe`
* Run the `ryzen-master-vbs-patch.exe`
* If successful `patched-AMD Ryzen Master.exe` should now be created.
* Copy this back to the `RyzenMaster` folder.
* Rename your existing `AMD Ryzen Master.exe` to `AMD Ryzen Master BACKUP.exe` or similar.
* Rename `patched-AMD Ryzen Master.exe` to `AMD Ryzen Master.exe`.

From the commandline, the syntax is:

```
 Usage: ryzen-master-vbs-patch [-p=patched] "AMD Ryzen Master.exe"
   -p string
         Specify prefix for output file. Set to "", overwrite input. (default "patched-")
```

# Building 

Requires Go SDK  installed.

In the source directory, use regular go build command to build the executable:

```bash
go build .
```

# License

```
The MIT License (MIT)

Copyright (c) 2020 Klaus Post

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
