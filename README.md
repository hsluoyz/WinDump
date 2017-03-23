# WinDump for Npcap

[![Release](https://img.shields.io/github/release/hsluoyz/windump.svg)](https://github.com/hsluoyz/windump/releases)
![License](https://img.shields.io/github/license/hsluoyz/windump.svg)
![Downloads](https://img.shields.io/github/downloads/hsluoyz/windump/latest/total.svg)
![TotalDownloads](https://img.shields.io/github/downloads/hsluoyz/windump/total.svg)

A user-mode packet dump software based on [Npcap](https://github.com/nmap/npcap). It's a fork of the [original WinDump](http://www.winpcap.org/windump/).

# Build

1. Get the latest [Npcap SDK](https://github.com/nmap/npcap#development-kit).
2. Build ``win32\prj\WinDump.sln`` with **Visual Studio 2013** or later.
3. **Note**: in this MSVC project, the Npcap SDK is pointing to ``J:\npcap\npcap-sdk``, you may need to adjust this setting to your own Npcap SDK location.

# Releases

https://github.com/hsluoyz/WinDump/releases

# Usage

Get the list of interfaces:
```
J:\github_repos\WinDump\win32\prj\Win32\Release>WinDump.exe -D
1.\Device\NPF_{9ADACD44-ECFF-45E2-BD5E-3491DEBA711F} (NdisWan Adapter)
2.\Device\NPF_{8A300A14-CA5A-4A3C-B52B-7516661B4CDA} (NdisWan Adapter)
3.\Device\NPF_{44DB6B7A-661D-4FA3-925E-6287EA48D3F6} (NdisWan Adapter)
4.\Device\NPF_{F0353155-69D0-4611-AB2A-EE864BE0ADD9} (Microsoft)
5.\Device\NPF_{385F30D0-9166-45D3-BBC6-F1D9C5300AF9} (Microsoft)
```

Capture on an interface:

```
J:\github_repos\WinDump\win32\prj\Win32\Release>WinDump.exe -i5
WinDump.exe: listening on \Device\NPF_{385F30D0-9166-45D3-BBC6-F1D9C5300AF9}
23:09:29.711696 IP AkiSn0w-PC.14468 > 125.33.6.205.2123: UDP, length 37
23:09:29.711801 IP AkiSn0w-PC.14468 > 125.33.6.205.2123: UDP, length 1428
23:09:29.711867 IP AkiSn0w-PC.14468 > 125.33.6.205.2123: UDP, length 1428
23:09:29.711893 IP AkiSn0w-PC.14468 > 125.33.6.205.2123: UDP, length 1428
23:09:29.715645 IP AkiSn0w-PC.60784 > AkiSn0w-PC.53:  45922+ PTR? 205.6.33.125.in-addr.arpa. (43)
23:09:29.721960 IP AkiSn0w-PC.61696 > AkiSn0w-PC.53:  2523+ A? dc.services.visualstudio.com. (46)
23:09:29.722197 IP AkiSn0w-PC.53 > AkiSn0w-PC.60784:  45922 NXDomain 0/1/0 (97)
23:09:29.722198 IP 105.92.9.221.adsl-pool.jlccptt.net.cn.46313 > AkiSn0w-PC.14468: UDP, length 48
23:09:29.722198 IP 105.92.9.221.adsl-pool.jlccptt.net.cn.46313 > AkiSn0w-PC.14468: UDP, length 100
23:09:29.722198 IP 105.92.9.221.adsl-pool.jlccptt.net.cn.46313 > AkiSn0w-PC.14468: UDP, length 99
23:09:29.722464 IP AkiSn0w-PC.14468 > 105.92.9.221.adsl-pool.jlccptt.net.cn.46313: UDP, length 322
23:09:29.722546 IP AkiSn0w-PC.14468 > 105.92.9.221.adsl-pool.jlccptt.net.cn.46313: UDP, length 1439
23:09:29.722564 IP
```

For other advanced usage, please refer to [WinDump docs](http://www.winpcap.org/windump/docs/default.htm).

# How to use Npcap first when Npcap and WinPcap coexist?

Please refer to [Npcap docs](https://rawgit.com/nmap/npcap/master/docs/npcap-guide-wrapper.html#npcap-feature-native).


