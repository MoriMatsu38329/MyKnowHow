
# JTagによるデバッグ方法

* VSCodeを起動  
* ソフトを開く  
* VSCodeの画面左の下図のアイコンをクリックする


* lanuch.jsonが以下であること確認。  elfはプロジェクトに合わせる  

```
{
    // IntelliSense を使用して利用可能な属性を学べます。
    // 既存の属性の説明をホバーして表示します。
    // 詳細情報は次を確認してください: https://go.microsoft.com/fwlink/?linkid=830387
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

* ターゲットに実行ファイルを書き込んでおく

* 環境を設定するため、VSCodeのターミナル上で以下を実行。VSCodeのターミナルは、「表示」→「ターミナル」で開く。
　（コマンドの内容は、ESP-IDF CMDをインストール時にできたコマンドプロンプトアイコンのプロパティの設定）

```
C:\WINDOWS\system32\cmd.exe /k ""C:\Espressif\idf_cmd_init.bat" esp-idf-320ad5a1f7f1ffa6c2d9808f7d43bb34"
```

* デバッグ環境設定のため、VSCodeのターミナル上で以下を実行

```
openocd -f board/esp32-wrover-kit-3.3v.cfg
```

* 実行・デバッグのアイコンをクリック

