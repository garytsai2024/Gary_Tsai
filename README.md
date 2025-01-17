# Python虛擬環境與Visual Studio Code開發環境
>  參考：何敏煌 Python虛擬環境與Visual Studio Code開發環境 - YouTube：https://www.youtube.com/watch?v=PsS5aA0qSD8 


執行 Visual studio code
---

Open Folder：
---
>  在Visual studio code中，選單中，選擇 File，選擇 Open Folder

New Terminal：
---
>  在 Visual studio code 選單中，選擇 Termial，選擇 New Terminal

建立 虛擬環境：
---
>  在 Visual studio code的Terminal中，執行： virtualenv venv

啟動 虛擬環境：
---
>  在 Visual studio code的Terminal中，執行： venv\scripts\activate.ps1，結果終端提示符號前會出現 (venv) ， 表示我們已經在venv虛擬環境中

檢查 虛擬環境：
---
>  在 Visual studio code的Terminal中，執行： pip list，應該只看見安裝了 pip 24.3.1，其他模組都沒有裝

在虛擬環境中安中模組：
---
>  在終端提示符號前有 (venv)的情況下安裝所需的模組，都只會安裝在此虛擬環境中

打包虛擬環境：
---
>  在終端提示符號前有 (venv)的情況下，執行：pip freeze > requirements.txt，就會將此虛擬環境安裝的模組與版本寫入requirements.txt

重建打包的虛擬環境：
---
>  在終端提示符號前有 (venv)的情況下，執行：pip install -r ".\requirememts.txt"，就會安裝requirements.txt中所列的全部模組

關閉 虛擬環境：
---
>  在終端提示符號前有 (venv)的情況下，執行：deactivate，就能關閉此虛擬環境

解決Visual Studio Code無法在Terminal中執行虛擬環境：
---
>  如果出現錯誤的紅字，表示目前無法執行  venv\scripts\activate.ps1 所以無法建立虛擬環境\
>  解決方法需要另外使用系統管理員權限去開一個Power Shell，然後執行以下的指令：Set-ExecutionPolicy RemoteSigned\
>  使用系統管理員權限去開一個Power Shell：選擇 Windows 開始，選擇 Powershell，按滑鼠右鍵選擇 Powershell 7 (x64)，選擇更多，選擇【以系統管理員身分執行】\
>  在 Powershell 中，在命令列輸入： Set-ExecutionPolicy RemoteSigned，然後按 Enter 執行。如果有出現問句，則輸入 y，然後按 Enter。\
>  回到 Visual studio code，將之前開的 Terminal 關掉， 然後在 Visual studio code 選單中，選擇 Termial，選擇 New Terminal，這時 Termial 應該就是在在venv虛擬環境中。
>  檢查在venv虛擬環境中，目前已安裝的模組，可以執行： pip list，檢查安裝的模組是不是只有 pip 24.3.1模組 及 numpy 2.2.1模組。
