# 1-1�G�إߤT�ӥΤ�A�b���W�٤��O���G examuser1, examuser2, examuser3 �A�P�ɤT�ӥΤ᪺�K�X���O�y ItIsExam �z�C    
�n�J�ϥΪ̱b����A��"su -"���O�������޲z��root    
��"useradd (username)"�إ߷s�b���B"passwd (username)"�]�w�K�X    

# 1-2�G�ЧR���t�Τ��� examuser3 �o�ӱb���A�P�ɱN�o�ӱb�����a�ؿ��P�l���ɮצP�B�R���C    
��"userdel -r (username)"�R���ϥΪ̪��a�ؿ��θ��    
�`�N!!! �S���[�W-r�a�ؿ����|�R��    

# 1-3�Gexamuser1 ���p�߳Q�޲z���R���F�A���O�o�ӱb�����a�ؿ��P�����l���٦s�b�C�аѦҳo�ӱb���i�઺�a�ؿ��ҫO�d�� UID �P GID�A �ù��եH�ӱb���즳�� UID/GID ��T�ӭ��ظӱb���C    
��"useradd -u (��b����UID) (username)"���رb��    

# 2-1�G�إ�examuser4�ϥΪ̱b���A�K�X���N�C    
�n�J�ϥΪ̱b����A��"su -"���O�������޲z��root    
��"useradd (username)"�إ߷s�b���B"passwd (username)"�]�w�K�X    

# 2-2�G�ϥ� root �N /etc/securetty �ƻs�� examuser4�A�B�o�ӱb���n�������ϥθ��ɮפ~��A(�Y���Ҧ����v��)�C    
����"cp"�ƻs�ɮסA�M���"chgrp"�ק�s�աA�̫��"chmod"�ק��v��    
[�Ʀr�k�Gr=4,w=2,x=1 ��n�����v���Ʀr�ۥ[]   

# 2-3�G�إߤ@�ӦW�� /examdata/change.txt �����ɮסA�o���ɮת��֦��̬� sshd�A�֦��s�լ� users�Asshd �iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v���C�B�o���ɮת��ק����нվ㦨 2012 �~ 12 �� 21 �� (������T�Y�i�A�ɶ��H�K)�C    
����"mkdir"�إ߸�Ƨ��A�A��"touch"�إ��ɮ�    
�H���"chown"���֦��̡A"chgrp"���s�աA"chmod"�ק��v��    
�̫�A��"touch -d (time) (�ɮצW��)"�ק�ɶ��A�o�˴N�i�H�F    

# 3-1�G�Шϥ� root �������إߩ��U���ɮ׻P�v���G    
drwxrwxr-x  root root /dev/shm/unit05/    
drwxr-xr--  root root /dev/shm/unit05/dir1/    
-rw-r--r--  root root /dev/shm/unit05/dir1/file1 (�ƻs�Ӧ� /etc/hosts)    
drwxr-x--x  root root /dev/shm/unit05/dir2/    
-rw-r--r--  root root /dev/shm/unit05/dir2/file2 (�ƻs�Ӧ� /etc/hosts)    
drwxr-xr-x  root root /dev/shm/unit05/dir3/    
-rw-rw-rw-  root root /dev/shm/unit05/dir3/file3 (�ƻs�Ӧ� /etc/hosts)    
drwxrwxrwx  root root /dev/shm/unit05/dir4/    
-rw-------  root root /dev/shm/unit05/dir4/file4 (�ƻs�Ӧ� /etc/hosts)    

��"mkdir"�إ߸�Ƨ��A"touch"�إ��ɮסA"cp"�ƻs�A"chmod"�ק��v��    

#�ϥΤ@��ϥΪ� �������i��U���u�@�G    
��"su (username)"���^�ϥΪ�    

# 3-2�G�Шϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H    
dir1����L�H�ϥ��v���� r--�A���M�i�H�\Ū�A���ʥFx�v���A�G�������    
dir2����L�H�ϥ��v���� --x�A���M�i�H����A���ʥFr�v���A�G����d��    
dir3����L�H�ϥ��v���� r-x�A�P�ɾ֦��\Ū�ΰ����v���A�i�H���`����    
dir4����L�H�ϥ��v���� rwx�A�P�ɾ֦��\Ū�ΰ����v���A�i�H���`����    

# 3-3�G�Шϥ� ls -l /dev/shm/unit05/dir1/file1 �A�̧ǱN�W�z���ɦW�� dir1/file1 ~ dir4/file4 ����A�̾ڲ��ͪ����G��������|�p���H    
file1���v���ʥFx�A�]���L�k����    
file2-4��x�v���A�]���i�H���`����    

# 3-4�G�Шϥ� vim /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4�A�����x�s (�αj���x�s)�A��������i�H/���i�H�x�s�H   
dir1  r--    
file1 r-- �]dir1�ʥFx�v���A�G�L�k����    

dir2  --x    
file2 r-- ���Mdir2�������v���A��file2�u��Ū�����v���A�]������}�ҩM�ק�    

dir3  r-x    
file3 rw- �]dir3���\Ū�B�����v���A��file3��r��w�v���A�G�ॿ�`Ū���M�ק�        

dir4  rwx    
file4 --- ���Mdir4�����v���A��file4�S�������v���A�]�����వ�����