# [洗錢資恐風險評估系統(https://www.amlo.taichung.gov.tw/)](https://www.amlo.taichung.gov.tw/)
* AP主機(xxx.xxx.2.54)、DB主機(xxx.xxx.4.42)
* ISMS-日誌備份(每個月備份一次)<br>
  一、因資安法及本局ISMS要求，所以要進行日誌的保存。<br>
  二、含application、secruity、system日誌的備份。<br>
  三、來源：%SystemRoot%\System32\winevt\Logs、目的：D:\EventLog_Backup。註：目前因為儲存空間都還夠，所以我是沒有把舊的刪除，都會保留下來<br>
  四、AP主機![AP主機](https://github.com/chiehpin0705/DigitalAffairs/blob/main/Log%E5%82%99%E4%BB%BD_2-54.png)<br>
        DB主機![DB主機](https://github.com/chiehpin0705/DigitalAffairs/blob/main/Log%E5%82%99%E4%BB%BD_4-42.png)<br>
* ISMS-資料庫備份(每個月備份一次)<br>
  一、為避免系統資料庫異常，故進行資料庫備份。<br>
  二、[Microsoft參考文件](https://learn.microsoft.com/zh-tw/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16)<br>
  三、<br>SSMS:步驟1<br>![SSMS:步驟1](https://github.com/chiehpin0705/DigitalAffairs/blob/main/DB%E5%82%99%E4%BB%BD_4-42_p1.png)<br>
      SSMS:步驟2<br>![SSMS:步驟2](https://github.com/chiehpin0705/DigitalAffairs/blob/main/DB%E5%82%99%E4%BB%BD_4-42_p2.png)<br>
  四、DB主機![DB主機](https://github.com/chiehpin0705/DigitalAffairs/blob/main/DB%E5%82%99%E4%BB%BD_4-42.png)
* 憑證產製及申請(每年一次)<br>
  一、因Domain Name需配合憑證，且無廠商直接協助，故需自行產製並申請。<br>
  二、command line介面。<br>
  三、AP主機、DB主機的桌面，都有放廠商當初的手冊![AP主機、DB主機的桌面，都有放廠商當初的手冊](https://github.com/chiehpin0705/DigitalAffairs/blob/main/%E4%B8%BB%E6%A9%9F%E6%A1%8C%E9%9D%A2%E5%B0%B1%E6%9C%89%E6%96%87%E4%BB%B6.png)<br>
      可參閱![可參閱](https://github.com/chiehpin0705/DigitalAffairs/blob/main/%E6%86%91%E8%AD%89.png)
* 弱點掃描修補<br>
  一、因為廠商直接協助，故需自行處理。<br>
  二、針對主機弱點需自己尋求解法; 針對網頁弱點則尋求廠商更版程式。 
* Tomcat更版<br>
  一、因無廠商直接協助，故需自己作業。<br>
  二、進行相關備份後進行升版。<br>
  三、廠商會給更版手冊，照著做就好。<br>
* 突發事件處理<br>
  一、因廠商為中央洗錢辦公室委外廠商，並不直接聽令於我們。而洗錢辦公室人員似乎皆非資訊人員，講什麼聽不懂什麼。可能只能請他們直接拿合約條款請廠商盡速處理問題。
  二、中央合約對廠商的約束力亦不高，要花時間與中央與廠商溝通，且廠商似不會直接根除問題。   
* 洗錢辦的議而無決<br>
  一、109年9月26日來文通知9月29日開會(當時有事無法出席參加)，事後完全無會議記錄。過了3個月後再詢問亦無會議記錄。<br>
  二、111年8月經技術服務中心通知，發生無效的存取控管事件後，洗錢辦原本電話中允諾會函文各縣市要求進行系統版本更新，但最後也都無聲無息。 
* GCB導入<br>
  一、廠商回覆可全數套用。<br>
  二、因為對廠商說法有疑慮，所以還沒全數套用。<br>
  三、加上使用的人少，難以發覺受影響的項目。
* 廠商-汎宇電商 02-2785-8898<br>
  一、專案經理   侯小姐 #662 kitty@universalec.com<br>
  二、系統分析師 陳先生 #220 kevin.chen@universalec.com<br>
  三、系統分析師 呂先生 #647 ginola@universalec.com<br>
  四、客服專線 客服人員 0800-588-889 cs@universalec.com<br>
* 行政院洗錢防制辦公室 02-2322-2618<br>
  一、諮詢研究員 張小姐 #204 ypchang@ey.gov.tw<br>
