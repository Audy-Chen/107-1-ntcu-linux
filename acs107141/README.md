##1 
<ol>
<li>�n�JCentOS</li>
#�إ߱b�� 
<li>��Juseradd examuser1</li>
<li>��Jpasswd examuser1</li>
<li>���New Password:�ÿ�JItIsExam</li>
<li>�t�η|�A�T�{�@�M�K�X�A�A����J�Y�i�����]�w</li>
<li>�ھ�2~6���B�J�A�̧ǳ]�w���user�A���O��examuser2�Mexamuser3�A�K�X�Ҭ�ItIsExam</li>
<li>�������Jll /home/�ˬd</li>
<li>���|���
	drwx------. 2 examuser1		examuser1	���	�ɶ�	examuser1 
	drwx------. 2 examuser2		examuser2	���	�ɶ�	examuser2 
	drwx------. 2 examuser3		examuser3	���	�ɶ�	examuser3	</li> 
#�R��examuser3	
<li>��Juserdel -r examuser3</li>
<li>��J$ll /home/�ˬd</li>
<li>���|���
	drwx------. 2 examuser1		examuser1	���	�ɶ�	examuser1 
	drwx------. 2 examuser2		examuser2	���	�ɶ�	examuser2 </li>
#��_examuser1 
<li>��Juserdel examuser1��������</li>
<li>��Jll /home/�ˬd</li>
<li>���|���
	drwx------. 2 1001			1001		���	�ɶ�	examuser1 
	drwx------. 2 examuser2		examuser2	���	�ɶ�	examuser2 </li>
<li>��Jsudo useradd -u 1001 -m examuser1</li>
<li>��Jsudo passwd examuser1</li>
<li>���New Password:�ÿ�JItIsExam</li></li>
<li>��Jid examuser1</li>
<li>���
	uid=1001(examuser1) gid=1001(examuser1) groups=1001(examuser1)</li>
</ol>

##2
<ol>
#�إ�examuser4 
<li>��Juseradd examuser4</li>
<li>��Jpasswd examuser4</li>
<li>���New Password:�]�w�K�X</li></li>
#�ƻs�ɮרç���v�� 
<li>��Jcp /etc/securetty /home/examuser4</li>
<li>��Jls /home/examuser4�ˬd�O�_��securetty</li>
<li>��Jchmod u=rwx,g=rwx,o=rwx /home/examuser4/securetty</li>
#CHECK 
<li>��Jsu - examuser4�����ϥΪ�</li>
<li>��Jll�ˬd�O�_����v��</li>
#�s���ɮ� 
<li>��Jcd /home/examuser4/�i�J�ؿ�</li>
<li>��Jmkdir examdata�إ߸�Ƨ�</li>
<li>��Jls</li>
<li>�p���
	examdata	securetty �N���\</li>
<li>��Jcd examdata�i�J</li>
<li>��Jtouch change.txt�إ��ɮ�</li>
<li>��Jll�ˬd</li>
<li>���|���
	-rw-rw-r--. 1	examuser4 examuser4 0	���	�ɶ�	change.txt</li>
#���v�� 
<li>���^ROOT</li>
<li>��Jcd /home/examuser4/examdata/</li>
<li>��Jchown sshd change.txt���֦��̬�sshd</li>
<li>��Jchgrp users change.txt���s�լ�users</li>
<li>��Jchmod u=rw,g=r,o= change.txt����v����-rw-r-----</li>
<li>��Jll�ˬd</li>
<li>���|���
	-rw-r-----. 1	sshd users 0	���	�ɶ�	change.txt</li></li>
#��ɶ� 
<li>��Jtouch -t 201212210807 change.txt</li>
</ol>

##3

#root�����إ��ɮ׻P�v�� 
<li>��Jcd /dev/shm/�i�J��Ƨ�</li>
<li>��Jmkdir unit05�إ��ɮ�</li>
<li>��Jchmod u=rwx,g=rwx,o=rx unit05</li>
<li>��Jcd unit05�i�J</li>
<li>��Jmkdir ���O�[�W�إߥ|�Ӹ�Ƨ� </li>
<li>�ק�dir1,dir2,dir3,dir4�v���p�U
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
