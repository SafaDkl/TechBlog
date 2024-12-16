# allow to troubleshoot issues like network
# reason of disabling: creates performance issue and slow down network traffic.
#SD
troubleshootInstalls

# may affect required services for wifi
# reason of disabling: contains blutooth manager and wifi can expose the pc to threats
#SD
beWifiSafe

# can stop vpn from functionning
# reason of disabling: slow down the internet and contains possible threats
#SD
beVpnPppoeSafe

# google dns proved to be less secure comparing to cloudflare
# reason of disabling: contains vulnarabilities
#AKA
useGoogleDNS

# useful for setting Nvidia config, helps improve the display and the gaming experience overall
# reason of disabling: waste of space and can slow down the overall cpu performance
#AKA
installNvidiaControlPanel

# reason of disabling: waste of space and slows down the internet
#AKA
disableWindowsUpdates

# it removes the possibility of creating restore points if something go bad
# reason of disabling: waste of space
#AKA
disableSystemRestore

# it can increase the CPU usage and overhead, as it requires more processing power to compress and decompress the data. This can affect the performance and responsiveness of your system, especially if you have a slow CPU or a high load
# reason of disabling: exhaust the cpu from compression and decompression not to mention it exhaust the RAM
# can ifigure out a better way than how windows does it and look into the process(SD Explain it better)=>how valid?
disableNtfsCompression

# reason of disabling: just preference no clear answer to this one
# SD
legacyRightClicksMenu

# service that help older programs to run on windows the newer version and solve compatibility problems
# reason of disabling: the prog assume you donèt use old progs as they may contain security threats
# no
PcaSvc 

# control turning on and off radio devices like bluetooth or wifi
# reason of disabling: useless for security reasons
# no
RmSvc

# manager the wifi networks, connects and handles network profiles
# reason of disabling: can be exploited by hackers and put u at risk to connect to suspecious networks
# SD
WlanSvc

# reason of disabling: help free up disk space but you won't be able to revert your system to a previous state in case of problems like faulty updates, driver issues, or system instability.
# AKA
disableSystemRestore is on

# helps monitor and troubleshoot system performance and health.
# reason of disabling: waste of space
# no
DusmSvc

# responsible for managing and handling storage-related operations in SSD
# The service helps with:
# Managing storage devices and volumes.
# Implementing features like Storage Spaces, which combines multiple physical drives,
into a single virtual drive for redundancy or performance improvements.
Assisting in detecting and handling storage hardware failures.
# reason of disabling: waste of psace
# AKA (explain it better)
StorSvc

# primarily used for keeping track of the data consumed by the system over a network connection
# reason of disabling: waste of space
# no
Ndu

# Bluetooth service
# reason of disabling: potential security risk
# no
BthAvctpSvc

# responsible for managing graphical sessions and visual effects, such as window transparency, animations, and rendering
# reason of disabling: improve the performance
# In essence, the DispBrokerDesktopSvc
# service helps facilitate the smooth operation of desktop virtualization
# by managing the connection to the virtual desktop for users, allowing 
# them to work in remote or virtualized environments as if they were 
# working on a physical machine. It is part of Windows 10 and newer 
# versions, particularly in enterprise or remote work scenarios.
# AKA explain it better
DispBrokerDesktopSvc

# peer-to-peer update sharing
# The DoSvc service stands for Delivery Optimization Service in Windows. Its main purpose is to manage and optimize the delivery of updates, apps, and other content from Microsoft to your device. Specifically, it is used to download Windows updates and apps more efficiently by allowing your system to receive updates not just from Microsoft servers, but also from other devices on the local network or the internet.
# reason of disabling: improve the bandwith
# AKA explain it better
DoSvc

# monitors the applications you use most often and preloads them into RAM to speed up their launch times
# reason of disabling: slow down the RAM
# AKA
Sysmain

# discover file shares on the network
# reason of disabling: slow down the internet and decrease the performance and security issue
# no
SSDPSRV

# transfers files in the background using idle network bandwidth, allowing efficient, resume-able file downloads, typically used for Windows updates and app downloads. Disabling it can stop background updates and app downloads
# reason of disabling: waste of space and useless
# if windows update mini tool need it 
BITS

# altering these services can impact network functionality, file sharing, and other core operations related to system services
# reason of disabling: mainly disable because of the file sharing feature that raise potential threats to the user's data
# no
netsvcs

# help collecting data about Connected User Experiences and Telemetry
# reason of disabling: waste of space 
# no
DiagTrack

# he disabled all kind of logging to free up more disk space


# stands for the IP Helper Service in Windows. It provides support for IPv6 transition technologies, such as 6to4, ISATAP, and Teredo, and helps in the configuration of network interfaces.
# reason of disabling: waste of space and it doesn't affect normal network performance
# no
iphlpsvc

# reason of disabling: it removes displaying the network icon when the pc is locked so you can not switch to another network if you leave your pc alone
# no
DontDisplayNetworkSelectionUI

# reason of disabling: although it might slow down the DNS name resolution there is a risk of DNS Cache Poisoning and having old DNS records if it stays enabled
# no
flushDNS

# reason of disabling: improves the overall performance
# aka
disableWindowsSounds

**Windows Update**
**in order wumt able to work you should enable the below list of services**
UsoSvc
CryptSvc
WaaSMedicSvc
wuauserv
BITS
**revert auto update using this code**
RegChange "SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate" "NoAutoUpdate" "0" "Enabling automatic updates" "DWord"


