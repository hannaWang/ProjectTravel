# ProjectTravel
圖像辨識旅遊專案

1.爬取旅行社行程jpPkTours.json
- http://www.ptrtour.com.tw/web_3/major_tour_list.asp
- http://www.startravel.com.tw/outbound/JP/index.html#JP03
- http://www.travel4u.com.tw/Web/Oversea/CountryPage.aspx?PageId=17
</br>

2.建立字典,爬取景點
- 清洗行程取出景點 (或日本政府觀光局取得景點:依目的地與主題,或TripAdviser提取:景點中英文,評論,類型)
- HBASE:{景點代碼:[景點(別)名],[景點評論],[景點類型],共享行程數,[行程]}
- 字典:1..{景點名:別名}或{景點代碼:景點(別)名}, 2.{景點:行程}, 3.{行程:類型分佈,分數}
- 輸入景點,爬取googleMap景點圖

3.圖片放在HDFS-使用HIPI
- 安裝HIPI:http://hipi.cs.virginia.edu/gettingstarted.html
- 透過HIPI匯入HDFS:http://hipi.cs.virginia.edu/examples/hibImport.html

4.
