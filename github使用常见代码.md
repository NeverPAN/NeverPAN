# gitһЩ����ָ��

## �ϴ�ָ��
git init  
git add README.md  ���ϴ�ȫ���ļ���git add . ��
git commit -m "first commit"
git branch -M main����ʱ����master��
git remote add origin https://github.com/NeverPAN/NeverPAN.git ����ַ���ţ�
git push -u origin main
## ��ȡָ��
git remote add origin https://github.com/NeverPAN/NeverPAN.git
git branch -M main
git push -u origin main

#### ���url��ַ��  
git remote -v�鿴��ϸ��Ϣ����ʾ������д���url��ַ ����취��   
1.ʹ�� git remote rm originָ���Ƴ�ԭ�ȴ����origin remote   
2.ʹ��git remote -vȷ���Ѿ�ɾ��   
3.ʹ��git remote add origin �Լ��ֿ��url��ַ  

#### ͼƬ����  
##### һ�����뱾��ͼƬ   
�� Markdown �в��뱾��ͼƬ���﷨�ܼ򵥣�ֻ��Ҫ���ı������һ���� ! ��ͷ���У��������ͼƬ��·�������磺  
![Alt text]��/path/to/image.jpg)   
�����ͬ�ļ��У���ֱ��дͼƬ��������1.png���������һ�ļ��У���д../1.png���Դ�����  
����������У�Alt text ��ͼƬ������ı�����ͼƬ�޷�����ʱ������ʾ����ı���/path/to/image.jpg ��ͼƬ��·�������������·�������·����  
##### ������������ͼƬ  
�� Markdown �в�������ͼƬҲ�ܼ򵥣�ֻ��Ҫ��ͼƬ�� URL ��ӵ� ![Alt text]��URL) ���﷨�м��ɡ����磺  
![Alt text��(https://example.com/image.jpg)    
����������У�Alt text ��ͼƬ������ı���https://example.com/image.jpg ��ͼƬ�� URL��  



#### ���´���
��һ�����鿴��ǰ��git�ֿ�״̬������ʹ��git status  
git status  
�ڶ���������ȫ��  
git add *  
����������������git commit -m ������˵����  
git commit -m ������˵����   
���Ĳ�����git pull,��ȡ��ǰ��֧���´��루Ҳ���ǻ�ȡGitHub�ϵ����´�����Ϣ�����±��ش��룩  
git pull  
���岽��push��Զ��master��֧�ϣ��޸ı��ش�����ٸ���GitHub�ϵĴ��룩  
git push origin master  
�������⣬��GitHub�Ѿ�ͬ����  
��֮����pull����push  
��������������������������������  
    ��Ȩ����������Ϊ����ԭ�����£���ѭ CC 4.0 BY-SA ��ȨЭ�飬ת���븽��ԭ�ĳ������Ӻͱ�������
                       
ԭ�����ӣ�https://blog.csdn.net/jasonLee_lijiaqi/article/details/79947741



#### error: failed to push some refs to�Ĵ�������������ڶ���ԭ����ɵġ�
������һЩ�����Ľ��������  
1. ���Զ�ֿ̲�����   
ȷ�����Զ�ֿ̲�����������ȷ������ʹ��git remote -v����鿴��ǰ���õ�Զ�ֿ̲⡣������ò���ȷ������ʹ��git remote set-url������������Զ�ֿ̲��ַ��  
2. ��ȡ���´���  
�����ʹ���֮ǰ����������ȡԶ�ֿ̲�����´��룬ȷ�����زֿ���Զ�ֿ̲��״̬һ�¡�����ʹ��git pull������ȡ���´��룬�����Ǳ�ڵĳ�ͻ��  
3. ����֧״̬
ȷ�����������͵ķ�֧�Ǵ��ڵģ�������Զ�ֿ̲�ķ�֧״̬һ�¡�����ʹ��git branch����鿴���ط�֧��ʹ��git ls-remote --heads����鿴Զ�̷�֧��  

4. ���Ȩ������
ȷ�������㹻��Ȩ�޽��������͵�Զ�ֿ̲⡣�����˽�вֿ⣬������Ҫ��֤��ݻ��ȡ����Ա��Ȩ��

5. ʹ��ǿ������
������Ϸ������޷�������⣬���Գ���ʹ��ǿ�����͡�ʹ��git push -f�������ǿ�ƽ����زֿ�ĸ������͵�Զ�ֿ̲⡣����ע�⣬ǿ�����ͻḲ��Զ�ֿ̲�Ķ�Ӧ��֧�������ʹ�á�

6. �鿴������־
�������������Ȼ�޷�������⣬���Բ鿴git push��������Ĵ�����־���Ի�ȡ����ϸ�Ĵ�����Ϣ���������ڽ�һ����λ�������ڡ�

7. ������
��ʱ��Git�Ļ�����ܻᵼ������ʧ�ܡ�����Գ�������Git�Ļ��棬Ȼ���������͡�����ʹ��git rm -r --cached .���������棬Ȼ��ʹ��git add .��git commit���������ύ���ġ�

�ܽ�  
����error: failed to push some refs to����ʱ����Ҫ���š���������������һ�Ų����⣬������һ���ܹ��ҵ����������ͬʱ�����������ʹ���֮ǰ���Ƚ��г�ֵĲ��ԣ�ȷ��������ȶ��ԺͿɿ��ԡ�


#### Updates were rejected because the tip of your current branch is behind (���±��ܾ�����Ϊ��ǰ��֧�������Զ�̷�֧)
 
�����ַ�����  
pushǰ�Ƚ�Զ��repository�޸�pull������Ȼ�������ͣ�  
git pull origin master   
git push -u origin master  
2. ʹ��ǿ��push�ķ�����  
git push -u origin master -f   
������ʹԶ���޸Ķ�ʧ��һ���ǲ���ȡ�ģ������Ƕ���Э��������ʱ��  
3. ������mergeԶ�̺ͱ����޸ģ������ȴ����µķ�֧:  
git branch [name]   
#Ȼ��push   
git push -u origin [name]  

git SSL certificate problem: unable to get local issuer certificate
�������������û���������εķ�����HTTPS��֤��Ĭ�ϣ�cURL����Ϊ�������κ�CAs������˵�����������κη�������֤��

ֻ��Ҫִ����������Ϳ��Խ����

git config --global http.sslVerify false
��������������������������������

  ��Ȩ����������Ϊ����ԭ�����£���ѭ CC 4.0 BY-SA ��ȨЭ�飬ת���븽��ԭ�ĳ������Ӻͱ�������
                        
ԭ�����ӣ�https://blog.csdn.net/weixin_44014995/article/details/109900149