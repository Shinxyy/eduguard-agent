## Compiling the custom Wazuh image which turns into Eduguard.

1. Run the docker and compile the project in the docker with the provided Dockerfile.
2. When the compilation is done make sure to zip the complete directory, so that you have a zip file containing the whole project called eduguard_v1.zip for example.
3. Start your windows VM with WIX toolset, .NET framework 3.5.1 and Microsoft Windows SDK installed.
4. Copy the eduguard_v1.zip into the vm.
5. Unzip the file and store it somewhere you like.
5. Open an administrator powershell window and navigate to the folder.
6. Now we are going to create an .msi installer, execute these commands:
- cd wazuh-4.12.0\src\win32
- .\wazuh-installer-build-msi.bat
7. When this is done you can find the .msi in the wazuh-4.12.0\src\win32 folder.

### References
https://documentation.wazuh.com/current/deployment-options/wazuh-from-sources/wazuh-agent/index.html
