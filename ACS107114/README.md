# HW3 ACS107114

## �Ĥ@�D
* �ϥ�useradd�إ߱b��examuser1,examuser2,examuser3
![](https://i.imgur.com/LSbXfAF.png)
* �R��examuser3,�s�P�a�ؿ��P�l���ɮצP�B�R��
![](https://i.imgur.com/TEu9lvn.png)
* examuser1�Q�R�� �����٭�ӨϥΪ�
�Hsudo userdel examuser1�������� �åHll /home/�ˬd
![](https://i.imgur.com/aiCfLcH.png)
�Hsudo user -u 1001 -m examuser1�٭�examuser1
![](https://i.imgur.com/PTaUHAC.png)

## �ĤG�D
* �إ�examuser4
![](https://i.imgur.com/IVcscn9.png)
* �ϥ� root �N /etc/securetty �ƻs�� examuser4 �ýᤩ�Ҧ��v��
![](https://i.imgur.com/Ugdo93o.png)

* �ˬd�O�_���\�ק��v��
![](https://i.imgur.com/DFFDjgI.png)

* �إ� /examdata/change.txt
![](https://i.imgur.com/SED0AIq.png)
* ���֦��̬� sshd �֦��s�լ� users�Asshd �iŪ�i�g users �s�զ����iŪ ��L�H�S�v��
![](https://i.imgur.com/kZtkInt.png)
* �ç����վ㦨2012�~12��21��
![](https://i.imgur.com/vP14TM0.png)

## �ĤT�D
* �i�J/dev/shm/ �ëإ�unit05(�ק���v��) �A�إ�dir1,dir2,dir3,dir4�|�Ӹ�Ƨ�
![](https://i.imgur.com/uIfIS64.png)
* �ק�dir1,dir2,dir3,dir4�v��
![](https://i.imgur.com/tte5XgO.png)
* �ƻs/etc/hosts�� dir1,dir2,dir3,dir4 �ñN�ɦW�אּ file1,file2,file3,file4
![](https://i.imgur.com/Nn7lfdn.png)
* �ק�file1�v��
![](https://i.imgur.com/g4zg29e.png)

* �ק�file2�v��
![](https://i.imgur.com/v6F2CDp.png)

* �ק�file3�v��
![](https://i.imgur.com/zoKuH4n.png)

* �ק�file4�v��
![](https://i.imgur.com/NDfjkJH.png)

#### �Шϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H
* dir1 �]�O drwxr-xr-- ��L�H�u��Ū
* dir2 �]�O drwxr-x--x �u����� �L�kŪ
* dir3 �]�O drwxr-xr-x ��Ū����� �L�k�ק�
* dir4 �]�O drwxrwxrwx �i�H���N����

#### �Шϥ� ls -l /dev/shm/unit05/dir1/file1 �A�̧ǱN�W�z���ɦW�� dir1/file1 ~ dir4/file4 ����A�̾ڲ��ͪ����G��������|�p���H
* file1 �]�O -rw-r--r-- �u��Ū��
* file2 �]�O -rw-r--r-- �u��Ū��
* file3 �]�O -rw-rw-rw- �i�HŪ���P�ק�
* file4 �]�O -rw------- �G�L�k�ϥ�

#### �Шϥ� vim /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4�A�����x�s (�αj���x�s)�A��������i�H/���i�H�x�s�H
* �L�k�x�s
* unit05 �]�O drwxrwxr-x ��L�H�S���ק諸�v��