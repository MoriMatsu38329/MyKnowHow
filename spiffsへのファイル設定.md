2023/12/29 松田

#      SPFFIS領域にビルド時にデータを設定する方法


ディレクトリを作成し、その下にファイルを保存する（現状、1ディレクトに1ファイルしかダメ見たい）  
例えば、spiffs_imageディレクを作成し、それ以下に下記のようにファイルを設定

・ TOPのディレクトリ直下にspiffs_imageディレクトリを作成

```  
　　　spiffs_image/ ----- html/ ---- control.html
                    +---- wifi/ ---- sta.txt
                    +---- hello.txt
```  

mainディレクトリのCMakeList.txtに以下の設定を追加

```
     spiffs_create_partition_image(storage ../spiffs_image FLASH_IN_PROJECT)

       storage          : 格納するパーティション名  
       ../spiffs_image  :  ファイルを格納しているディレクトリ名。CMakefile.txtのある場所基準  
       FLASH_IN_PROJECT : 固定　  
``` 

 上記の設定により、ビルド時にspiffsにディレクトリ/ファイル名でファイルが格納される  

fopenにて、fopen("/spiffs/wifi/sta.txt","r")でファイルをオープンすれば普通のディスク  
アクセス同様,情報の取得が可能である  

ただし、現状は、高水準だけ。低水準は2023/12/29時点では詳細不明。    
ILI9341のテストプログラムを解析すれば分かると思うのだが・・・・  




