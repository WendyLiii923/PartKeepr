# 離線安裝PartKeepr # 
要備有一台有網路的電腦

## 先在有網路的電腦準備 ##  
### 安裝 PHP ###   
- 下載Windows 7.0.32 版本 (7.0.X或7.1.X)  
  - [php-7.0.32-nts-Win32-VC14-x64.zip](https://windows.php.net/downloads/releases/archives/)  
- 解壓縮到 C:\php  
- 設定環境變數：C:\php 加入 Path  
- cmd測試 php -v  
### 安裝 Composer ###  
- 下載 1.10.26 版本的composer.phar (1.X.X)  
  - https://getcomposer.org/download/  
- cmd測試 php composer.phar --version  
### 下載 PartKeepr 及其依賴 ###  
- 找任意位置下載 PartKeepr 源碼 (假設為C:\path)  
  - cd C:\path  
  - git clone https://github.com/partkeepr/PartKeepr.git  
- 將composer.phar放到C:\path\PartKeepr  
- 下載 vendor/ 依賴  
  - cd C:\path\PartKeepr  
  - php composer.phar install  

## 在離線電腦 ##
- 安裝xampp-windows-x64-7.4.33-0-VC15-installer.exe  
  - 必須安裝：Apache、MySQL/MariaDB、PHP  
  - 推薦安裝：phpMyAdmin  
  - 可選安裝：FileZilla、Mercury、Tomcat  
- 重設root 用戶的密碼  
- 新建資料庫名稱：partkeepr  
- 下載 PartKeepr 的源碼   
  - cd C:\xampp\htdocs  
  - git clone https://github.com/partkeepr/PartKeepr.git  
