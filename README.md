# ms17010-nsa-EternalBlue
integration ms17010 and nsa-EternalBlue

��Ҫ����nsa������֮����ms17010ϵ��poc��
����֮��poc��windows 7/2008 �� windows 8/2012 x64
ms17010 ����win all��Windows Vista���¿��������ɹ���ȡsystemȨ�ޣ�
vista��������Ҫ �����ܵ� ����Ȩ�ޣ�һ����Ҫ���û�Ȩ�ޡ�

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
						
���ڣ�https://github.com/worawit/MS17-010 

