# <p align="center">出入口管理系統(QR Code)</p>


### 主要功能
         1.QR Code掃描記錄進出人員資料　
         2.管理進出人員歷史資料
         
### 語言
         C#
         
### 套件
         QR Code -> ZXING 
         OpenCV
         
### DES加密法加密身分證字號 
        private string Encode(string encode)//DES加密
        {
            string original = encode;
            string key = "abcdefgh";
            string iv = "12348765";

            DESCryptoServiceProvider des = new DESCryptoServiceProvider();
            des.Key = Encoding.ASCII.GetBytes(key);
            des.IV = Encoding.ASCII.GetBytes(iv);
            byte[] s = Encoding.ASCII.GetBytes(original);
            ICryptoTransform desencrypt = des.CreateEncryptor();
            return BitConverter.ToString(desencrypt.TransformFinalBlock(s, 0, s.Length)).Replace("-", string.Empty);

        }
        
## 掃描頁面
<p align="center">
<img src ="img/scanner.jpg" width = 600>
</p>

## 掃描頁面
<p align="center">
<img src ="img/Staffinfo.jpg" width = 600>
</p>

## 出入記錄查詢頁面
<p align="center">
<img src ="img/Enter&Exit.jpg" width = 600>
</p>

## 員工資料管理頁面
<p align="center">
<img src ="img/StaffinfoM.jpg" width = 600>
</p>

## 員工資料新增頁面
<p align="center">
<img src ="img/newStaff.jpg" width = 600>
</p>

## 系統Log
<p align="center">
<img src ="img/Log.jpg" width = 600>
</p>
