# Linux HW-3

# �Ĥ@�D



### �Ĥ@�p�`



![1.1](https://images2.imgbox.com/c3/ac/lFYS3RYd_o.png)



>�����n�إߤT�ӱb���A�Q��**useradd**�����O�إߡC

>�إ߱K�X�H**echo password | passws --stdin username**�����O�i��A�]����ܥX�K�X�O�o�����n�D�A�o���O�i�H�j�q�]�w�K�X�A����ܱK�X�P�ɤ]�O�o�ӫ��O�����I/�a�B�Ҧb�C



### �ĤG�p�`



![1.2](https://images2.imgbox.com/59/0b/gPPOC77D_o.png)



>���ۧQ��**ls / ls -l / ll**���������O�T�{�a�ؿ����إߡA�A��**userdel -r**�����O�R��**examuser3**�A�M��A�Q�Ϋ��O�T�{/home�M/var/spool/mail�����e�C



### �ĤT�p�`



![1.3](https://images2.imgbox.com/d3/33/rYUYHIq9_o.png)



>�Q��**userdel**�����O�R��**examuser1**�åB���s�T�{/home�M/var/spool/mail�����e�C



![1.4](https://images2.imgbox.com/1e/a1/odL1kzQQ_o.png)



>���F�άۦP��UID���سQ�R�����b���A�ϥ�**useradd -u**���ѼƨӥH���wUID���覡�Ыرb���A�å[�J **-U** ���ѼƨӫإߩM�b��ۦP���s�աC
>�b�T�{�b��UID�ۦP����A�A�H�W�z**echo password | passwd --stdin username**�����O�]�w�K�X�Y�i�C



# �ĤG�D



### �Ĥ@�p�`



![2.1](https://images2.imgbox.com/95/28/R2jWhLiR_o.png)



>�o�����ըϥ�**useradd -p**�����O�H�����]�w�K�X��123���覡�إߨϥΪ̡C

>���ۨϥ�**cp  �ɮרӷ�  �ƻs�ت��a**�����O�ƻs�@���ɮר�/home/examuser4�̡A�ê`�N����examuser4���o���ƻs���ɮ��ݩ�other�������B�S�������v���C


![2.2](https://images2.imgbox.com/3a/37/qEVvsHsu_o.png)



>���Q��**chown**�����O�Nexamuser4�令�o���ƻs�ɮת��֦��̡A�A�Q��**chmod**�����O�t�X�Ʀr�k�N�֦��̪��v���� **6(rw-)** ���ɦ� **7(rwx)** �C



###�ĤG�p�`



![2.2](https://images2.imgbox.com/59/35/4EVL0h7R_o.png)

>�Q��**mkdir**�����O�إߦW��exmadata���ؿ��A���ۦAexamdata���Q��**touch**�����O�إߤ@���Ū�change.txt�ɮסC



![2.3](https://images2.imgbox.com/81/08/lWRbuKwf_o.png)



>�Q��**chown**�����O����ɮ׾֦��̬�**sshd**�A���ۧQ��**grep users /etc/group**�����O�T�{users���s�լO�_�s�b�C

>���ۧQ��**chgrp**�����O�ܧ��ɮת��s�աA��**chmod**�����O�N�v���אּ640�����A�A�A�Q�Ϋ��O�T�{�ɮת��ݩʡC



![2.4](https://images2.imgbox.com/9f/b4/frVrUmuy_o.png)



>�̫�Q��**touch -t**�����O�ק�ɶ��A�ѫe�����O��**�褸�~ �� �� �p�� �� ��**�C


# �ĤT�D



### �Ĥ@�p�`



![3.1](https://images2.imgbox.com/03/8b/KdoBLXj9_o.png)



>�����N��檺�ɮשM�ؿ��إ߰_�ӡA���ƧQ��**chmod / mkdir / cp **�T�ث��O�C



![3.2](https://images2.imgbox.com/60/cc/ubFL5Tit_o.png)



>���۽T�{�U���ݩʩM���W�@�P�C

### �ĤG�p�`



![3.3](https://images2.imgbox.com/6e/2c/AYG2K7zP_o.png)



>���Q��**su**�����O�N������**root**�����^**�@��ϥΪ�(shimakaze)**�A���ۿ�J **ls -l /dev/shm/unit05/dir[1-4]** �����O���[��{�H�C

�����ڭ̵o�{**�ɮ�1**�M**�ؿ�2**�L�k���\��ܥX�ӡA���ۤ���U�ӥؿ������٦��ɮפ������v���A�A�t�X���~�o�ͮɩҴ��Ѫ��^�崣�ܡA�ڭ̥i�H����**�ɮ�1**���ҥH�L�k��ܬO�]��**dir1**���**shimakaze**�Ө������i���檺�A�ɭP�ڭ̥u�i���d�b��Ū��**dir1**�����ΡF�ӲĤG���Ʀܳs**�ɮ�2**���S�X�{�O�]��**dir2**���**shimakaze**�Ө��O���iŪ�����ؿ��A�J�M���iŪ���N���δ���`�J���Ʊ��F�C



### �ĤT�p�`



![3.4](https://images2.imgbox.com/97/aa/AgvFm4pK_o.png)



>�Q�Ϋ��O�̧ǰ���|�Ӷ��ءC

�b�|�ӥؿ����u��**dir1**���**shimakaze**�Ө������i���檺�A�]���S�����|�i�H��F�ؿ������ɮסC�Ө�L�T�ӳq�L�ؿ���A�������ɮ׹��**shimakaze**�Ө��ҬO�iŪ�����A�䤤**file4**�O�]���B��**dir4**���[�c���A�ӫD�����ݩʡC

### �ĥ|�p�`



![3.5](https://images2.imgbox.com/14/35/eIR6YMYr_o.png)
![3.6](https://images2.imgbox.com/57/02/LOByRp0Q_o.png)

![3.7](https://images2.imgbox.com/89/57/2XFtE0AC_o.png)



>�Q�Ϋ��O�i�J��r�s��Ҧ�

�o�{**file1**�O��Ū�ɮסA�ä����ǥѱj���x�s�h�X�ӧ�ʤ��e�C�]��**file1**���**shimakaze**�Ө������i��g���C



![3.8](https://images2.imgbox.com/06/b0/HQtEak73_o.png)

![3.9](https://images2.imgbox.com/74/b9/Z4yrCTYQ_o.png)



�o�{**file2**�]�O��**file1**���ۦP���ΡA�j��]�S�ΡC



![3.10](https://images2.imgbox.com/08/81/Pe22pXod_o.png)

![3.11](https://images2.imgbox.com/3c/a5/92Qqe3or_o.png)



**file3**������**shimakaze**�Ө��O�i��g���A�]���i�H���`����ʤ��e�C



![3.12](https://images2.imgbox.com/4f/33/n3T44PKE_o.png)

![3.13](https://images2.imgbox.com/7b/63/ZlTcFMqD_o.png)

![3.14](https://images2.imgbox.com/bb/a2/jsNpLJ8j_o.png)



**file4**���**shimakaze**�Ө��O���i��g���A�]�����`�x�s�L�k��ʨ䤺�e�C���O�]��**file4**���**dir4**�[�c���A��**dir4**���**shimakaze**�Ө��O�i��g���A�]���ڭ̥i�H�αj������x�s���}�ӧ��**file4**�����e�C