### 1-1 �إߤT�ӥΤ�A�b���W�٤��O���G examuser1, examuser2, examuser3 �A�P�ɤT�ӥΤ᪺�K�X���O�y ItIsExam �z  
     
 useradd �b��   
 passwd �b��    
 ��J�K�X      
![1](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/1.png?raw=true)  
 
### 1-2 �ЧR���t�Τ��� examuser3 �o�ӱb���A�P�ɱN�o�ӱb�����a�ؿ��P�l���ɮצP�B�R��   
 
 userdel -r examuser3  
![2](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/2.png?raw=true)  
 
### 1-3 examuser1 ���p�߳Q�޲z���R���F�A���O�o�ӱb�����a�ؿ��P�����l���٦s�b�C�аѦҳo�ӱb���i�઺�a�ؿ��ҫO�d�� UID �P GID�A �ù��եH�ӱb���즳�� UID/GID ��T�ӭ��ظӱb���C�ӳo�ӱb�����K�X�е��� ItIsExam ���˦�  
   
 userdel examuser1  
 ll /home/ �|�ݨ�1001    
 useradd -u 1001 -U examuser1     
![3](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/3.png?raw=true) 
 
### 2-1 �إ�examuser4�ϥΪ̱b���A�K�X���N 
 
  useradd �b��   
  passwd �b��   
  ��J�K�X    
![4](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/4.png?raw=true)  
 
### 2-2 �ϥ� root �N /etc/securetty �ƻs�� examuser4�A�B�o�ӱb���n�������ϥθ��ɮפ~��  
#### �ƻs     
  cp /etc/securetty /home/examuser4     
  cd examuser4      
  ls �|�ݨ�securetty    
![5](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/5.png?raw=true) 
   
#### ����v��    
  ������root su - root     
  chmod u=rwx,g=rwx,o=rwx /home/examuser4/securetty       
![6](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/6.PNG?raw=true) 
 
### 2-3 �إߤ@�ӦW�� /examdata/change.txt �����ɮסA�o���ɮת��֦��̬� sshd�A�֦��s�լ� users�Asshd �iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v���C�B�o���ɮת��ק����нվ㦨 2012 �~ 12 �� 21 �� (������T�Y�i�A�ɶ��H�K) 
 
  cd /      
  mkdir examdata     
  cd examdata      
  ls �d���ɮ�    
  touch change.txt    
  ll �d���v��     
  �o���ɮת��֦��̬� sshd:chown sshd change.txt      
  �֦��s�լ� users:chgrp users change.txt       
  sshd �iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v��:chmod u=rw,q=r,0= change.txt      
  ll �T�{         
![7](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/7.PNG?raw=true) 

#### �ק����нվ㦨 2012 �~ 12 �� 21 �� touch -t 201212210000 change.txt        
  ll�T�{               
![8](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/8.PNG?raw=true) 
 
### 3-1 �Шϥ� root �������إߩ��U���ɮ׻P�v���G              
 drwxrwxr-x  root root /dev/shm/unit05/    
 drwxr-xr--  root root /dev/shm/unit05/dir1/       
 -rw-r--r--  root root /dev/shm/unit05/dir1/file1 (�ƻs�Ӧ� /etc/hosts)         
 drwxr-x--x  root root /dev/shm/unit05/dir2/            
 -rw-r--r--  root root /dev/shm/unit05/dir2/file2 (�ƻs�Ӧ� /etc/hosts)         
 drwxr-xr-x  root root /dev/shm/unit05/dir3/           
 -rw-rw-rw-  root root /dev/shm/unit05/dir3/file3 (�ƻs�Ӧ� /etc/hosts)       
 drwxrwxrwx  root root /dev/shm/unit05/dir4/          
 -rw-------  root root /dev/shm/unit05/dir4/file4 (�ƻs�Ӧ� /etc/hosts)          
 
 cd /dev/shm     
![9](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/9.PNG?raw=true)  
 
 �إ�unit05: mkdir unit05      
 �]�wunit05���v��:chmod u=rwx,g=rwx,o=rx unit05         
 cd unit05/     
#### �إ߸�Ƨ�        
 mkdir dir1      
 mkdir dir2    
 mkdir dir3   
 mkdir dir4     
![10](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/10.PNG?raw=true) 
  
#### �]�wdir 1-4���v��       
 chmod u=rwx,g=rx,o=r dir1   
 chmod u=rwx,g=rx,o=x dir2  
 chmod u=rwx,g=rx,o=rx dir3  
 chmod u=rwx,g=rwx,o=rwx dir4  
![11](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/11.PNG?raw=true)  
 
#### �ƻs 
 cp /etc/hosts /dev/shm/unit05/dir1/file1        
 cp /etc/hosts /dev/shm/unit05/dir2/file2       
 cp /etc/hosts /dev/shm/unit05/dir3/file3         
 cp /etc/hosts /dev/shm/unit05/dir4/file4         
![12](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/12.PNG?raw=true) 
 
#### �]�wfile 1-4���v�� 
 cd dir1/         
 chmod u=rw,g=r,o=r file1        
 cd ..       
 cd dir2/        
 chmod u=rw,g=r,o=r file2      
 cd ..        
 cd dir3/    
 chmod u=rw,g=rw,o=rw file3     
 cd ..      
 cd dir4/     
 chmod u=rw,g=,o=  file4       
![13](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/13.png?raw=true) 
 
### 3-2�ϥΤ@��ϥΪ� �������i��U���u�@�G        
  
### 1.�Шϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H   
![14](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/14.PNG?raw=true) 
       
### 2.�Шϥ� ls -l /dev/shm/unit05/dir1/file1 �A�̧ǱN�W�z���ɦW�� dir1/file1 ~ dir4/file4 ����A�̾ڲ��ͪ����G��������|�p���H         
![15](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-3/ACS107131/15.PNG?raw=true)  
          
### 3.�Шϥ� vim /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4�A�����x�s (�αj���x�s)�A��������i�H/���i�H�x�s�H      
 vim /dev/shm/unit05/dir1/file1 �L�k�x�s �]���S���v��           
 vim /dev/shm/unit05/dir2/file2 �L�k�x�s �]���S���v��       
 vim /dev/shm/unit05/dir3/file3 �i�H�x�s �]�����v��     
 vim /dev/shm/unit05/dir4/file4 �L�k�x�s �]���S���v��          