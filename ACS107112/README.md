![](https://i.imgur.com/csrQVyj.png)
+ �ЫؤT�ӨϥΪ�
![](https://i.imgur.com/FphnW1X.png)
+ �]�w�K�X ItIsExam
![](https://i.imgur.com/No2z7V9.png)
+ �R��examuser3
![](https://i.imgur.com/V9CuIdj.png)
+ �R��examuser1
![](https://i.imgur.com/txeLUY0.png)
![](https://i.imgur.com/FLx9ZYZ.png)
![](https://i.imgur.com/kpQj1Xb.png)
![](https://i.imgur.com/8rF4N84.png)
+ ��examuser1�Ыئ^��
+ �ó]�w�K�X
![](https://i.imgur.com/fd02Jdx.png)
+ �Ы�examuser4
![](https://i.imgur.com/N25tID9.png)
+ �ó]�w�K�X
![](https://i.imgur.com/UPljQpU.png)
+ �ϥ� root �N /etc/securetty �ƻs�� examuser4
![](https://i.imgur.com/GQmGIRt.png)
![](https://i.imgur.com/YJTcS9r.png)
![](https://i.imgur.com/3RLrLn8.png)
+ �إߤ@�ӦW�� /examdata/change.txt �����ɮסA�o���ɮת��֦��̬� sshd�A�֦��s�լ� users�Asshd �iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v���C�B�o���ɮת��ק����нվ㦨 2012 �~ 12 �� 21 ��



+ �]���ѤF�I�ϡA�S���Ϥ��Ш���
#root�����إ��ɮ׻P�v�� 
+ ��Jcd /dev/shm/�i�J��Ƨ�
+ ��Jmkdir unit05�إ��ɮ�
+ ��Jchmod u=rwx,g=rwx,o=rx unit05</li>
+ ��Jcd unit05�i�J</li>
+ ��Jmkdir ���O�[�W�إߥ|�Ӹ�Ƨ� </li>
+ �ק�dir1,dir2,dir3,dir4�v���p�U
	dir1��chmod u=rwx,g=rx,o=r dir1
	dir2��chmod u=rwx,g=rx,o=x dir2 
	dir3��chmod u=rwx,g=rx,o=rx dir3
	dir4��chmod u=rwx,g=rwx,o=rwx dir4 </li>
<li>�ƻs/etc/hosts�� dir1,dir2,dir3,dir4�A�N�ɦW�אּ file1,file2,file3,file4
	dir1��cp /etc/hosts /dev/shm/unit05/dir1/file1
	dir2��cp /etc/hosts /dev/shm/unit05/dir2/file2
	dir3��cp /etc/hosts /dev/shm/unit05/dir3/file3
	dir4��cp /etc/hosts /dev/shm/unit05/dir4/file4 </li>
#�ק�file1�v��
<li>��Jcd unit05/dir1/</li>
<li>��Jchmod u=rw,g=r,o=r file1</li>
#�ק�file2�v��
<li>��Jcd unit05/dir2/</li>
<li>��Jchmod u=rw,g=r,o=r file2</li>
#�ק�file3�v��
<li>��Jcd unit05/dir3/</li>
<li>��Jchmod u=rw,g=rw,o=rw file3</li>
#�ק�file4�v��
<li>��Jcd unit05/dir4/</li>
<li>��Jchmod u=rwx,g=rwx,o=rwx file4</li>
#�Шϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H
<li>dir1��Ū</li>
<li>dir2�O�u�����A�L�kŪ</li>
<li>dir3�L�k�ק�</li>
<li>dir4�i�H���N����</li>
#�� ls -l /dev/shm/unit05/dir1/file1�A�̧ǱN�W�z���ɦW�� dir1/file1 ~ dir4/file4 ����A�̾ڲ��ͪ����G��������|�p���H
<li>dir1,dir2��Ū</li>
<li>dir3�iŪ�i�ק�</li>
<li>dir4�L�k�ϥ�</li>
#�� vim /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4�A�����x�s (�αj���x�s)�A��������i�H/���i�H�x�s�H
<li>other�S�����unit05��4�Ӹ�Ƨ����ק��v��</li>
</ol> 
