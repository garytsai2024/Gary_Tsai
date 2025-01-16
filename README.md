Python虛擬環境與Visual Studio Code開發環境
===
參考：何敏煌 Python虛擬環境與Visual Studio Code開發環境 - YouTube：https://www.youtube.com/watch?v=PsS5aA0qSD8 

建立Python虛擬環境
---
> 建一個資料夾，例如在 D:\md python-course，結果在D碟跟目錄就有新增了 python-course 資料夾\
> 進入python-course資料夾，D:\cd python-course\
> 建立虛擬環境，執行： virtualenv venv\
> 檢查執行結果： 執行 dir，可以看到在 python-course 資料夾增加了一個 venv 資料夾\
> 檢查還未進入虛擬環境時，目前已安裝的模組，執行： pip list，可以看見所以在整體環境中已安裝的模組

啟動Python虛擬環境
---
> 啟動虛擬環境：在 D:\python-course 執行 venv\scripts\activate.bat，結果會出現 (venv) D:\python-course>， 表示我們已經在venv虛擬環境中\
> 檢查在venv虛擬環境中，目前已安裝的模組，執行： pip list，可以看見只安裝了 pip 24.3.1，其他模組都沒有裝\
> 我們在venv虛擬環境中設著安裝模組，執行：pip install numpy\
> 檢查在venv虛擬環境中，目前已安裝的模組，執行： pip list，可以看見除了 pip 24.3.1模組，還新增了numpy 2.2.1模組

在Visual studio code中啟動虛擬環境
---
> 執行 Visual studio code\
> 在 Visual studio code 中，選單中，選擇 File，選擇 Open Folder，選擇 D:\python-course 資料夾\
> 在 Visual studio code 中，在 D:\python-course 資料夾內增加一個測試檔案：test.py，輸入以下程式碼：
>> import numpy as np\
>> arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])\
>> newarr = arr.reshape(4, 3)\
>> print(newarr)

> 在 Visual studio code 選單中，選擇 Termial，選擇 New Terminal，這時 Termial 應該就是在在venv虛擬環境中。\
> 可以執行： pip list，檢查安裝的模組是不適只有 pip 24.3.1模組 及 numpy 2.2.1模組

解決Visual Studio Code無法在Terminal中執行虛擬環境
---
> 如果出現錯誤的紅字，表示目前無法執行  venv\scripts\activate.ps1 所以無法建立虛擬環境\
> 解決方法可參考：解決Visual Studio Code無法在Terminal中執行虛擬環境：https://104.es/index.php/2020/09/28/visual-studio-code-terminal-conda
> 
> 需要另外使用系統管理員權限去開一個Power Shell，然後執行以下的指令：Set-ExecutionPolicy RemoteSigned\
> 使用系統管理員權限去開一個Power Shell：選擇 Windows 開始，選擇 Powershell，按滑鼠右鍵選擇 Powershell 7 (x64)，選擇更多，選擇【以系統管理員身分執行】\
> 在 Powershell 中，在命令列輸入： Set-ExecutionPolicy RemoteSigned，然後按 Enter 執行。如果有出現問句，則輸入 y，然後按 Enter。\
> 回到 Visual studio code，將之前開的 Terminal 關掉， 然後在 Visual studio code 選單中，選擇 Termial，選擇 New Terminal，這時 Termial 應該就是在在venv虛擬環境中。
> 檢查在venv虛擬環境中，目前已安裝的模組，可以執行： pip list，檢查安裝的模組是不是只有 pip 24.3.1模組 及 numpy 2.2.1模組。
  
打包虛擬環境
---
> 在venv虛擬環境中執行： pip freeze > requirement.txt，就會將此虛擬環境安裝的模組與版本寫入requirement.txt\
> 當其他人要重建此虛擬環境時，只要執行：pip install -r ".\requirement.txt"，就能依據 requirement.txt 所列的模組及對應版本進行安裝
> 
