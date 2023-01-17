# Prerequisite for Windows

## MinGW Installation

### Download MinGW-W64

The download site

> [https://sourceforge.net/projects/mingw-w64/files/mingw-w64/](https://sourceforge.net/projects/mingw-w64/files/mingw-w64/)

Download "x86\_64-posix-seh" of "MinGW-W64 GCC-8.1.0"

Then, named "x86\_64-8.1.0-release-posix-seh-rt\_v6-rev0.7z" file should be on your local side.

> x86\_64-8.1.0-release-posix-seh-rt\_v6-rev0.7z

<figure><img src="../../../../.gitbook/assets/image (3) (3).png" alt=""><figcaption><p>x86_64-posix-seh</p></figcaption></figure>

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

### Download Git BASH

The download site

> [https://gitforwindows.org/](https://gitforwindows.org/)

<figure><img src="../../../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Download Git BASH</p></figcaption></figure>

The download file name

> Git-x.xx.x.x-64-bit.exe

### Install Git BASH

Install Git BASH as default option clicking "NEXT" button.

### Install make

Go to the below site

> [https://gist.github.com/evanwill/0207876c3243bbb6863e65ec5dc3f058](https://gist.github.com/evanwill/0207876c3243bbb6863e65ec5dc3f058)

Go to the ezwinports site clicking below or "ezwinprts".

> [https://sourceforge.net/projects/ezwinports/files/](https://sourceforge.net/projects/ezwinports/files/)

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption><p>How to add more to Git Bash on Windows</p></figcaption></figure>

Download "make" file named below

> make-4.x-without-guile-w32-bin.zip

Extract zip. The extracted folder name of the zip file should be "mingw64".&#x20;

Copy the contents to below path merging the folders, but do NOT overwrite/replace any existing files.

> C:\Program Files\Git\mingw64

### Execute Git BASH

<figure><img src="../../../../.gitbook/assets/image.png" alt=""><figcaption><p>Git Bash</p></figcaption></figure>

