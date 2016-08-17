# ProjectTravel
圖像辨識旅遊專案

1.獲取旅行社行程jpPkTours.json
- http://www.ptrtour.com.tw/web_3/major_tour_list.asp
- http://www.startravel.com.tw/outbound/JP/index.html#JP03
- http://www.travel4u.com.tw/Web/Oversea/CountryPage.aspx?PageId=17
</br>

2.建立字典,獲取景點圖
- 清洗行程取出景點 (或日本政府觀光局取得景點:依目的地與主題,或TripAdviser提取:景點中英文,評論,類型)
- HBase:{景點代碼:[景點(別)名],[景點評論],[景點類型],共享行程數,[行程]}
- 字典:1.{景點名:別名}或{景點代碼:景點(別)名}, 2.{景點:行程}, 3.{行程:類型分佈,分數}
- 輸入景點,獲取googleMap景點圖

3.圖片放在HDFS-使用HIPI</br>
- 3.1 安裝HIPI:http://hipi.cs.virginia.edu/gettingstarted.html</br>
        - Gradel:http://www.codedata.com.tw/java/understanding-gradle-3-getting-started/</br>
- 3.2 透過HIPI匯入HDFS:http://hipi.cs.virginia.edu/examples/hibImport.html</br>

4.Django w/ hdfs
- 1.modelLayer vs. viewLayer : modelLayer需要自行定義class(使用套件:連接hdfs,建立資料架構,用資料庫語法操作資料庫), viewLayer僅需定義操作行為(使用套件:連接hdfs,用python取出資料後操作資料內容), 
