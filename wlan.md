## Wireless LAN
### Abstract
The WLAN API recommendations are:
- cfg80211 driver for WLAN
- hostapd, wpa_supplicant, and iw support with WLAN management frames transmitted via nl80211

### Scope
The primary focus is the control interface to radio and access point functionality, with STA (client) functionality as a lower priority. The data path is generally not a problem, as all known existing drivers model this as a Linux Ethernet device.
Availability of source code, and the license of, the device driver, microcode, and any firmware on an embedded offloaded processor, are out of scope.
The operating system scope is limited to Linux.

### Recommended APIs
Vendor-specific extensions should be limited to hardware or implementation specific functionality that is distinctly not present in cfg80211, and does not lend itself to an extension of cfg80211 either.
Examples are control of embedded firmware, debugging interfaces to the lower layers of the implementation, and special calibration logic. Any interfaces that must be used by an operational control interface should be standardized. The recommended interface for vendor-specific extensions is cfg80211 vendor commands.

### Next Steps
#### Basic profile definition
- Define a set of features and perform dedicated analysis
- Align with participants and members on roles and responsibilities
- Have a dedicated project team to continue with the project planning and developments
- Plan and align on Testing and Certification (currently under internal alignment)

#### RDK-B harmonization
- Define and develop a unified Wi-Fi HAL to be used below the RDK-B HAL (under alignment with major RDK-B operators)
- Work closely with RDK-B members and get support to access CCSPWiFiHAL and involvements and commitments on the evolution on the new Wi-Fi HAL
- Plan and align on Testing and Certification (currently under internal alignment)

#### EasyMesh (Multi-AP)
- Wi-Fi Alliance (WFA) has released a specification of a protocol to communicate between Wi-Fi extenders
- Work closely with prpl members, WFA members and Broadband Forum (BBF) members, to drive improvements on the functionalities targeted on this specification
- Create an open source reference implementation based on the first WFA specification and continue with its evolution.
