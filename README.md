openuploadify
==========

�����󱪵�Huploadify ģ�µ�uploadify�Ļ������������¹���
1. ���Ӷ�̬��ȡ��ҳ����
2. ����phpɾ��ҳ�棬��ɾ���Ѿ��ϴ��ļ���


����ΪԭHuploadify�Ĺ���
jQuery�ļ��ϴ������HTML5��uploadify��������uploadifyһ�µ�API����ȫɽկ��Uploadify������[http://www.uploadify.com/](http://www.uploadify.com/)

#####��ʵ�ֵ������У�
1. ���ļ��ϴ�
2. ��ʾ������
3. ��ʾ���ϴ��ļ���С�Ͱٷֱ�
4. �ļ���׺�����ļ���С���
5. �������ύ��������
6. �Զ����ļ������е�htmlģ��
7. css��ʽ����������ļ������Լ�������ʽ
8. ����ļ��ϴ����׶εĻص�����

------------

#####��ʵ�ֳ��õ�API��default������Ϣ���£�
    fileTypeExts:'*.*',//�����ϴ����ļ����ͣ���ʽ'*.jpg;*.doc'
    uploader:'',//�ļ��ύ�ĵ�ַ
    auto:false,//�Ƿ����Զ��ϴ�
    method:'post',//��������ķ�ʽ��get��post
    multi:true,//�Ƿ�����ѡ�����ļ�
    formData:null,//���͸�����˵Ĳ�������ʽ��{key1:value1,key2:value2}
    fileObjName:'file',//�ں�˽����ļ��Ĳ������ƣ���PHP�е�$_FILES['file']
    fileSizeLimit:2048,//�����ϴ����ļ���С����λKB
    showUploadedPercent:true,//�Ƿ�ʵʱ��ʾ�ϴ��İٷֱȣ���20%
    showUploadedSize:false,//�Ƿ�ʵʱ��ʾ���ϴ����ļ���С����1M/2M
    buttonText:'ѡ���ļ�',//�ϴ���ť�ϵ�����
    removeTimeout: 1000,//�ϴ���ɺ����������ʧʱ�䣬��λ����
    itemTemplate:itemTemp,//�ϴ�������ʾ��ģ��
    onUploadStart:null,//�ϴ���ʼʱ�Ķ���
    onUploadSuccess:null,//�ϴ��ɹ��Ķ���
    onUploadComplete:null,//�ϴ���ɵĶ���
    onUploadError:null, //�ϴ�ʧ�ܵĶ���
    onInit:null,//��ʼ��ʱ�Ķ���
    onCancel:null//ɾ����ĳ���ļ���Ļص��������ɴ������file
    onClearQueue:null,//����ϴ����к�Ļص��������ڵ���cancel���������*ʱ����
    onDestroy:null,//�ڵ���destroy����ʱ����
    onSelect:null,//ѡ���ļ���Ļص��������ɴ������file
    onQueueComplete:null//�����е������ļ��ϴ���ɺ󴥷�
#####ʹ�÷���
����ҳ������Ҫһ��������ͨ����һ��div���磺

`<div id="upload"></div>`

Ȼ����ò�����ɣ�

    $('#upload').Huploadify({
        auto:true,
        fileTypeExts:'*.jpg;*.png;*.exe',
        multi:true,
        formData:{key:123456,key2:'vvvv'},
        fileSizeLimit:1024,
        showUploadedPercent:true,
        showUploadedSize:true,
        removeTimeout:9999999,
        uploader:'upload.php',
        onUploadStart:function(file){
            console.log(file.name+'��ʼ�ϴ�');
        },
        onInit:function(obj){
            console.log('��ʼ��');
            console.log(obj);
        },
        onUploadComplete:function(file){
            console.log(file.name+'�ϴ����');
        },
        onCancel:function(file){
            console.log(file.name+'ɾ���ɹ�');
        },
        onClearQueue:function(queueItemCount){
            console.log('��'+queueItemCount+'���ļ���ɾ����');
        },
        onDestroy:function(){
            console.log('destroyed!');
        },
        onSelect:function(file){
            console.log(file.name+'�����ϴ�����');
        },
        onQueueComplete:function(queueData){
            console.log('�����е��ļ�ȫ���ϴ����',queueData);
        }
    });

�����APIʹ�÷�ʽ���ɲο�uploadify��������ȫ�ǲ�������API���ġ�

#####ʹ�ý�ͼ��
![ʹ�ý�ͼ](http://images.cnitblog.com/blog/520134/201312/01185252-55d3c4606ddb4a8995dc1b9563d2847b.jpg)