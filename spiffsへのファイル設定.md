2023/12/29 ���c

#      SPFFIS�̈�Ƀr���h���Ƀf�[�^��ݒ肷����@


�f�B���N�g�����쐬���A���̉��Ƀt�@�C����ۑ�����i����A1�f�B���N�g��1�t�@�C�������_���������j  
�Ⴆ�΁Aspiffs_image�f�B���N���쐬���A����ȉ��ɉ��L�̂悤�Ƀt�@�C����ݒ�

�E TOP�̃f�B���N�g��������spiffs_image�f�B���N�g�����쐬

```  
�@�@�@spiffs_image/ ----- html/ ---- control.html
                    +---- wifi/ ---- sta.txt
                    +---- hello.txt
```  

main�f�B���N�g����CMakeList.txt�Ɉȉ��̐ݒ��ǉ�

```
     spiffs_create_partition_image(storage ../spiffs_image FLASH_IN_PROJECT)

       storage          : �i�[����p�[�e�B�V������  
       ../spiffs_image  :  �t�@�C�����i�[���Ă���f�B���N�g�����BCMakefile.txt�̂���ꏊ�  
       FLASH_IN_PROJECT : �Œ�@  
``` 

 ��L�̐ݒ�ɂ��A�r���h����spiffs�Ƀf�B���N�g��/�t�@�C�����Ńt�@�C�����i�[�����  

fopen�ɂāAfopen("/spiffs/wifi/sta.txt","r")�Ńt�@�C�����I�[�v������Ε��ʂ̃f�B�X�N  
�A�N�Z�X���l,���̎擾���\�ł���  

�������A����́A�����������B�ᐅ����2023/12/29���_�ł͏ڍוs���B    
ILI9341�̃e�X�g�v���O��������͂���Ε�����Ǝv���̂����E�E�E�E  




