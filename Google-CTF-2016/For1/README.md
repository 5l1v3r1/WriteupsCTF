# GOOGLE CTF 2016
#Forensics - For1  100 Points

                    We Can Check The File Using file or Strings or hexdump or xxd To Get Some Informations About File
                    This Memory Dump We Can Investigat it Using Volatility Or Rekal Or Any Memory Forensics Framework
                    I've Found A Solution Using Rekal Framework

          rekal -f dump1.raw
      [1] dump1.raw 00:19:31> pslist()
        _EPROCESS            Name          PID   PPID   Thds    Hnds    Sess  Wow64           Start                     Exit          
      -------------- -------------------- ----- ------ ------ -------- ------ ------ ------------------------ ------------------------
      0xe00032553780 System                   4      0    126        -      - False  2016-04-04 16:12:33+0000 -                       
      0xe00033f1f780 sihost.exe              92    796     10        -      1 False  2016-04-04 16:12:37+0000 -                       
      0xe0003389c040 smss.exe               268      4      2        -      - False  2016-04-04 16:12:33+0000 -                       
      0xe000349285c0 taskhostw.exe          332    796     10        -      1 False  2016-04-04 16:17:40+0000 -                       
      0xe0003381b080 csrss.exe              344    336      8        -      0 False  2016-04-04 16:12:33+0000 -                       
      0xe000325ba080 wininit.exe            404    336      1        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000325c7080 csrss.exe              412    396      9        -      1 False  2016-04-04 16:12:34+0000 -                       
      0xe00033ec6080 winlogon.exe           460    396      2        -      1 False  2016-04-04 16:12:34+0000 -                       
      0xe00033efb440 services.exe           484    404      3        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe00033f08080 lsass.exe              492    404      6        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe00033ec5780 svchost.exe            580    484     16        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe00034377780 svchost.exe            608    484     17        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe00034202280 svchost.exe            612    484      9        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe00034ade080 svchost.exe            628    484      1        -      1 False  2016-04-04 16:14:43+0000 -                       
      0xe000341cb640 dwm.exe                712    460      8        -      1 False  2016-04-04 16:12:34+0000 -                       
      0xe00034222780 svchost.exe            796    484     45        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000342a7780 VBoxService.ex         828    484     10        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000342ad780 svchost.exe            844    484      8        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000342c0080 svchost.exe            852    484      6        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000342dd780 svchost.exe            892    484     18        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000342bc780 svchost.exe            980    484     17        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000343e7780 spoolsv.exe           1072    484      8        -      0 False  2016-04-04 16:12:34+0000 -                       
      0xe000343e9780 svchost.exe           1092    484     23        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe0003442a780 rundll32.exe          1148    796      1        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe00034494780 CompatTelRunne        1224   1148      9        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe00034495780 svchost.exe           1276    484     10        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe0003259b3c0 taskhostw.exe         1532    796      9        -      1 False  2016-04-04 16:12:37+0000 -                       
      0xe0003461d780 svchost.exe           1564    484      5        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe000345da780 wlms.exe              1616    484      2        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe00034623780 MsMpEng.exe           1628    484     24        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe00034b08780 OneDrive.exe          1692   2336     10        -      1 True   2016-04-04 16:12:55+0000 -                       
      0xe00033e00780 svchost.exe           1772    484      3        -      0 False  2016-04-04 16:12:37+0000 -                       
      0xe000343b2340 cygrunsrv.exe         1832    484      4        -      0 False  2016-04-04 16:12:35+0000 -                       
      0xe0003479b780 cygrunsrv.exe         1976   1832      0        -      0 False  2016-04-04 16:12:36+0000 2016-04-04 16:12:36+0000
      0xe000347aa780 conhost.exe           2004   1976      2        -      0 False  2016-04-04 16:12:36+0000 -                       
      0xe0003472b080 notepad.exe           2012   2336      1        -      1 False  2016-04-04 16:14:49+0000 -                       
      0xe000347c1080 sshd.exe              2028   1976      3        -      0 False  2016-04-04 16:12:36+0000 -                       
      0xe000339d4340 NisSrv.exe            2272    484      6        -      0 False  2016-04-04 16:12:38+0000 -                       
      0xe000336e8780 userinit.exe          2312    460      0        -      1 False  2016-04-04 16:12:38+0000 2016-04-04 16:13:04+0000
      0xe000336e3780 explorer.exe          2336   2312     31        -      1 False  2016-04-04 16:12:38+0000 -                       
      0xe0003374f780 RuntimeBroker.        2456    580      6        -      1 False  2016-04-04 16:12:38+0000 -                       
      0xe00033a39080 SearchIndexer.        2664    484     13        -      0 False  2016-04-04 16:12:39+0000 -                       
      0xe00033a79780 ShellExperienc        2952    580     41        -      1 False  2016-04-04 16:12:39+0000 -                       
      0xe000349e4780 WmiPrvSE.exe          3032    580      6        -      0 False  2016-04-04 16:16:37+0000 -                       
      0xe00033b57780 SearchUI.exe          3144    580     38        -      1 False  2016-04-04 16:12:40+0000 -                       
      0xe000348c6780 VBoxTray.exe          3324   2336     10        -      1 False  2016-04-04 16:12:55+0000 -                       
      0xe00033e1d780 DismHost.exe          3636   1224      2        -      0 False  2016-04-04 16:12:47+0000 -                       
      0xe000348e9780 svchost.exe           3992    484      6        -      0 False  2016-04-04 16:12:52+0000 -                       
      0xe00034b0f780 mspaint.exe           4092   2336      3        -      1 False  2016-04-04 16:13:21+0000 -                       
           Out<1> Plugin: pslist

                    In Last Line We Can See mspaint.exe PID 4092 Let's Try To See More About This Process 

                  [1] dump1.raw 00:19:59> pstree()
      _EPROCESS                                 PPid   Thds   Hnds            Time          
      ---------------------------------------- ------ ------ ------ ------------------------
        0xe0003381b080 csrss.exe (344)            336      8      - 2016-04-04 16:12:33+0000
        0xe000325ba080 wininit.exe (404)          336      1      - 2016-04-04 16:12:34+0000
      . 0xe00033efb440 services.exe (484)         404      3      - 2016-04-04 16:12:34+0000
      .. 0xe00033ec5780 svchost.exe (580)         484     16      - 2016-04-04 16:12:34+0000
      ... 0xe0003374f780 RuntimeBroker. (2456)    580      6      - 2016-04-04 16:12:38+0000
      ... 0xe00033a79780 ShellExperienc (2952)    580     41      - 2016-04-04 16:12:39+0000
      ... 0xe000349e4780 WmiPrvSE.exe (3032)      580      6      - 2016-04-04 16:16:37+0000
      ... 0xe00033b57780 SearchUI.exe (3144)      580     38      - 2016-04-04 16:12:40+0000
      .. 0xe00034377780 svchost.exe (608)         484     17      - 2016-04-04 16:12:34+0000
      .. 0xe00034202280 svchost.exe (612)         484      9      - 2016-04-04 16:12:34+0000
      .. 0xe00034ade080 svchost.exe (628)         484      1      - 2016-04-04 16:14:43+0000
      .. 0xe00034222780 svchost.exe (796)         484     45      - 2016-04-04 16:12:34+0000
      ... 0xe00033f1f780 sihost.exe (92)          796     10      - 2016-04-04 16:12:37+0000
      ... 0xe000349285c0 taskhostw.exe (332)      796     10      - 2016-04-04 16:17:40+0000
      ... 0xe0003442a780 rundll32.exe (1148)      796      1      - 2016-04-04 16:12:35+0000
      .... 0xe00034494780 CompatTelRunne (1224)   1148      9      - 2016-04-04 16:12:35+0000
      ..... 0xe00033e1d780 DismHost.exe (3636)   1224      2      - 2016-04-04 16:12:47+0000
      ... 0xe0003259b3c0 taskhostw.exe (1532)     796      9      - 2016-04-04 16:12:37+0000
      .. 0xe000342a7780 VBoxService.ex (828)      484     10      - 2016-04-04 16:12:34+0000
      .. 0xe000342ad780 svchost.exe (844)         484      8      - 2016-04-04 16:12:34+0000
      .. 0xe000342c0080 svchost.exe (852)         484      6      - 2016-04-04 16:12:34+0000
      .. 0xe000342dd780 svchost.exe (892)         484     18      - 2016-04-04 16:12:34+0000
      .. 0xe000342bc780 svchost.exe (980)         484     17      - 2016-04-04 16:12:34+0000
      .. 0xe000343e7780 spoolsv.exe (1072)        484      8      - 2016-04-04 16:12:34+0000
      .. 0xe000343e9780 svchost.exe (1092)        484     23      - 2016-04-04 16:12:35+0000
      .. 0xe00034495780 svchost.exe (1276)        484     10      - 2016-04-04 16:12:35+0000
      .. 0xe0003461d780 svchost.exe (1564)        484      5      - 2016-04-04 16:12:35+0000
      .. 0xe000345da780 wlms.exe (1616)           484      2      - 2016-04-04 16:12:35+0000
      .. 0xe00034623780 MsMpEng.exe (1628)        484     24      - 2016-04-04 16:12:35+0000
      .. 0xe00033e00780 svchost.exe (1772)        484      3      - 2016-04-04 16:12:37+0000
      .. 0xe000343b2340 cygrunsrv.exe (1832)      484      4      - 2016-04-04 16:12:35+0000
      ... 0xe0003479b780 cygrunsrv.exe (1976)    1832      0      - 2016-04-04 16:12:36+0000
      .... 0xe000347aa780 conhost.exe (2004)     1976      2      - 2016-04-04 16:12:36+0000
      .... 0xe000347c1080 sshd.exe (2028)        1976      3      - 2016-04-04 16:12:36+0000
      .. 0xe000339d4340 NisSrv.exe (2272)         484      6      - 2016-04-04 16:12:38+0000
      .. 0xe00033a39080 SearchIndexer. (2664)     484     13      - 2016-04-04 16:12:39+0000
      .. 0xe000348e9780 svchost.exe (3992)        484      6      - 2016-04-04 16:12:52+0000
      . 0xe00033f08080 lsass.exe (492)            404      6      - 2016-04-04 16:12:34+0000
        0xe000325c7080 csrss.exe (412)            396      9      - 2016-04-04 16:12:34+0000
        0xe00033ec6080 winlogon.exe (460)         396      2      - 2016-04-04 16:12:34+0000
      . 0xe000341cb640 dwm.exe (712)              460      8      - 2016-04-04 16:12:34+0000
      . 0xe000336e8780 userinit.exe (2312)        460      0      - 2016-04-04 16:12:38+0000
      .. 0xe000336e3780 explorer.exe (2336)      2312     31      - 2016-04-04 16:12:38+0000
      ... 0xe00034b08780 OneDrive.exe (1692)     2336     10      - 2016-04-04 16:12:55+0000
      ... 0xe0003472b080 notepad.exe (2012)      2336      1      - 2016-04-04 16:14:49+0000
      ... 0xe000348c6780 VBoxTray.exe (3324)     2336     10      - 2016-04-04 16:12:55+0000
      ... 0xe00034b0f780 mspaint.exe (4092)      2336      3      - 2016-04-04 16:13:21+0000
        0xe00032553780 System (4)                   0    126      - 2016-04-04 16:12:33+0000
      . 0xe0003389c040 smss.exe (268)               4      2      - 2016-04-04 16:12:33+0000
                 Out<2> Plugin: pstree

                                        #Dump Procees For msfpaint.exe
                [1] dump1.raw 00:20:41> memdump(pid=4092)
      **************************************************
      Writing mspaint.exe 0xe00034b0f780 mspaint.exe  4092 to mspaint.exe_4092.dmp
                 Out<3> Plugin: memdump                      

                                        #Now We Can Rename mspaint.exe_4092.dmp To mspaint.exe_4092.data 
               [1] dump1.raw 00:26:09> mv  mspaint.exe_4092.dmp mspaint.exe_4092.data

                                        #Using Gimp We Can Resolve This Challenge To Get The Flag
                    Screenshot Gimp.png
  ![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/Google-CTF-2016/For1/gimp.png)
We Can See The Flag Is Reversed  :  CTF{HeRe_GoEs_thE_FLaG}
  ![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/Google-CTF-2016/For1/For1.png)

Flag Is :  CTF{HeRe_GoEs_thE_FLaG}<br>
Regards,<br>
By Soufiane Boussali

