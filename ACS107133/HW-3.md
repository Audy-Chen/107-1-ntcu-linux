1.��J#useradd examuser1�إߤT�ӱb��:examuser1, examuser2, examuser3�C��J�K�X#passwd examuser1�A�|�_�Xnew password:�A�A��JItIsExam�A�|�X�{Retype new password:�A�A��J�@���K�X�A���᭫�ưʧ@�C
2.�ϥ�# userdel -r examuser3�A�R��examuser3�b���M�a�ؿ��A�R���᥼�X�{�ԭz�A�ҥH�ڵL�k�T�w�O�_�R���A�ڦA��J�@���@�˪����O�A�o�{�o��examuser3���s�b�A�ҥH�ڽT�w�ڤw�g�R��examuser3�F�C
3.��J# id examuser1 �d��examuser1��id�AUID�MGID�o�{��1002�A�A��J# userdel examuser1�R�����b��(���R���a�ؿ�)�C
4.��J#adduser -u 1002 examuser1�A�إ߱b���A�A��Jpasswd examuser1���K�X�C


1.��J#useradd examuser4�A�A��J#passwd examuser4�A�ڿ�J���K�X��pp22�A����ܻ��ڪ��K�X�OBAD PASSWORD�A�]���֩�C���r�C
2.�ڭ����T�{�O�_�s�bsecuretty�A�]���ڲ��ʨ�ؿ�etc�U�A�M���Jcd securetty�ANot a directory�A�쥻�H�����s�b�o��securetty�A����ӵo�{�A�O�]��securetty�ڥ����O�@�Ӹ�Ƨ��A�p�G��ls���O�N�i�H�ݨ�etc��Ƨ��U�s�bsecuretty�C
3.���۶}�l�Nsecuretty�ƻs��examuser4�A�����T�{examuser4�����|�A��cd���O���ʨ�examuser4����A��Jpwd���O�A�|��ܥX��e�����|�A���ۥ�cd���O���ʦ^etc��Ƨ��U�A�M���J���Ocp securetty "��~�ƻs��examuser4���|"�A�N�����F�ƻssecuretty�C
4.����ls -l�d��securetty���v���A�ثe�Oroot�Ҿ֦��A��J���Ochown examuser4 securetty�A�M��A��ls -l�d�ݤ@��securetty���v���A�i�H�o�{�w�g�ܬ�examuser4�Ҿ֦��A����ۤv���v�����Orw-�A�u��Ū�M�g�A���������C
5.���F���examuser4��securetty���v���A��examuser4�i�H����securetty�A��Jchmod 700 securetty�A�䤤7�N��ϥΪ̥iŪ���B�i�g�J�B�i�����ɮסA00�N��s�ժ��H�M��L�H���iŪ���B�g�J�B�����ɮסC�䤤7�N��1(����) + 2(�g�J) + 4(Ū��)�C��J�����O���ls -l�T�{�v���O�_��勵�T�A�i�H�ݨ��v���w�g��אּ700�A�ϥΪ̥iŪ���B�i�g�J�B�i����C
6.�]���쥻�S��examdata��Ƨ��A�ҥH�n���Ыؤ@�ӡA��J���Omkdir examdata�A��ls�i�H�ݨ�Ыت���Ƨ��A�M��cd examdata�A���ʨ��Ƨ��U�A���۳Ы�change.txt�A��J���Ovi change.txt�A�ѩ�쥻���s�bchange.txt�A�ҥH�|�۰ʳЫؤ@��change.txt���ɮסA�]���S���n�s�褺�e�A�ҥH�����x�s���}�N�i�H�F�A����esc��A�M���J:wq�A�g�J�����}�A�������Jls�A�T�{change.txt�w�g�Ыئ��\�C
7.��Jls -l�A�i�H�ݨ�{�b���ɮ׾֦��̬Oroot�A�B��l�H�u��Ū�����v���C��Jchown sshd change.txt�A�M���ls -l�d�ݡA�o�{�ɮת��֦��̤w�g�ܬ�sshd�C
8.���M�֦��̤w�g��אּsshd�A���֦��s�ը̵M�Oroot�A��J���Ochgrp users change.txt�A���s�վ֦��̬�users�A�ϥ�ls -l�d�ݡA�o�{�s�վ֦��̤w�g���T���C
9.�ثe�ٳѤU�v���٨S���A�쥻���v���O�ϥΪ̥iŪ���B�i�g�J�A�s�վ֦��̥iŪ���A��L�H�iŪ���A���D�حn�D��L�H���iŪ���A�]���A�ϥ�chmod 640 change.txt�A�N��L�H���v���]�����iŪ���A�ϥ�ls -l�ˬd�o�{�v���w�g���T�ܧ�C�䤤6�N��2(�g�J) + 4(Ū��)�A4�N��iŪ���B���i�g�J�B���i����A0�N���iŪ���B���i�g�J�B���i����C
10.����ls -l�d�ݭ쥻�ɶ���Oct 22 01:23�A�A�ӬO�n���ɶ��A��Jtouch -t 201212210303 change.txt�A�A���ls -l�d�ݮɶ��A�ܬ�Dec 21 2012�A�o�˴N�ק令�\�F�C


1.��Jcd dev�i�J���ؿ���A�A��Jcd shm�A��Jmkdir unit05 �إߦ��ؿ��A�ϥ�ls -l�d���v���o�{��drwxr-xr-x�A��Jchmod 775 unit05�A�N����אּdrwxrwxr-x�C
2.�Aunit05�o�ӥؿ��U�A�إߤ@�ӥs��dir1���ؿ��A��Jmkdir dir1�A�ϥ�ls -l�d���v���A�o�{��drwxr-xr-x�A��Jchmod 754 dir1�A�N�v����אּdrwxr-xr--�C
3.�ϥΫ��Ovi file1�A�bdirl���ؿ��U�إߤ@�ӥs��file1���ɮסA�|���X�s���ɮסA���UESC��h�X�A�b��J:wq�A�i�h�X�s��Ҧ��A�b�ϥ�ls -l�d���v���i�o�{���ɮ��v���N��-rw-r--r--�C
4.��Jcd ..�h��unit05���ؿ��A�ϥ�mkdir dir2�إߥؿ��A�b����ls -l�d���v����drwxr-xr-xr--�A��Jchmod 751 dir2����v����drwxr-x--x�C
5.��Jcd dir2�i�J�ؿ��A��Jvi file2�إ��ɮסA�ë�ESC�h�X�s��A�b��J:wq�����h�X�A��Jls -l�d���v���i�o�{��-rw-r--r--�C
6.��Jcd ..�h��unit05���ؿ��A�ϥ�mkdir dir3�إߥؿ��A�b����ls -l�d���v����drwxr-xr-xr--�A��Jchmod 755 dir3����v���A�b��Jls -l�d���v���ܧ�drwxr-xr-x�C
7.��Jcd dir3�i�J�ؿ��A��Jvi file3�إ��ɮסA�ë�ESC�h�X�s��A�b��J:wq�����h�X�A��Jls -l�d���v���i�o�{��-rw-r--r--�A��Jchmod 666 file3����v����-rw-rw-rw-�C
8.��Jcd ..�h��unit05���ؿ��A�ϥ�mkdir dir4�إߥؿ��A�b����ls -l�d���v����drwxr-xr-xr--�A��Jchmod 777 dir4����v����drwxrwxrwx�C
9.��Jcd dir4�i�J�ؿ��A��Jvi file4�إ��ɮסA�ë�ESC�h�X�s��A�b��J:wq�����h�X�A��Jls -l�d���v���i�o�{��-rw-r--r--�A��Jchmod 600 file4����v����-rw-------
10.��Juseradd examuser �Ыؤ@��b���A�b��Jpasswd examuser�A�ڱN�K�X�]��556677�C
11.��Jsu examuser�󴫬��@��ϥΪ̡A�ϥ�cd dir1��ܬ�Permission denied�A�]��dir1�o�ӥؿ���examuser�o�ӨϥΪ̨ӻ��v����r--�u�iŪ�����i����C
12.�A�ӿ�Jcd dir2�A�i�i�J���ؿ��A�]���L��examuser���v����--x�i����A���ϥ�ls -l�o�ӫ��O�L�k�ݨ�L���v���A�]�������iŪ�C
13.��Jcd ..�h��unit05���ؿ��A�b��Jcd dir3�i�J�ؿ��A�o�{�i�H�i�J�]��userexam���v����r-x�A�ϥ�ls -l�]�i�d���v���A���L�k�ϥ�vi�s���ɮסC
14.��Jcd ..�h��unit05���ؿ��A�A��Jcd dir4�i�J�ؿ��A�o�{�i�i�J�]�i�ϥ�ls -l�d���v���]��examuser���v����rwx�C
15.��Jcd ~�h�^host ~�A��Jls -l /dev/shm/unit05/dir1/file1�A�]�Xpermission denied�A�]��examuser��file1���v����r--�C
16.��Jls -l /dev/shm/unit05/dir2/file2�A�]�Xpermission denied�A�]��examuser��file2���v����r--�C
17.��Jls -l /dev/shm/unit05/dir3/file3�A�]�Xpermission denied�A�]��examuser��file3���v����rw-�C
18.��Jls -l /dev/shm/unit05/dir4/file4�A�]�Xpermission denied�A�]��examuser��file4���v����---�C
20.��Jvim /dev/shm/unit05/dir1/file1�A�L�k�x�s�A�]���v����r--
21.��Jvim /dev/shm/unit05/dir2/file2�A�]�L�k�x�s�A�v���P��r--
22.��Jvim /dev/shm/unit05/dir3/file3�A�i�H�x�s�A�]���v����rw-
23.��Jvim /dev/shm/unit05/dir4/file4�A���i�x�s�A�]���v����---