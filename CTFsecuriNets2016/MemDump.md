#Solution - Forensics 90 Points
memdump.mem

      We Can Check The File Using file or Strings or hexdump or xxd To Get Some Informations About File
      This Memory Dump We Can Investigat it, I've Found A Solution Using Volatility Forensics Framework
      With Volatility We Can Extract All Precess And Dll's And Administrator Password .......
      
      ./volatility -f memdump.mem --profile=WinXPSP2x86 psscan
      ./volatility -f memdump.mem --profile=WinXPSP2x86 pslist
      ./volatility -f memdump.mem --profile=WinXPSP2x86 dlllist
      .....
      
      Sorry For This Short Writeup because Players CTF Have Not Problem To Use Volatility FrameWork
      
      In This Challenge The Flag Like a KeyLogger Name Thats Why Nothing Seeying In Process list 
      We Can Scan Command Line To Get Keylogger : who_names_keyloggers_like_this.exe
      
![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/CTFsecuriNets2016/90FORENSICS.png)
  

        Flag Is : who_names_keyloggers_like_this
        Warm Regards,
        By 
![alt tag](https://github.com/MrMugiwara/MrMugiwara.github.io/blob/master/images/Mr.Mugiwara.jpg)

