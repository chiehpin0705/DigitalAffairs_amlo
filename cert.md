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

# 憑證GCA申請
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

# 憑證安裝（待ＧＣＡ憑證回覆後再執行）
-步驟1:請至 GTLSCA 網站下載已經壓縮打包好的憑證串鏈檔案，下載網址為 https://gtlsca.nat.gov.tw/download/GTLSCA_All.zip<br>
-步驟2:將 GTLSCA_All.zip 解壓縮，可以得到 「ROOTeCA_64.crt」、「eCA1_to_eCA2-New.crt」和「GTLSCA.crt」共3個檔案<br>
-步驟3:將.keystore 檔、憑證請求檔(amlo.csr)、憑證回覆檔(向GCA申請，為xxx.cerl.)及3個下載檔案(共6個)，放至 C:\amlo\cert\ssl<br>
-步驟4:以[系統管理員身分]開啟命令提示字元，並切換路徑「cd C:\Program Files\Eclipse Adoptium\jdk-8.0.312.7-hotspot\bin」<br>
-步驟5-1:安裝eCA憑證<br>
keytool -import -alias eca -file C:\amlo\cert\ssl\ROOTeCA_64.crt -keystore C:\amlo\cert\ssl\.keystore<br>
-步驟5-2:安裝eCA2憑證<br>
keytool -import -alias eca2 -file C:\amlo\ssl\eCA1_to_eCA2-New.crt -keystore C:\amlo\cert \ssl\.keystore<br>
-步驟5-3:安裝GTLSCA憑證<br>
keytool -import -alias gtlsca -file C:\amlo\ssl\GTLSCA.crt –keystore  C:\amlo\cert \ssl\.keystore<br>
-步驟5-4:匯入 SSL 伺服器應用軟體憑證<br>
keytool –import –alias tomcat –file C:\amlo\cert\ssl\XXXXXXXXXXX.cer –keystore C:\amlo\ssl\.keystore<br>
(其中XXXXXXXXXXX.cer為GCA回覆的檔案)
-步驟6:將產生的.keystore 重新命名為server.keystore(名稱必須完全相同)

# 憑證放置
將server.keystore檔案放至C:\amlo\cert\ssl
