
.. _h3942e173f1332963f187c606e6c:

\ |IMG1|\ FuriKanji
*******************

這是幫助日文學習的Chrome擴充功能（外掛）。使用FuriKanji可以知道日文漢字(Kanji)的讀音(振り仮名；Furigana)，只要滑鼠在漢字上點一下，就會連結到辞書上查詢該漢字。

.. _h174fb648377959437b5c1f697c1c40:

問題意識
========

FuriKanji是為了解決開發者本身在網路上自學日文中會遇到的「怎麼唸」與「什麼意思」兩大問題。「Google翻譯外掛」是一個很實用的工具，它有發音功能，它的「日文翻英文」功能也有相當程度的準確性。然而，「Google翻譯外掛」仍有幾個問題：

#. 它雖然有發音，但是日文漢字上沒有注音(Furigana)。

#. 如果漢字上已經有注音，它無法正確選取要翻譯的內文。

#. 它無法連結與辞書查詢作連結。

「Google翻譯外掛」能翻譯全世界的語言，並不是專門為了日文學習而設計，日文學習者要利用「Google翻譯外掛」克服「怎麼唸」與「什麼意思」的兩大問題，需要增加特別的功能。

.. _h1634483c7822441972316c7301545:

功能
====

為了解決上述的問題，於是有了FuriKanji，FuriKanji的功能設計是從學習日文者的角度出發的。FuriKanji跟其他能顯示Furigana的Chrome外掛不同之處是以下的特點：

* 顯示使用者所選擇的日文漢字的讀音(Furigana)。

    * 有別於「IPA Furigana外掛」是顯示網頁上全部日文漢字的讀音，FuriKanji只顯示使用者圈選的文字。這樣可以改善顯示速度，尤其是遇到像是Facebook這種很長很長的網頁時，或者遇到中日文夾雜的網頁時，常常我們只需要顯示部份的漢字讀音。

    * FuriKanji也能顯示在輸入欄位(input, textarea)所選擇的日文漢字。

* 在網頁下方顯示讀音，不影響原始內文。

    * 在內文上的Furigana會導致使用者無法選取該段文字，影響「複製」功能，而且會導致「Google 翻譯外掛」錯誤解讀所要翻譯的文字內容。

* 自動產生漢字查詢連結。

    * 使用者點選顯示Furigana的漢字，會直接連結到辞書網站的查詢頁面。

    * 目前有五個辞書網站可以選擇：ふりがな文庫、Goo、Nifty、Weblio及Yahoo。歡迎提供其他建議。

* 在「Google 翻譯外掛」彈跳出來的顯示視窗上的日文漢字也能顯示Furigana

    * 「Google 翻譯外掛」是一個很棒的外掛，可以知道發音跟意義，對學習日文很有幫助。

    * 但是「Google 翻譯外掛」彈跳出來的顯示視窗上的日文漢字沒有Furigana。FuriKanji改善了這個問題，使用FuriKanji之後，「Google 翻譯外掛」彈跳出來的顯示視窗上的漢字就會有讀音，並且滑鼠一點就可以查字典。

* FuriKanji也是一種Furigana的開關。

    * 有些網站本來就有Furigana，但是這些Furigana一樣會導致「Google 翻譯外掛」錯誤解讀所要翻譯的文字內容。FuriKanji會將網站上的Furigana暫時隱藏起來，讓使用者圈選不到，這樣就可以回復原有的文字複製功能，也能讓「Google 翻譯外掛」正常運作。

    * 隱藏之後使用者可以用滑鼠靠近漢字來顯示該漢字的讀音。

.. _h1634483c7822441972316c7301545:

安裝
====

* \ |LINK1|\ 

.. _h174fb648377959437b5c1f697c1c40:

使用要領
========

* 啟動與關閉：每一個網頁都可單獨開啟或關閉FuriKanji的功能

    * 關閉狀態是藍色小圖\ |IMG2|\ ，此時點一下藍色小圖就會啟動

    * 開啟狀態是紅色小圖\ |IMG3|\ ，此時點一下紅色小圖就會關閉

    * 在同一個網頁上可以開啟又關閉，關閉又開始。

    * 為了使用方便，載入.jp的網址時FuriKanji會自動開啟。

* 標注Furigana

    * 把要標注的漢字選起來像這樣\ |IMG4|\ 

    * 頁面下方會顯示 \ |IMG5|\ 

    * 取消圈選文字三秒之後下方的Furigana顯示版會自動消失。或者點選顯示板右上方的關閉按鈕。

* 與Google翻譯外掛合用時

    * 把要標注的漢字選起來會像這樣\ |IMG6|\ 

    * 按下圈選區下方的圖示後會顯示這樣\ |IMG7|\ 。請注意，必須是Google翻譯外掛上顯示「日文」的文字才會進行Furigana的標注。

* 辞書查詢

    * 將滑鼠移到有Furigana標注的漢字上方後，點選該漢字就可以開啟查詢頁面。

    * \ |IMG8|\ 

    * FuriKanji預設的查詢的辞書是 「ふりがな文庫」。這個網站是Furigana的專門網站，速度快，而且沒有廣告，是很棒的網站。

    * 切換到其他辞書的按鈕會顯示在查詢網站的「查詢」按鈕旁邊。按下綠色按鈕後點選辞書名稱即可。\ |IMG9|\ 

.. _h174fb648377959437b5c1f697c1c40:

相關外掛
========

* \ |LINK2|\ （推薦）

.. _h174fb648377959437b5c1f697c1c40:

測試網站
========

* \ |LINK3|\  。這是NHK News的簡易版，漢字已經有furigana的網站，不需使用IPA Furigana這一類外掛，缺點是無法與Google 翻譯外掛一起使用，因為選擇要翻譯的文字時會連同Furigana一起，造成Google 翻譯外掛的混淆。使用本外掛之後，可以解決這個問題。

* \ |LINK4|\  。這是NHK News網站。需使用IPA Furigana這一類的外掛才會有漢字讀音。或者使用Google 翻譯外掛。如果是使用IPA Furigana會遇到與\ |LINK5|\ 相同的問題，如果是使用Google 翻譯外掛，會遇到Google 翻譯外掛沒有提供Furigana的問題。使用本外掛之後，這兩個問題都可以解決。

* Facebook

.. _h572187820253c7294643631303029:

技術性特點
==========

* 節省資源

    * FuriKanji是一種開關型的外掛，當使用者在網頁上啟動之後才會運作。其他像是「Google 翻譯外掛」是所有網頁都會自動運作，這樣會讓Chrome瀏覽器消耗比較多的系統資源。使用者可以需要的時候才開啟FuriKanji，並且在不需要的時候關閉它。

    * 當使用者離開Chrome，切換到其他應用程式(例如Word)，或者切換到其他網頁（例如Google)，也就是FuriKanji所運作的視窗(frame)失去使用者的焦點(focus)時，FuriKanji會暫時停止運作。這也是為了替Chrome節省系統資源而設計的功能。

* 子網頁(iframe)內仍可運作

    * 子網頁inner-frame是包在主網頁內的網頁，很多外掛無法在子網頁內正常運作，因為這些子網頁經常會有動態創建與消滅的情況，結構上與主網頁有區別。FuriKanji可以在子網頁內正常運作。

    * 小於500x500的子網頁，FuriKanji視為廣告性子網頁，FuriKanji不會運作。

.. _h174fb648377959437b5c1f697c1c40:

已知問題
========

* 連結文字中的日文無法直接用選取，需先「按住ALT鍵」然後再用滑鼠選取。

* Google 翻譯外掛有時會將日文判斷為中文，需手動調整。

* 本外掛發音受到Google TTL的限制，每日有限額，超過之後會無法發聲。

.. _h1634483c7822441972316c7301545:

致謝
====

* https://github.com/hexenq/kuroshiro.js

.. _h174fb648377959437b5c1f697c1c40:

改版紀錄
========


+---------+----------------------------------------------------------------------------------------------------------+
|版本     |主要異動                                                                                                  |
+---------+----------------------------------------------------------------------------------------------------------+
|1.17.5.29|* 為了在Google翻譯外掛提供Furigana，所以單獨提供Furigana功能。如此一來，導致使用者不必再安裝IPA Furigana。|
|         |                                                                                                          |
|         |* 從I.F. Add-on改名為FuriKanji                                                                            |
+---------+----------------------------------------------------------------------------------------------------------+
|1.17.5.26|讓\ |LINK6|\ 可與Google翻譯外掛一起使用。                                                                 |
+---------+----------------------------------------------------------------------------------------------------------+
|1.0      |2017/1/26 首次發布是一個\ |LINK7|\                                                                        |
+---------+----------------------------------------------------------------------------------------------------------+


.. bottom of content


.. |LINK1| raw:: html

    <a href="https://chrome.google.com/webstore/detail/if-add-on/plpdljndcikodkdhcbcbfnbmeplcjdeh" target="_blank">請用Chrome點選開啟: FuriKanji 外掛</a>

.. |LINK2| raw:: html

    <a href="https://chrome.google.com/webstore/detail/google-translate/aapbdbdomjkkjkaonfhkkikfgjllcleb" target="_blank">Google 翻譯外掛</a>

.. |LINK3| raw:: html

    <a href="http://www3.nhk.or.jp/news/easy/index.html" target="_blank">NHK Web News Easy</a>

.. |LINK4| raw:: html

    <a href="http://www3.nhk.or.jp/" target="_blank">NHK Web News</a>

.. |LINK5| raw:: html

    <a href="http://www3.nhk.or.jp/news/easy/index.html" target="_blank">NHK Web News Easy</a>

.. |LINK6| raw:: html

    <a href="https://chrome.google.com/webstore/detail/ipa-furigana/jnnbgnfnncobhklficfkdnclohaklifi" target="_blank">IPA Furigana 外掛</a>

.. |LINK7| raw:: html

    <a href="https://chrome.google.com/webstore/detail/ipa-furigana/jnnbgnfnncobhklficfkdnclohaklifi" target="_blank">IPA Furigana外掛的patch</a>


.. |IMG1| image:: static/I_F_Add-on_1.png
   :height: 29 px
   :width: 29 px

.. |IMG2| image:: static/I_F_Add-on_2.png
   :height: 34 px
   :width: 50 px

.. |IMG3| image:: static/I_F_Add-on_3.png
   :height: 33 px
   :width: 56 px

.. |IMG4| image:: static/I_F_Add-on_4.png
   :height: 44 px
   :width: 388 px

.. |IMG5| image:: static/I_F_Add-on_5.png
   :height: 60 px
   :width: 228 px

.. |IMG6| image:: static/I_F_Add-on_6.png
   :height: 64 px
   :width: 390 px

.. |IMG7| image:: static/I_F_Add-on_7.png
   :height: 144 px
   :width: 296 px

.. |IMG8| image:: static/I_F_Add-on_8.png
   :height: 98 px
   :width: 300 px

.. |IMG9| image:: static/I_F_Add-on_9.png
   :height: 224 px
   :width: 348 px
