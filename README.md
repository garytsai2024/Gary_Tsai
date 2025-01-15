# Gary_Tsai
Python虛擬環境與Visual Studio Code開發環境

參考 何敏煌 Python虛擬環境與Visual Studio Code開發環境 - YouTube：https://www.youtube.com/watch?v=PsS5aA0qSD8 

建一個資料夾，例如在 D:\md python-course，結果在D碟跟目錄就有新增了 python-course 資料夾

進入python-course資料夾，D:\cd python-course

建立虛擬環境，執行： virtualenv venv

檢查執行結果： 執行 dir，可以看到在 python-course 資料夾增加了一個 venv 資料夾

檢查還未進入虛擬環境時，目前已安裝的模組，執行： pip list，可以看見所以在整體環境中已安裝的模組 

啟動虛擬環境：在 D:\python-course 執行 venv\scripts\activate.bat，結果會出現 (venv) D:\python-course>， 表示我們已經在venv虛擬環境中

檢查在venv虛擬環境中，目前已安裝的模組，執行： pip list，可以看見只安裝了 pip 24.3.1，其他模組都沒有裝

我們在venv虛擬環境中設著安裝模組，執行：pip install numpy

檢查在venv虛擬環境中，目前已安裝的模組，執行： pip list，可以看見除了 pip 24.3.1模組，還新增了numpy 2.2.1模組

執行 Visual studio code，

在 Visual studio code 中，選單中，選擇 File，選擇 Open Folder，選擇 D:\python-course 資料夾

在 Visual studio code 中，在 D:\python-course 資料夾內增加一個測試檔案：test.py，輸入以下程式碼：

  import numpy as np

  arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])

  newarr = arr.reshape(4, 3)

  print(newarr)
