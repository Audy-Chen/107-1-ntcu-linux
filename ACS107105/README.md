+ (I)  ![GITHUB](https://i.imgur.com/Is80iRv.jpg "git�ϥ�")
 
+ �إߤT�ӥΤ�A�b���W�٤��O���G examuser1, examuser2, examuser3

+ �K�X�]�w��ItIsExam

![GITHUB](https://i.imgur.com/96uHFZx.jpg "git�ϥ�")

+ �ϥΡuuserdel -r examuser3�v�R���t�Τ���examuser3�b��(�]�t�a�ؿ�.�l���ɮ�)

+ �ϥΡuuserdel examuser1�v�R�� examuser1 ,���ɵo�{�a�ؿ�.�l���ɮפ��M�d�s

+ �Q��UID/GID���� examuser1�����b����� �K�X�]�w��ItIsExam

![GITHUB](https://i.imgur.com/jtF8FtJ.jpg "git�ϥ�")
![GITHUB](https://i.imgur.com/Is80iRv.jpg "git�ϥ�")

+ (II)

+ �إ�examuser4

![GITHUB](https://i.imgur.com/t0kKm5S.jpg "git�ϥ�")

+ �ϥ� root �N /etc/securetty �ƻs�� examuser4

![GITHUB](https://i.imgur.com/kFdrXbl.jpg "git�ϥ�")

+ �Q��ROOT���A,�ק�/etc/securetty���v��

![GITHUB](https://i.imgur.com/96uHFZx.jpg "git�ϥ�")

+ �إߤ@�ӦW�� /examdata/change.txt �����ɮסA�֦���:sshd�A�s��:users�Asshd�iŪ�i�g�Ausers �s�զ����iŪ�A��L�H�S�v���C
+ �N�ק����нվ㦨 2012 �~ 12 �� 21 �� 

[Imgur](https://i.imgur.com/dgM7LGH.jpg)

[Imgur](https://i.imgur.com/QgixQej.jpg)

+ (III)

+ �ϥ�root�i�J/>/dev/shm�A�إ߸�Ƨ�unit05,�íק���v��

+ �i�hunit05�s�Wdir1.dir2.dir3.dir4.dir5,�íק���v��

+ �N/etc/hosts�ƻs��/dev/shm/unit05/dir1/file1 (�P�z����file4)

[Imgur](https://i.imgur.com/VO7HBy4.jpg)

+ �i�Jdir1�A���Q��"ll"�d�ݪ�l�v���A�A�Q��"ls"�d��file1�O�_�s�b�A�íק������v���C (�P�z�i�J��L��Ƨ����ק�) 

[Imgur](https://i.imgur.com/xzwa9V3.jpg)

+ �ڱN�b��������examuser1

+ �ϥΫ��O ls -l /dev/shm/unit05/dir[1-4] 
+ examuser1���dir1�Mdir2�S���v���Adir3(o=r-x)�Mdir4(o=rwx)���v��������N�ϥΡC 

[Imgur](https://i.imgur.com/S6XQhv0.jpg)

+ �ϥΫ��O ls -l /dev/shm/unit05/dir1/file1 �A
�̧ǱN�W�z���ɦW�� dir1/file1 ~ dir4/file4 ����A
���G��examuser1���file1(�S���v��)�Bfile2(o=r--)�Bfile3(o=rw-)���v��������N�ϥΡBfile4(o=---)

[Imgur](https://i.imgur.com/wKns2PE.jpg)

+ �ϥ� vim /dev/shm/unit05/dir1/file1 ~ file4
+ �����x�s���G�X�{"command not found"
+ ���examuser1���㦳����"vim"���O���v���A�ҥH�����x�s

[Imgur](https://i.imgur.com/VEw9sSy.jpg)









