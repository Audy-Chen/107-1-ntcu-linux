1.�b���޲z����:

(1)�����i�J���������A�ϥ�root�n�J�A���ۤ��O��useradd examuser1�Apasswd examuser1;useradd examuser2�Apasswd examuser2;useradd examuser3�Apasswd examuser3�ӫإ߱b��(�K�X���O:ItIsExam)�C

(2)��userdel -r examuser3 �N�b�����a�ؿ��P�l���ɮצP�B�R���C

(3)��ls -al /home/�i�H�ݨ줣�p�߳Q�R����examuser1��UID�MGID�A�M���useradd -u UID�X -U examuser1�N�i�H��UID���رb���C


2.�v���޲z����:

(1)��useradd examuser4�Apasswd examuser4�إ߱b���C

(2)��cp /etc/securetty /home/examuser4/�A���ۥ�chown examuser4 securetty�A��chmod u=rwx, g=rwx, o=rwx examuser4�Ϧ��b���֦�����ϥ��ɮת��v���C

(3)��mkdir examdata�A����cd�i�hexamdata�̭��A��touch change.txt�إߪ��ɮסA��chown sshd change.txt�N�֦��̧אּsshd�A���ۥ�chgrp users change.txt�N�s�էאּusers�A���ۥ�chmod u=rw,g=r,o= change.txt�Nsshd�iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v���A�̫��touch -t 20121221 change.txt�N�ɮת��ק����վ㦨 2012 �~ 12 �� 21 ��C


3.�����ާ@:
(1)�ϥ� root �������n�J�Acd�i�hdev�A���ۥ�shm�A�M���mkdir unit05�A���ۥ�chmod u=rwx,g=rwx,o=rx unit05�ӧ���v���C�A��cd�i�Junit05�̡A��mkdir dir1�A�M��chmod u=rwx,g=rx,o=r dir1;�A��mkdir dir2�A�M��chmod u=rwx,g=rx,o=x dir2;�A��mkdir dir3�A�M��chmod u=rwx,g=rx,o=rx dir3;�A��mkdir dir4�A�M��chmod u=rwx,g=rwx,o=rwx dir4�C�A�ӥ�cp /etc/hosts dev/shm/unit05/dir1/file1 �i�hdir1�A�M��chmod u=rw,g=r,o=r file1;�Acd�i�Junit05�A��cp /etc/hosts dev/shm/unit05/dir2/file2 �i�hdir2�A�M��chmod u=rw,g=r,o=r file2;�Acd�i�Junit05�A��cp /etc/hosts dev/shm/unit05/dir3/file3 �i�hdir3�A�M��chmod u=rw,g=rw,o=rw file3;�Acd�i�Junit05�A��cp /etc/hosts dev/shm/unit05/dir4/file4 �i�hdir4�A�M��chmod u=rw,g=,o= file4�A�o�˴N�إߦn�ɮ׻P�v���F�C

(2)�ϥΤ@��ϥΪ̪������n�J�A�ϥ� ls -l /dev/shm/unit05/dir1�ɡA�|�Q�i���v�������A���㦳r���v���i�H�d���ɦW�A�]�S��x���v���A�ҥH�|�X�{�ݸ�;�ϥ� ls -l /dev/shm/unit05/dir2�ɡA�]�S��r���v���A�ҥH����d���ɦW;�ϥ� ls -l /dev/shm/unit05/dir3~4�ɡA�]���㦳r�Mx���v���A�ҥH�i�H����C

(3)�b����dir1/file1 ~ dir4/file4�ɡA�]�S��x���v���A�ҥH�L�k����C

(4)�ϥ� vim /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4 �x�s�ɡA�]dir3��w���v�� �ҥH�i�H�x�s�A��dir1,dir2,dir4�S��w���v���A�ҥH�����x�s�C
