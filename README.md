Fips Build For OpenSSL

## Step 0: Prerequisites

0. Windows 7 Recommended with 32 Bit
1. Programming languages\Visual C++\Common Tools for Visual C++ 2015; You may download Visual C++ 2015/2017 Build Tools from here http://landinghub.visualstudio.com/visual-cpp-build-tools
2. Open Visual C++ Build Tools
3. Perl should be installed and location shoule be added in PATH system variable like: 'C:\Perl32\bin'. Also you may download pearl from here https://www.activestate.com/activeperl/downloads (if needed)
4. NASM (Netwide Assembler) installed and location should be added to the PATH system variable like: 'C:\Program Files\NASM' [After adding PATH, you may require to reopen your command prompt or reload environment variables]. Also may download from here https://sourceforge.net/projects/nasm/ (if needed)

## Step 1: Build the FIPS Object Module from Source

### Download FIPS Module and Compile:
1. Download openssl-fips-2.0.16.tar.gz from: here https://www.openssl.org/source/
2. Extract/Unzip downloaded file in some directory; like we are creating here `openssl-fips-2.0.16`
3. Open a VC++ or `VS2013 x86 Native Tools Command Prompt` to execute commands
4. Go to into extracted directory, then execute following command in your command prompt

> cd ..\openssl-fips-2.0.16\
..\openssl-fips-2.0.16> Set PROCESSOR_ARCHITECTURE=x86
..\openssl-fips-2.0.16> ms\do_fips

Follow screen instructions and done.

4. After getting a message of `FIPS BUILD SUCCESS`, you may find generated files in below directory:

..\openssl-fips-2.0.16>	 `C:\usr\local\ssl\fips-2.0`

You have successfully generated a build of FLIPS for OpenSSL.

#### Note: 
- You will have following files in C:\usr\local\ssl\fips-2.0\lib directory on build success: `fipscanister.lib`, `fipscanister.lib.sha1` and `fips_premain.c`.
