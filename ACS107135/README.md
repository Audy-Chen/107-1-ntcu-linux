### Q1-1:�إߤT�ӥΤ�A�b���W�٤��O���G examuser1, examuser2, examuser3 �A�P�ɤT�ӥΤ᪺�K�X���O�y ItIsExam �z�C(�аѦҮѤWpasswd --stdin������)    
����ϥΪ̤�����root�v���A�M���useradd�إ߱b���B��passwd�]�w�K�X    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/1.PNG)    
--------------------------------------    
### Q1-2:�ЧR���t�Τ��� examuser3 �o�ӱb���A�P�ɱN�o�ӱb�����a�ؿ��P�l���ɮצP�B�R���C    
�Q��userdel -r (username)�P�ɧR���b�����a�ؿ��P�l���ɮ�    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/2.PNG)    
--------------------------------------    
### Q1-3:examuser1 ���p�߳Q�޲z���R���F�A���O�o�ӱb�����a�ؿ��P�����l���٦s�b�C�аѦҳo�ӱb���i�઺�a�ؿ��ҫO�d�� UID �P GID�A �ù��եH�ӱb���즳�� UID/GID ��T�ӭ��ظӱb���C�ӳo�ӱb�����K�X�е��� ItIsExam ���˦��C(�����ظm�b�������O�A�аѦ� man useradd ���u�W��󪺻���)    
��useradd -u (��b����uid) (username) ����examuser1���b��    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/3.PNG)    
--------------------------------------    
### Q2-1:�إ�examuser4�ϥΪ̱b���A�K�X���N�C    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/4.PNG)    
--------------------------------------    
### Q2-2:�ϥ� root �N /etc/securetty �ƻs�� examuser4�A�B�o�ӱb���n�������ϥθ��ɮפ~��A(�Y���Ҧ����v��)�C    
��cp���O�ƻs�ɮסA�A��chmod���O�ק��v��    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/4.5.PNG)    
--------------------------------------    
### Q2-3:�إߤ@�ӦW�� /examdata/change.txt �����ɮסA�o���ɮת��֦��̬� sshd�A�֦��s�լ� users�Asshd �iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v���C�B�o���ɮת��ק����нվ㦨 2012 �~ 12 �� 21 �� (������T�Y�i�A�ɶ��H�K)    
����mkdir�إ߸�Ƨ��A�A��touch�إ��ɮסA�M��ק��v���C�̫��touch -d (time) (username) �ק�ɶ�    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/5.PNG)    
--------------------------------------    
### Q3-1:�Шϥ� root �������إߩ��U���ɮ׻P�v���G    
### drwxrwxr-x  root root /dev/shm/unit05/    
### drwxr-xr--  root root /dev/shm/unit05/dir1/    
### -rw-r--r--  root root /dev/shm/unit05/dir1/file1 (�ƻs�Ӧ� /etc/hosts)    
### drwxr-x--x  root root /dev/shm/unit05/dir2/    
### -rw-r--r--  root root /dev/shm/unit05/dir2/file2 (�ƻs�Ӧ� /etc/hosts)    
### drwxr-xr-x  root root /dev/shm/unit05/dir3/    
### -rw-rw-rw-  root root /dev/shm/unit05/dir3/file3 (�ƻs�Ӧ� /etc/hosts)    
### drwxrwxrwx  root root /dev/shm/unit05/dir4/     
### -rw-------  root root /dev/shm/unit05/dir4/file4 (�ƻs�Ӧ� /etc/hosts)    
mkdir�إߥؿ��Btouch�إ��ɮסBcp�ƻs�Bchmod����v��    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/6.PNG)    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/7.PNG)    
--------------------------------------    
### Q3-2:�Шϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H    
1.dir1����L�H�v����r--�C���֦�r(�\Ū)�v���o���֦�x(����)�v���A�ҥH�ɭPfile1�X�{�\�h??�����p�C    
2.dir2����L�H�v����--x�C�]���ʥF�Fr(�\Ū)�v���A�ҥH�L�k�d�ݨ䤺�e�C    
3.dir3����L�H�v����r-x�C�P�ɾ֦�r�Bx�v���A��X���`�C    
4.dir4����L�H�v����rwx�C�P�ɾ֦�r�Bx�v���A��X���`�C    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/8.PNG)    
--------------------------------------    
### Q3-3:�Шϥ� ls -l /dev/shm/unit05/dir1/file1 �A�̧ǱN�W�z���ɦW�� dir1/file1 ~ dir4/file4 ����A�̾ڲ��ͪ����G��������|�p���H    
1.�]��dir1����L�H�v����r--�A�ʥFx�v���ɭP��U��file1�L�k����C    
2.dir[2-4]����L�H�v���Ҿ֦�x�v���A�ҥH��Ufile[2-4]�����O�Ҭ����`    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/9.PNG)    
--------------------------------------    
### Q3-4:�Шϥ� vim(or vi) /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4�A�����x�s (�αj���x�s)�A��������i�H/���i�H�x�s�H    
file1->�]��W��dir1����L�H�v���ʥFx(����)�v���A�ҥH�L�k�}��    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/10.PNG)    
    
file2(��L�H�v����r--)->��Ū�ɡA�i�H�d�ݦ�����ק�s��    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/11.5.PNG)    
    
file3(��L�H�v��rw-)->�֦�r(�\Ū)�Bw(�ק�)�v���A�i�H�d�ݤ]��ק�s��    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/12.PNG)    
    
file4(��L�H�v��rwx)->�֦�r(�\Ū)�Bw(�ק�)�v���A�i�H�d�ݤ]��ק�s��    
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-3/ACS107135/photo/13.PNG)    