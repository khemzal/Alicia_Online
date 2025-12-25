# Setting up your own local development server for Story of Alicia
  Hi im writing this guide down as I struggled with following the HOWTORUN.md from (https://github.com/Story-Of-Alicia/alicia-server/tree/master) provided by the development team, because im not very competent. This guide is for Windows 10.

## Install Alicia
  1. install Alicia from one of the provided links from chrommds server site (https://bruhvrum.github.io/registertest/play.html) <br> <img width="954" height="187" alt="obrazek" src="https://github.com/user-attachments/assets/4a251e99-5550-418a-9fde-c17eb5910971" />
  2. Run the Story of Alicia Setup <br> <img width="340" height="89" alt="obrazek" src="https://github.com/user-attachments/assets/cdd199c0-79fa-411e-8eaf-19b20be54956" />
  3. You can now find the Alicia.exe file in ```C:\Users\_YOURUSERNAMEHERE_\AppData\Roaming\Story of Alicia\game```   (search %appdata% to open in folder search on Windows) <br> <img width="974" height="579" alt="obrazek" src="https://github.com/user-attachments/assets/6568b781-b81e-44f0-8a81-2a02ff66da35" />
## Installing the reqired dependencies
<img width="212" height="186" alt="obrazek" src="https://github.com/user-attachments/assets/dedf17c8-3ee7-476c-b9f1-5252d719dc70" />

### Github 
Most users do have Github installed and are logged in. However, if not, create an account on github.com and run the downloaded installer from https://desktop.github.com/download/. Make sure add GIT to Path is enabled. You can check by running Powershell and typing ```git --version``` <br> <img width="218" height="63" alt="obrazek" src="https://github.com/user-attachments/assets/beeedc76-5c4d-4ab4-867a-d3f06214bbea" />
### CMake
Go to https://cmake.org/download/ and follow the same process. Here is the list of copatible versions with Boost (https://stackoverflow.com/questions/42123509/cmake-finds-boost-but-the-imported-targets-not-available-for-boost-version)
Make sure Add CMAKE to Path is enabled. 
### A C++20 compatible compiler
Visual Studio 2019 and newer.
### Boost

Open up Powershell and type 
```cd C:\Users\_YOURUSERNAMEHERE_ <br>```
```git clone https://github.com/microsoft/vcpkg.git```<br>
```cd C:\Users\_YOURUSERNAMEHERE_\vcpkg```<br>
```bootstrap-vcpkg.bat```<br>
Now you should have ```cd C:\Users\_YOURUSERNAMEHERE_\vcpkg\vcpkg.exe``` <br><img width="715" height="670" alt="obrazek" src="https://github.com/user-attachments/assets/452c0370-9ec7-4a2e-b1e8-17b47d9929c0" /> <br>
```vcpkg integrate install```<br>

In a new Powershell window
```cd C:\Users\_YOURUSERNAMEHERE_\vcpkg```<br>
```vcpkg install boost``` (if you are using Command line type ```./vcpkg install boost```) <br>

Go to https://original.boost.org/users/download/ and download the .zip or .7z file. Exctract it. Open C:\Program Files on the side. Go inside of the extracted file and from there move the boost folder over to the Program Files directory.  

### libpq
PostgreSQL comes vwith libpq.
Download and [https://www.postgresql.org/docs/current/libpq.html](https://www.postgresql.org/download/). Run the installer. Choose your own password for the superuser. Keep the port at 5432. Keep the locale to default. You can close the Stack Builder, we dont need it. <br>
Add PostgreSQL to PATH by running Windows key + R and typing sysdm.cpl<br> 
<img width="1489" height="557" alt="obrazek" src="https://github.com/user-attachments/assets/197c8136-9d0f-406e-9818-96845ca07b48" />



