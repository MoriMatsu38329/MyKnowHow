
# JTag�ɂ��f�o�b�O���@

* VSCode���N��  
* �\�t�g���J��  
* VSCode�̉�ʍ��̉��}�̃A�C�R�����N���b�N����


* lanuch.json���ȉ��ł��邱�Ɗm�F�B  elf�̓v���W�F�N�g�ɍ��킹��  

```
{
    // IntelliSense ���g�p���ė��p�\�ȑ������w�ׂ܂��B
    // �����̑����̐������z�o�[���ĕ\�����܂��B
    // �ڍ׏��͎����m�F���Ă�������: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name":  "ESP32 OpenOCD",
            "type":  "cppdbg",
            "request": "launch",
            "cwd": "${workspaceFolder}/build",
            "program": "${workspaceFolder}/build/udp_multicast.elf",
            "miDebuggerPath": "C:/Users/morim/.espressif/tools/xtensa-esp-elf-gdb/12.1_20221002/xtensa-esp-elf-gdb/bin/xtensa-esp32-elf-gdb.exe",
            "setupCommands": [
                {"text": "target remote 127.0.0.1:3333"},
                {"text": "set remote hardware-watchpoint-limit 2"},
                {"text": "monitor reset halt"},
                {"text": "flushregs"}
            ]
        }
    ]
}
```

* �^�[�Q�b�g�Ɏ��s�t�@�C������������ł���

* ����ݒ肷�邽�߁AVSCode�̃^�[�~�i����ňȉ������s�BVSCode�̃^�[�~�i���́A�u�\���v���u�^�[�~�i���v�ŊJ���B
�@�i�R�}���h�̓��e�́AESP-IDF CMD���C���X�g�[�����ɂł����R�}���h�v�����v�g�A�C�R���̃v���p�e�B�̐ݒ�j

```
C:\WINDOWS\system32\cmd.exe /k ""C:\Espressif\idf_cmd_init.bat" esp-idf-320ad5a1f7f1ffa6c2d9808f7d43bb34"
```

* �f�o�b�O���ݒ�̂��߁AVSCode�̃^�[�~�i����ňȉ������s

```
openocd -f board/esp32-wrover-kit-3.3v.cfg
```

* ���s�E�f�o�b�O�̃A�C�R�����N���b�N

