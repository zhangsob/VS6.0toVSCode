# MSBuild사용하기 (VS2010기준)
## 1. VSCode에서 프로젝트를 폴더에 아래와 같은 설정을 한다.
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
  *.vscode/setting.json* 에 위과 같이 설정한다.\
  Visual Studio 2010의 vcvars32.bat를 실행해야 msbuild를 사용할 수 있다.

  ![.vscode/setting.json](image/vs2010.settings.json.png)

## 2. &lt;Ctrl>+`으로 Terminal 열기
  ![vs2010.terminal](image/vs2010.terminal.png)

## 3. Terminal에서 아래와 같이 Compile하기
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

## 4. VS2022도 .vscode/setting.json을 설정하면 된다.

