# Prerequisite for Windows

## MinGW Installation

### Download MinGW-W64

The download site : [https://sourceforge.net/projects/mingw-w64/files/mingw-w64/](https://sourceforge.net/projects/mingw-w64/files/mingw-w64/)

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption><p>x86_64-posix-seh</p></figcaption></figure>

Download "x86\_64-posix-seh" of "MinGW-W64 GCC-8.1.0"

Then, named "x86\_64-8.1.0-release-posix-seh-rt\_v6-rev0.7z" file should be on your local side.

> x86\_64-8.1.0-release-posix-seh-rt\_v6-rev0.7z

### Extract "7z" file

Extract the "7z" file, then "mingw64" folder should be existed on your local disk.

> mingw64

Copy and paste the extracted folder into "C:\Program Files".

> C:\Program Files\mngw64

### Set Windows System Environment variables

Set "C:\Program Files\mingw64\bin" at System Variables and User Variables on Windows.

> C:\Program Files\mingw64\bin

You can check the version of GCC on windows command prompt.

> C:>gcc --version

<figure><img src="../../../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Version of GCC</p></figcaption></figure>



## Git for Windows

