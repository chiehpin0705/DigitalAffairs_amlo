
[產生.keystore 檔]<br>
-步驟1:<br>
以[系統管理員身分]開啟命令提示字元，並切換路徑「cd C:\Program Files\Eclipse Adoptium\jdk-8.0.312.7-hotspot\bin」<br>
-步驟2: 指令：.\keytool -genkey -alias tomcat -keyalg RSA –keysize  2048 -keystore "C:\amlo\cert\ssl\.keystore"<br>
C:\Program Files\Java\jdk1.8.0_221\bin>   .\keytool -genkey -alias tomcat -keyalg RSA –keysize  2048 -keystore "C:\amlo\cert\ssl\.keystore"


[產生憑證請求檔 amlo.csr]<br>


