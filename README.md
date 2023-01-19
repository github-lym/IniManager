讀取*.ini檔案：讀取用的ReadIniFile引數分別是：

要讀取哪個Section  
該Section下要讀取哪個Key  
如果沒有找到這組Section與Key的話，預設回傳第三個引數

```
    IniManager iniManager = new IniManager("D:/test.ini");
 
    iniManager.ReadIniFile("Section_A", "Key_A", "default");
    iniManager.ReadIniFile("Section_A", "Key_B", "default");
```  
  


寫入*.ini檔案：寫入用的WriteIniFile引數分別是：  
要寫入哪個Section  
該Section下要寫入哪個Key  
要寫入的訊息  
```CSharp

    IniManager iniManager = new IniManager("D:/test.ini");
 
    iniManager.WriteIniFile("Section_A", "Key_A", "1");
    iniManager.WriteIniFile("Section_B", "Key_B_1", "2");
    iniManager.WriteIniFile("Section_B", "Key_B_2", "3");
```
**刪除的用法：**  
刪除Key：將寫入的值設為null即可刪除key  
WriteIniFile(Section_A, key, null)  
刪除整個Section：只要將key設為null即可刪除整個section  
WriteIniFile(Section_A, null, null)，Section_A會整個被刪除  
