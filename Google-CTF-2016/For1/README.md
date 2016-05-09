# GOOGLE CTF 2016
https://capturetheflag.withgoogle.com/          
#Forensics - For1  100 Points

          We Can Check The File Using file or Strings or hexdump or xxd To Get Some Informations About File
          This Memory Dump We Can Investigat it Using Volatility Or Rekal Or Any Memory Forensics Framework
          I've Found A Solution Using Rekal Framework

# Solution Using Volatility FrameWork
# imageinfo
![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/Google-CTF-2016/For1/volinfo.png)
# pslist
![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/Google-CTF-2016/For1/volist.png)
# pstree
![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/Google-CTF-2016/For1/voltree.png)
# mspaint.exe is the process we go To dump it using memdump Argument On Volatility
# memdump & Rename The output From 4092.dmp to 4092.data 
![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/Google-CTF-2016/For1/voldata.png)
# And Final Step We Can Open The Data As Picture And Modify Type 2 The alpha RVB to Get The Flag :
![alt tag](https://github.com/MrMugiwara/WriteupsCTF/blob/master/Google-CTF-2016/For1/Fl.png)

      Flag Is :  CTF{HeRe_GoEs_thE_FLaG}
      Regards, By
![alt tag](https://github.com/MrMugiwara/MrMugiwara.github.io/blob/master/images/Mr.Mugiwara.jpg)
 

