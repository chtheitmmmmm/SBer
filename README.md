
# SBer
����һ��ͨ�������а�������ʱ��ؼ�¼��ʵĹ��ߡ�<br>
<br>��ǰ�汾��1.0.0
<br>��֧��Windowsƽ̨��

## To use
Put the whole package "SBer" under "D:\\".<br>
Add "SBer\bin" to your Path. Open cmd.exe, input 
```
sber -v
```
to test if it could work.
## Full Usage
```
sber [[-h|-help] || [-v|-ver|-version] || [-config] || [-i|-in|-input [path?]] || [-o|-out|-output path]] [--default] [thought?]
```

<aside>ע��</aside>
<ul>
<li>�������Ҫ����������ʻ��ض�������·��������<b>ANSI����</b>��ʽ��������ļ����Ҳ�Ҫ�Գ�ANSI����֮����������뷽ʽ��config.json���ֶ���д�������ݡ���Ȼ�����˱��������ֵġ�
</ul>

# Options
## -h
It give you a simple guide about how to use this tool via console output.
```s
sber -h
```
## -v
It give you a info about the current version that sber is.
```s
sber -v
```

## -i
Wether open the input mode or specifying an input file.If there is an option after this option, the option will open getting input file from the configured input path.If there is an normal string after this option, it will be resolved as a path of a new input stream.

```s
sber -i "Today I pictured a number of beautiful flowers."
```
The usage above will firstly add the content of the configured file in SB\src\config.json['input'] to the configured file in SB\src\config.json['output'], and put the last sentence to the same output target at its tail. Rember to keep a newline token in your input file.
```s
sber -i d:\mythought.txt "My thought."
```
The usage above will just redirected the input file to d:\mythought.txt��and the last sentence will be add as usual.


## -config
You can configure the input file and output file in an inner json file mannally, or use this option. When appear, the given path after `-o` and the probably given path after `-i` will be writen to the json file automatically as an addtional function.
```s
sber -i c:\mythought.txt -o d:\mysb.txt -config
```
With `-config`, we have the path after `-i` and/or `-o` saved in the SB\src\config.json.
```
sber -config -i -o d:\mysb.txt
```
This usage will only save the new output path after `-o` option. And `-i` option will work as usual.
## --default
If appears, only `-config` can be recognized, other options will be ignored.<br>
With this option, input file will set to config.json["default"]["input"], and output file will be set to config.json["default"]["output"], and timeformat string will be set to config.json["default"]["timeformat"].
```shell
sber --default -config
```
The above usage will be the same as followed:
```shell
sber -config -i ..\default\input.txt -o ..\default\output.txt -tf \n%Y��%m��%d�� %H:%M:%S\n -config
```
All other options will be ignored. 
## thought
Your thought, may usually should be quoted by 
' " ' around, will be added at last.
<hr/>

# ���������С�������С��ϷҲ����Ȥ�Ļ�����ӭ���<a href="http://www.cmtheit.com">�ҵ���վ</a>������ˣร�

ɧ�ŷ�ʽ
<address>QQ:2905432378</address>
<address>΢�ţ�zc2905432378</address>
<address>E-mail: cmtheit@outlook.com</address>