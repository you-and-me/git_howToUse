SVN�Ǽ���ʽ�汾����ϵͳ
GIT�Ƿֲ�ʽ�汾����ϵͳ��ÿ̨���Ծ���һ�������İ汾�⣬����ʱ�Ͳ���Ҫ�����ˣ������Ե��޸����͸��Է��Ϳ��Ի��࿴���Է����޸��ˡ�

һ�������汾��
1�������㴴�����ļ��� -> shift+�Ҽ� -> ������� -> �������git init

�������ļ���ӵ��汾��
1��git add �ļ���       ���ļ���ӵ��ݴ���
2��git commit -m "xxx�ύ��"      ���ļ��ύ���ֿ⣬�����ڵ���ע��
3��git status       �鿴�Ƿ����ļ�δ�ύ
4��git diff �ļ���      �鿴�ļ��޸���ʲô
ע���ļ��޸ĺ�Ҫִ��1/2���������ύ��

5��git log         �鿴��ʷ��¼
   git log -pretty=online       �鿴������ʷ��¼
6��git reset -hard HEAD^        ���˵��ϸ��汾
   git reset -hard HEAD^^       ���˵����ϸ��汾
   git reset -hard HEAD~100        ���˵�ǰ100���汾
7��git reflog         ���˺󣬲鿴����ǰ�İ汾
8��git checkout -- �ļ���	����δ�ŵ��ݴ���������
9��cat �ļ���		�鿴�ļ�����

����ɾ���ļ�
1��git rm �ļ���	ɾ���ύ�ˡ�δ�޸ĵ��ļ�

�ģ�Զ�ֿ̲�
1���ѱ��زֿ���������͵�github�ֿ�
�ڱ��زֿ����������git remote add origin git@github.com:you-and-me/test-use.git

		      git push -u origin master
	����Զ�̿��ǿյģ����ǵ�һ������master��֧ʱ�������� �Cu������Git������ѱ��ص�master��֧�������͵�Զ���µ�master��֧������ѱ��ص�master��֧��Զ�̵�master��֧�������������Ժ�����ͻ�����ȡʱ�Ϳ��Լ����

	��Զ�ֿ̲ⲻ�ǿյ�ʱ��ֻ��git push origin master
2��git clone git@github.com:you-and-me/test-use.git	��Զ�̿��¡�����ؿ�

�壺������ϲ���֧
1��git checkout -b ��֧��	-b��ʾ�������л�����֧���ȼ��������������
   git branch ��֧��		������֧
   git checkout ��֧��		�л�����֧

   git branch 			�鿴��֧����ǰ��֧ǰ������һ���Ǻš�

2��git merge ��֧��		�ϲ�ָ����֧����ǰ��֧��
   git merge -no-ff -m "ע��" ��֧		ʹ�ô����� �Cno-ff�����á�Fast forward��ģʽ������ɾ����֧�󶪵���֧��Ϣ

3��git branch -d ��֧��		ɾ����֧

4��git stash			����ǰ�����ֳ���������
   git stash list		�鿴�����ֳ�
   git stash apply		�ָ�
   git stash drop		ɾ��stash����
   git stash pop		�ָ���ɾ��stash����

��������Э��
1��git remote		�鿴Զ�̿���Ϣ
   git remote -v	�鿴Զ�̿����ϸ��Ϣ
2��git push origin master	Git���master��֧���͵�Զ�̿��Ӧ��Զ�̷�֧��	

