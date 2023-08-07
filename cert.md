# 產生憑證請求檔
[產生.keystore 檔]<br>
-步驟1:<br>
以[系統管理員身分]開啟命令提示字元，並切換路徑「cd C:\Program Files\Eclipse Adoptium\jdk-8.0.312.7-hotspot\bin」<br>
-步驟2: 指令：.\keytool -genkey -alias tomcat -keyalg RSA –keysize  2048 -keystore "C:\amlo\cert\ssl\.keystore"<br>
C:\Program Files\Java\jdk1.8.0_221\bin>   .\keytool -genkey -alias tomcat -keyalg RSA –keysize  2048 -keystore "C:\amlo\cert\ssl\.keystore"<br>


[產生憑證請求檔 amlo.csr]<br>
-步驟:指令：.\keytool -certreq -keystore "C:\amlo\cert \ssl\.keystore" - alias tomcat -file "C:\amlo\cert\ssl\amlo.csr"<br>
C:\Program Files\Java\jdk1.8.0_221\bin>.\keytool -certreq -keystore "C:\amlo\cert \ssl\.keystore" - alias tomcat -file "C:\amlo\cert\ssl\amlo.csr"<br>


[備份keystore檔備和憑證請求檔(.CSR)]<br>
拷貝至<br>
C:\amlo\cert\ssl\.keystore <br>
C:\amlo\cert \ssl\amlo.csr<br>

# 憑證申請
-步驟1:到GCA網站<br>
https://gcp.nat.gov.tw/index.html<br>

-步驟2:點選「評證申請」<br>


-步驟3:點選「TLS類憑證申請」<br>

-步驟4:點選「發文申請」<br>
-步驟5-1:填寫相關資訊<br>
-步驟5-2:網站名稱(Domain Name)如：w ww.cht.com.tw請填下列兩者<br>
https://www.amlo.taichung.gov.tw/<br>
https://amlo.taichung.gov.tw/<br>
-步驟5-3:上傳CSR檔<br>
