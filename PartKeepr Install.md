# 離線安裝PartKeepr # 
要備有一台有網路的電腦(這邊簡稱電腦W)  

## 先在電腦W準備 ##  
### 安裝 PHP ###   
選擇 Non-Thread Safe (NTS) 版本  
https://windows.php.net/download/#php-8.4-nts-vs17-x64  
Zip 下載並解壓縮到 C:\php  
設定環境變數：C:\php 加入 Path  
cmd測試 php -v  
### 安裝 Composer ###  
下載 Composer-Setup.exe並執行安裝  
https://getcomposer.org/download/  
確保選擇 C:\php\php.exe 來運行 Composer  
cmd測試 composer -v  
### 下載 PartKeepr 及其依賴 ###  
找任意位置下載 PartKeepr 源碼  
cd C:\some\path  
git clone https://github.com/partkeepr/PartKeepr.git  
下載 vendor/ 依賴  
cd C:\some\path\PartKeepr  
composer install --prefer-dist --no-dev --ignore-platform-reqs  
打包 vendor/ 及 composer.lock  

## 在離線電腦 ##
安裝xampp-windows-x64-7.4.33-0-VC15-installer.exe  
	必須安裝：Apache、MySQL/MariaDB、PHP  
	推薦安裝：phpMyAdmin  
	可選安裝：FileZilla、Mercury、Tomcat  
重設root 用戶的密碼  
新建資料庫名稱：partkeepr  
下載 PartKeepr 的源碼   
	cd C:\xampp\htdocs  
	git clone https://github.com/partkeepr/PartKeepr.git  
