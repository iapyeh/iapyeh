
.. _h3942e173f1332963f187c606e6c:

\ |IMG1|\ FuriKanji
*******************

這是幫助日文學習的Chrome擴充功能（外掛）。使用FuriKanji可以知道日文漢字(Kanji)的注音(振り仮名；Furigana)，只要滑鼠在漢字上點一下，就會連結到辞書上查詢該漢字。

.. _h174fb648377959437b5c1f697c1c40:

問題意識
========

FuriKanji是為了解決開發者本身在網路上自學日文中會遇到的「怎麼唸」與「什麼意思」兩大問題。「Google翻譯外掛」是一個很實用的工具，它有發音功能，它的「日文翻英文」功能也有相當程度的準確性。然而，「Google翻譯外掛」仍有幾個問題：

#. 它雖然有發音，但是日文漢字上沒有注音(Furigana)。

#. 如果漢字上已經有注音，因無法正確選取，導致翻譯的結果不準確。

#. 它無法連結與辞書查詢作連結。

#. 它有時會將日文漢字誤認為中文。

「Google翻譯外掛」能翻譯全世界的語言，並不是專門為了日文學習而設計，日文學習者要利用「Google翻譯外掛」克服「怎麼唸」與「什麼意思」的兩大問題，需要增加特別的功能。

.. _h1634483c7822441972316c7301545:

功能
====

為了解決上述的問題，於是有了FuriKanji，FuriKanji的功能設計是從學習日文者的角度出發的。FuriKanji跟其他能顯示Furigana的Chrome外掛不同之處是以下的特點：

* 在「Google 翻譯外掛」彈跳出來的顯示視窗上的日文漢字也能顯示Furigana

    * 「Google 翻譯外掛」是一個很棒的外掛，可以知道發音跟意義，對學習日文很有幫助。

    * 但是「Google 翻譯外掛」彈跳出來的顯示視窗上的日文漢字沒有Furigana。FuriKanji改善了這個問題，使用FuriKanji之後，「Google 翻譯外掛」彈跳出來的顯示視窗上的漢字就會有讀音，並且滑鼠一點就可以查字典。

    * 當「Google 翻譯外掛」認為要翻譯的內容是中文時，會在旁另外顯示一個「漢字よ」讓使用者快速改變成日文。

* 顯示使用者所選擇的日文漢字的注音。

    * 有別於「IPA Furigana外掛」是顯示網頁上全部日文漢字的注音，FuriKanji只顯示使用者圈選的文字。這樣可以改善顯示速度，尤其是遇到像是Facebook這種很長很長的網頁時，或者遇到中日文夾雜的網頁時，常常我們只需要顯示部份的漢字注音。

    * 對於在輸入欄位(input, textarea)所選取的日文漢字也有作用。

* 連結辞書網站。

    * 使用者點選漢字，會直接連結到辞書網站的查詢頁面。

    * 目前有五個辞書網站可以選擇：ふりがな文庫、Goo、Nifty、Weblio及Yahoo。

* 讓日文注音可以開關

    * 有些網站本來就有Furigana，或者是使用「IPA Furigana外掛」這一類外掛替漢字加上注音之後，然而這些日文注音會導致「Google 翻譯外掛」錯誤解讀所要翻譯的文字內容。FuriKanji會將網站上的Furigana暫時隱藏起來，讓使用者可以圈選原本的日文漢字，使得「Google 翻譯外掛」可以翻譯正確的內容。

    * 隱藏之後使用者可以用滑鼠靠近漢字來顯示該漢字的注音。

    * 使用者也可以透過這個功能測試自己是否在沒注音時也能正確讀出漢字。

.. _h1634483c7822441972316c7301545:

安裝
====

* \ |LINK1|\ 

.. _h174fb648377959437b5c1f697c1c40:

使用要領
========

.. _h2164242e4c6048506f23311549231654:

啟動與關閉：
------------

每一個網頁都可單獨開啟或關閉FuriKanji的功能

* 關閉狀態是藍色小圖\ |IMG2|\ ，此時點一下藍色小圖就會啟動

* 開啟狀態是紅色小圖\ |IMG3|\ ，此時點一下紅色小圖就會關閉

* 在同一個網頁上可以開啟又關閉，關閉又開始。

* 為了使用方便，載入.jp的網址時FuriKanji會自動開啟。

.. _h133554e66c4fc3e492e3325c63:

標注音-- 無「Google翻譯外掛」時
-------------------------------

* 把要標注的漢字選起來像這樣

* \ |IMG4|\ 

* 如果使用者，則FuriKanji會在網頁下方顯示自帶的顯示區：

*  \ |IMG5|\ 

* 取消圈選文字三秒之後下方的顯示區會自動消失。

.. _h133554e66c4fc3e492e3325c63:

標注音-- 有「Google翻譯外掛」時
-------------------------------

* 把要標注的漢字選起來會像這樣

* \ |IMG6|\ 

* 點一下圈選區右下方的小圖示後，「Google翻譯外掛」就會顯示注音，如下圖：\ |IMG7|\ 。

* 如果Google翻譯外掛把日文當中文，請按下右邊的「漢字よ」按鈕修改成日文。

* \ |IMG8|\ 

.. _h174fb648377959437b5c1f697c1c40:

辞書查詢
--------

* 將滑鼠移到有注音的漢字上方後，點選該漢字就可以開啟查詢頁面。

* \ |IMG9|\ 

* FuriKanji預設的查詢的辞書是 「ふりがな文庫」。這個網站是Furigana的專門網站，內容豐富，速度快又沒有廣告，是學習ふりがな很棒的網站。

* 綠色的\ |IMG10|\ 小圖是用來切換到其他辞書查詢的按鈕，它會顯示在辞書原有的「查詢按鈕」右邊。按下這一個按鈕後點選辞書名稱即可連結到該辞書網站。

* \ |IMG11|\ 

.. _h174fb648377959437b5c1f697c1c40:

相關外掛
========

* \ |LINK2|\ （推薦）

.. _h174fb648377959437b5c1f697c1c40:

測試網站
========

* \ |LINK3|\  。NHK News網站。可以測試FuriKanji加持後，有日文注音的「Google 翻譯外掛」。

* \ |LINK4|\  。這是NHK News的簡易版，漢字已經有注音。因為無法正確選擇要翻譯的文字，Google 翻譯外掛的混淆。可以測試FuriKanji暫時「關閉」注音的功能。

* NHK School 。這是NHK的兒童教育網站。很多利用子視窗顯示的影片，可以測試FuriKanji在子視窗運行的能力。

* \ |LINK5|\  上的日文貼文可以用來測試FuriKanji的功能。

.. _h572187820253c7294643631303029:

技術性特點
==========

* 節省系統資源

    * 很多外掛，像是「Google 翻譯外掛」會在使用者瀏覽所有網頁自動運行，使得Chrome消耗比較多的系統資源。FuriKanji是一種開關型的外掛，在網頁上手動啟動之後只會在該網頁上運行。使用者可以需要的時候才開啟FuriKanji，並且在不需要的時候關閉它。

    * 當使用者暫時離開Chrome，切換到其他應用程式(例如Word)，或者切換到其他分頁時，FuriKanji所運行的視框(frame)不再是使用者的焦點(focus)時，FuriKanji會自動暫停以節省系統資源。

* 子網頁(inner-frame)內仍可作用

    * 子網頁是包在主網頁內的網頁，這些子網頁經常會有動態創建與消滅的情況，很多外掛無法在子網頁內運作。FuriKanji具備在子網頁內正常運作的能力。

    * 小於500x500的子網頁，FuriKanji視為廣告性子網頁，FuriKanji不會運作。

.. _h174fb648377959437b5c1f697c1c40:

已知問題
========

* 連結文字中的日文無法直接用選取，需先「按住ALT鍵」然後再用滑鼠選取。

* Google 翻譯外掛有時會將日文判斷為中文，需手動調整。

* 本外掛自帶的發音受到Google TTL的限制，每日有限額，超過之後會無法發聲。

.. _h174fb648377959437b5c1f697c1c40:

回報問題
========

您可以利用「Facebook訊息」將訊息傳給\ |LINK6|\ 

.. _h1634483c7822441972316c7301545:

致謝
====

* \ |LINK7|\ 功能

* \ |LINK8|\  這是一個專門介紹Furigana內容很棒的網站，感謝他們的用心與努力

* \ |LINK9|\  提供自學者非常豐富的學材料

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
|1.17.5.26|讓\ |LINK10|\ 可與Google翻譯外掛一起使用。                                                                |
+---------+----------------------------------------------------------------------------------------------------------+
|1.0      |2017/1/26 首次發布是一個\ |LINK11|\                                                                       |
+---------+----------------------------------------------------------------------------------------------------------+


.. bottom of content


.. |LINK1| raw:: html

    <a href="https://chrome.google.com/webstore/detail/if-add-on/plpdljndcikodkdhcbcbfnbmeplcjdeh" target="_blank">請用Chrome點選開啟: FuriKanji 外掛</a>

.. |LINK2| raw:: html

    <a href="https://chrome.google.com/webstore/detail/google-translate/aapbdbdomjkkjkaonfhkkikfgjllcleb" target="_blank">Google 翻譯外掛</a>

.. |LINK3| raw:: html

    <a href="http://www3.nhk.or.jp/" target="_blank">NHK Web News</a>

.. |LINK4| raw:: html

    <a href="http://www3.nhk.or.jp/news/easy/index.html" target="_blank">NHK Web News Easy</a>

.. |LINK5| raw:: html

    <a href="https://www.facebook.com" target="_blank">Facebook</a>

.. |LINK6| raw:: html

    <a href="https://www.facebook.com/singuan.iap" target="_blank">這個帳號</a>

.. |LINK7| raw:: html

    <a href="https://www.npmjs.com/package/kuroshiro" target="_blank">FuriKanji使用KuroShiro的Furigana API提供Furigana</a>

.. |LINK8| raw:: html

    <a href="https://furigana.info" target="_blank">ふりがな文庫</a>

.. |LINK9| raw:: html

    <a href="http://www3.nhk.or.jp/" target="_blank">NHK</a>

.. |LINK10| raw:: html

    <a href="https://chrome.google.com/webstore/detail/ipa-furigana/jnnbgnfnncobhklficfkdnclohaklifi" target="_blank">IPA Furigana 外掛</a>

.. |LINK11| raw:: html

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
   :height: 88 px
   :width: 238 px

.. |IMG9| image:: static/I_F_Add-on_9.png
   :height: 98 px
   :width: 300 px

.. |IMG10| image:: static/I_F_Add-on_1.png
   :height: 20 px
   :width: 20 px

.. |IMG11| image:: static/I_F_Add-on_10.png
   :height: 224 px
   :width: 348 px
