#### Linux�ɮ��v���M��¦�b���޲z

## �إ߱b��
1.�n�Jroot����
2.�إߤT�ӱb��examuser1,examuser2,examuser3�A�K�X�Ҭ�ItIsExam
  * useradd examuser �إ�
  * passwd examuser �ק�K�X
3.�ˬd�b��(UID/GID)
  * id examuser1
     wid=1001  gid=1001  groups=1001
  * id examuser2
     wid=1002  gid=1002  groups=1002
  * id examuser3
     wid=1003  gid=1003  groups=1003
  * id         (root����)
     wid=0  gid=0  groups=0
----------------------------------------------------

## �R���b��
1.userdel examuser3 -r
  * -r �s�P�a�ؿ��R��
2.userdel examuser1
  * �u�R���ϥΪ�
3.�ˬd�ϥΪ�
  * ll -d /home/examuser
  * �ɮ��v��:
   (1)drwx------. 2 1001 1001 62 Oct 15:50 /home/examuser1
   (2)drwx------. 2 examuser2 examuser2 62 Oct 15:51 /home/examuser2
   (3)No such file or directory
----------------------------------------------------

## ���رb��
1.useradd -u 1001 -U examuser1
2.�ˬd�ϥΪ�(ll -d /home/examuser)
  * drwx------. 2 examuser1 examuser1 62 Oct 15:50 /home/examuser1
3.passwd examuser1 �ק�K�X
----------------------------------------------------

## �إ߭ק鶴�����ɮ�
1.�إ�examuser4
2.�ϥ�root�N/etc/securetty�ƻs��examuser4
  * cp /etc/securetty /home/examuser4
3.�ˬd�O�_���ƻs
  (1)su examuser4 �i�Jexamuser4�b��
  (2)cd /home/examuser4 �����ؿ�
  (3)ll �ˬdsecuretty�O�_�s�b
4.�ק��v��
  (1)�^��root�b��
  (2)chmod u+x,g+rwx,o+rwx securetty
  (3)ll �ˬd�O�_�ק令�\
5.�إߤέק�/examdata/change.txt
  (1)mkdir examdata
  (2)cd examdata
  (3)vi change.txt
  (4)[Esc]�A:wq
  (5)�ק�֦��� chown sshd change.txt
  (6)�ק�s�� chgrp users change.txt
  (7)�ק��v�� chmod (sshd�i�g�iŪ�Ausers�iŪ�A��L�H�S�v��)
  (8)�ק�ɶ� touch -t 201212210829[YYYYMMDDhhmm]
----------------------------------------------------


## root�������ɮ׻P�v��
1.�إߥؿ�   mkdir + �ؿ��W��
2.�����ؿ�   cd + �ؿ��W��
3.�إ��ɦW     vi + �ɦW
  * �i�J�ɮפ��A�ϥ�[esc]�A:w(�x�s)q(���})
4.�����^�W�h�ؿ�  cd ..
5.�ק��v��   chmod + u/g/o/a + +/-/= + �ɦW
  �̫�אּ
drwxrwxr-x  root root /dev/shm/unit05/
drwxr-xr--  root root /dev/shm/unit05/dir1/
-rw-r--r--  root root /dev/shm/unit05/dir1/file1
drwxr-x--x  root root /dev/shm/unit05/dir2/
-rw-r--r--  root root /dev/shm/unit05/dir2/file2
drwxr-xr-x  root root /dev/shm/unit05/dir3/
-rw-rw-rw-  root root /dev/shm/unit05/dir3/file3
drwxrwxrwx  root root /dev/shm/unit05/dir4/
-rw-------  root root /dev/shm/unit05/dir4/file4
----------------------------------------------------

## �@��ϥΪ̨���
1.root�������@��ϥΪ�
  * su + �Τ�W
2.ls -l /dev/shm/unit05/dir[1-4]�ˬd��X���G
  �L�k�ϥΦ���k�A�ҥH�Q��cd�����ؿ�
  (1)���ϥ�cd ~
  (2)�A��cd .. (home)
  (3)cd .. (/)
  (4)cd dev
  (5)cd shm
  (6)cd unit05
  (7)cd dir[1~4]
   - dir1 ����
   - dir2 ��
   - dir3 ��
   - dir4 ��
    * �q���i��Oother���v���S��x(����)�ӵL�k�}��
3.ls -l /dev/shm/unit05/dir[1~4]/file[1~4]�ˬd��X���G
  ��k�P�W�A�A�h���@����file[1~4]
  - dir1/file1 ����
  - dir2/file2 ����
  - dir3/file3 ����
  - dir4/file4 ����
    * �q���i��Oother���v���S��x(����)�ӵL�k�}��
4.vi /dev/shm/unit05/dir1/file1 ~ vi /dev/shm/unit05/dir4/file4�����x�s
  - vi /dev/shm/unit05/dir1/file1 �L�k�x�s
  - vi /dev/shm/unit05/dir2/file2 �L�k�x�s
  - vi /dev/shm/unit05/dir3/file3 �L�k�x�s
  - vi /dev/shm/unit05/dir4/file4 �L�k�x�s
    * �q���i��Oother���v���S��w(�s��)�ӵL�k�}��