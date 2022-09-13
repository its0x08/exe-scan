# Exe scan
### An experimental windows executable scanner that uses github-actions to process the input

These actions are used to statically scan executables automatically.
Below you can see an example output of the yara scan.

```
disable_dep [] [author="x0r",description="Bypass DEP",version="0.1"] input/mal.exe
keylogger [] [author="x0r",description="Run a keylogger",version="0.1"] input/mal.exe
Njrat2 [] [description="detect njRAT in memory",author="JPCERT/CC Incident Response Group",rule_usage="memory scan",hash1="d5f63213ce11798879520b0e9b0d1b68d55f7727758ec8c120e370699a41379d"] input/mal.exe
Njrat [RAT] [description="Njrat",author="botherder https://github.com/botherder"] input/mal.exe
NETexecutableMicrosoft [] [author="malware-lu"] input/mal.exe
IsPE32 [PECheck] [] input/mal.exe
IsNET_EXE [PECheck] [] input/mal.exe
IsWindowsGUI [PECheck] [] input/mal.exe
Microsoft_Visual_Studio_NET [PEiD] [] input/mal.exe
Microsoft_Visual_C_v70_Basic_NET_additional [PEiD] [] input/mal.exe
Microsoft_Visual_C_Basic_NET [PEiD] [] input/mal.exe
Microsoft_Visual_Studio_NET_additional [PEiD] [] input/mal.exe
Microsoft_Visual_C_v70_Basic_NET [PEiD] [] input/mal.exe
NET_executable_ [PEiD] [] input/mal.exe
NET_executable [PEiD] [] input/mal.exe
```

An example input file can be found [here](input/mal.exe) and the rules used for this project are listed below.
More rules are to be added in the future!
- [Yara-Rules](https://github.com/Yara-Rules/rules)

## Setup:

Go to repository **Settings** > **Secrets** > **Actions** > **New repository secret**

Name => EMAIL

Secret => Your email here.
