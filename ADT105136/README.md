#Linux用戶管理

先建立起三個用戶，密碼都設定成「ItIsExam」，同時也觀察家目錄是否存在，還有UID/GID
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/001.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/002.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/003.PNG)
之後使用userdel [-r] {username}將用戶連同家目錄一起刪除，不留一點痕跡
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/004.PNG)
如果過程中不小心誤刪了其他用戶，而用戶的家目錄還在，可以使用增加參數的方式重新建立用戶，並將用戶的uid和家目錄(需用絕對路徑)指定到新用戶上
新增完畢之後還需要再次檢查確認是否有漏掉甚麼
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/005.PNG)


#檔案權限的管理

先建立一個用戶並用cp [參數] {origin file position} {new position}把檔案拷貝到新用戶的家目錄裡，並且檢查家目錄中是否真的有檔案，因為檢查很重要所以要檢查三次！(誤
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/006.PNG)
但是現在只是把檔案丟過去，新建立的用戶沒有任何的權限，所以需要將擁有者、群組、使用權限做更改
首先進到檔案的目錄中，這樣確保不會去動到最原始的/etc/securetty檔案，再來就是一連串的連續技，為了確保安全，每次更動完就確認一次檔案屬性
全部都更動完畢後用戶就可以使用家目錄中的securetty了！
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/007.PNG)
若是要調整一份檔案的屬性，首先要先確定要變更的資料是否正確，例如：uid or gid是否存在，檔案的位置是否有重複名稱的檔案等等
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/008.PNG)
之後便可以用touch [-t YYYYMMddhhmm] {filename}去修改時間，以及修改權限等等 
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/009.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/010.PNG)

#檔案修改的權限

首先建立許多的目錄及拷貝檔案，然後修改每個檔案的權限
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/011.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/012.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/013.PNG)
接下來去查閱每個目錄
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/014.PNG)
根據當前的使用者來說dir1的權限是指可以閱讀但無法執行，所以無法看到目錄中檔案的各種屬性，只能知道有檔案在裡面；雖然dir2可以執行但是因為無法閱讀而查閱遭到拒絕；dir3、dir4因為可讀可執行所以可以很順利地看到各種資訊
所以要查閱目錄使用者必須擁有可讀可執行的權限


再來是去查閱目錄中的各個檔案
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/015.PNG)
因為dir1的目錄可讀而不可執行所以無法取得file1的檔案資訊；而file2、file3、file4因為目錄可以執行所以可以順利取得檔案資訊，且從檔案權限中可以看出，即使使用者對檔案的權限是0也依然能夠顯示檔案資訊(file4)
所以要查閱檔案，使用者必須要對檔案的目錄擁有可執行的權限


最後是編輯檔案
直接上結果
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/016.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/017.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/018.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/019.PNG)
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/020.PNG)
會發現file1、file2強制存檔也依然無法成功修改檔案，但是神奇的是file4，強制存檔竟然成功了，明明使用者的權限是0，但其實系統只是把檔案的擁有者和群組換成了當前的使用者，才得以強制存檔成功
![image](https://github.com/boolenboom/107-1-ntcu-linux/blob/HW-3/ADT105136/021.PNG)
可是這樣子為什麼file1、file2不也跟著照做就好了嗎？只要從目錄上就能夠知道為什麼它們無法強制存檔
file1從一開始進入vi就無法讀取到檔案的內容，因為目錄無法執行；而file2雖然能夠讀到檔案內容，但是目錄不能進行寫入而無法轉換擁有者及群組
相對的，因為file4的目錄權限是777，所以能夠利用強制存檔，但是原始的檔案內容也會因此被破壞。