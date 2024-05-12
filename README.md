# 介紹
這是我第一次跑比較完整的資料分析流程，從擷取資料開始，此專案適合新新手參考。</br>
分為以下步驟:
1. 使用python寫爬蟲，擷取下文本(aka. 志祺77 youtube影片標題、觀看數、上片時間)，存成csv檔
2. 使用Exel資料剖析分欄
3. 使用Jieba斷詞、計算各keyword出現次數，存成csv檔
4. 使用Excel觀察資料，找出有興趣的insights
5. 使用Tableau繪製圖表及dashboard


# Python爬蟲
檔案: crawl.ipynb </br>
output: 77yt_titles.csv

# Jieba
檔案: jieba-yt.ipynb </br>
output: 77yt_jieba_result.csv

# Tableau
完成作品: [shasha 77 Youtube Analysis](https://public.tableau.com/app/profile/yi.shan.hsieh/viz/shasha77/Dashboard1)
第一次在Tableau上用中文創作，發現中文最大問題就是字體選擇少，而且在profile頁面thumbnail無法顯示中文，變成框框。

# 參考資料
1. 爬蟲基本code框架都是從這為基礎: [Scrap YouTube titles, views and thumbnails using Selenium and Python, by AI Decoder](https://www.youtube.com/watch?v=VQU58dZEFfo)
   * Notice: Selenium 4 以上版本，已經將executable_path停用，請參考 [TypeError: WebDriver.__init__() got an unexpected keyword argument 'executable_path' in Selenium Python](https://stackoverflow.com/questions/76550506/typeerror-webdriver-init-got-an-unexpected-keyword-argument-executable-p)

2. Jieba新手可以從這篇開始: [Python - 知名 Jieba 中文斷詞工具教學](https://blog.kennycoder.io/2020/02/12/Python-%E7%9F%A5%E5%90%8DJieba%E4%B8%AD%E6%96%87%E6%96%B7%E8%A9%9E%E5%B7%A5%E5%85%B7%E6%95%99%E5%AD%B8/)


# Reflection
1. 由於url是用youtube/video，上片時間我只能擷取到"n個月前" 或 "n年前"，還要研究如何可以取得具體日期。
3. 年份是手動確認各年的分界線，如果可以取到完整日期真的會方便很多。
4. 時間資料太粗也導致最後資料視覺化無法分析到月，只能討論到"年"，所以也使用適用categorical data的長條圖。
