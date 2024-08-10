# MSBuild����ϱ� (VS2010����)
## 1. VSCode���� ������Ʈ�� ������ �Ʒ��� ���� ������ �Ѵ�.
  ```json
  {
    "terminal.integrated.profiles.windows": {
        "Visual Studio 10": {
            "path": "C:\\Windows\\System32\\cmd.exe",
            "args": ["/K", "c:\\Program Files (x86)\\Microsoft Visual Studio 10.0\\VC\\bin\\vcvars32.bat"]
        }
    },
    "terminal.integrated.defaultProfile.windows": "Visual Studio 10",
  }
  ```
  *.vscode/setting.json* �� ���� ���� �����Ѵ�.\
  Visual Studio 2010�� vcvars32.bat�� �����ؾ� msbuild�� ����� �� �ִ�.

  ![.vscode/setting.json](image/vs2010.settings.json.png)

## 2. &lt;Ctrl>+`���� Terminal ����
  ![vs2010.terminal](image/vs2010.terminal.png)

## 3. Terminal���� �Ʒ��� ���� Compile�ϱ�
  ```command
  > dir *.vcxproj
  > msbuild gartmain.vcxproj
  > msbuild gartmain.vcxproj /t:clean
  > msbuild gartmain.vcxproj /t:build
  > msbuild gartmain.vcxproj /t:rebuild
  > msbuild -help
  > msbuild gartmain.vcxproj -t:clean
  > msbuild gartmain.vcxproj -t:build
  > msbuild gartmain.vcxproj -t:rebuild
  ```

## 4. VS2022�� .vscode/setting.json�� �����ϸ� �ȴ�.

