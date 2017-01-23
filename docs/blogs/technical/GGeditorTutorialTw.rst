
.. _h576f1b202351c1687b3d6e431b6254:

Tutorial 繁體中文版
*******************

這份Tutorial以影片的方式，介紹一個專案網站從無到有的過程。

.. _h572187820253c7294643631303029:

步驟行程表
==========


|REPLACE1|

.. _h1634483c7822441972316c7301545:

影片
====

影片會發出聲音，開啟前請先適度調整音量。

\ |IMG1|\ 

本文件使用GGeditor編輯，\ |LINK1|\ 。

.. bottom of content


.. |REPLACE1| raw:: html

    <table cellspacing="0" cellpadding="0" style="width:100%">
    <thead>
    <tr><th style="width:7%;background-color:#666666;color:#ffffff;vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p style="color:#ffffff"><span  style="color:#ffffff">步驟</span></p></th><th style="width:30%;background-color:#666666;color:#ffffff;vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p style="color:#ffffff"><span  style="color:#ffffff">主題</span></p></th><th style="width:63%;background-color:#666666;color:#ffffff;vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p style="color:#ffffff"><span  style="color:#ffffff">說明與相關資料</span></p></th></tr>
    </thead><tbody>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>一</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>安裝GGeditor</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>方法一：（影片上的方法）</p><ol style="list-style:decimal;list-style-image:inherit;padding:0px 40px;margin:initial"><li style="list-style:inherit;list-style-image:inherit">開啟任何一個Google Docs的文件，選擇「外掛程式/取得外掛程式」</li><li style="list-style:inherit;list-style-image:inherit">在搜尋欄輸入 ggeditor 後按 Enter 進行搜尋</li><li style="list-style:inherit;list-style-image:inherit">點選右側的安裝按鈕執行安裝</li></ol><p>方法二：</p><ul style="list-style:disc;list-style-image:inherit;padding:0px 40px;margin:initial"><li style="list-style:inherit;list-style-image:inherit"><a href="https://chrome.google.com/webstore/detail/ggeditor/piedgdbcihbejidgkpabjhppneghbcnp" target="_blank">直接點選本連結</a> （非手機使用者）</li></ul></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>二</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>建立Github的repository</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>請進入<a href="https://github.com/" target="_blank">Github</a>網站進行。使用既有的repository也可以，位必須要建立新的repository。</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>三</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>建立RTD的project網站</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>請進入 <a href="https://readthedcocs.io" target="_blank">RTD(readthedocs) </a>網站進行。本步驟的目的是用Github的repository在RTD創建一個屬於該repository的專案文件網站。</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>四</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>建立Google Docs文件</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>這份文件將成為專案網站的首頁的內容。</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>五</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>把文件Commit到repository</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>在這個步驟中，新的GGeditor將會設定Github帳號。並以該帳號把Google Docs的文件產生的reStrcturedText檔案與文件中的圖片一起commit到Github的repository裡面（在docs 目錄下）</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>六</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>客製RTD project網站</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>為RTD的專案網站設定 conf.py與theme_overrides.css兩個檔案。<a href="http://ggeditor.readthedocs.io/en/latest/how2Readthedocs.html#step-3-conf-py" target="_blank">請點我開啟這兩個檔案的內容範本</a>。</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>七</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>客製RTD project網站的CSS</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>示範用theme_overrides.css客製專案網站的方式。全程可在Github的網站上完成。客製CSS並非必要，但如果需要時，可以參考這裡的作法。</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>八</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>更新Google Docs文件</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>這個步驟示範透過文件更新的方式更新專案網站上的內容。</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>九</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>建立另一個Google Docs文件</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>這個步驟示範建立另一個文件，及在RTD網站上產生新網頁的方式。</p></td></tr>
    <tr><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>十</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>建立側邊欄的章節選單</p></td><td style="vertical-align:Top;padding-top:5px;padding-bottom:5px;padding-left:5px;padding-right:5px;border:solid 1px #000000"><p>專案網站就像一本書，這個步驟示範在RTD網站的首頁上，把其他章節加入側邊欄的方式。</p></td></tr>
    </tbody></table>


.. |LINK1| raw:: html

    <a href="https://docs.google.com/document/d/1pbNOF2GSYliF4X9bsB05tVm-diBGt4Kfys8MudcHJhs/edit?usp=sharing" target="_blank">請點我開啟原始檔</a>


.. |IMG1| image:: static/GGeditorTutorialTw_1.png
   :height: 268 px
   :width: 477 px
   :target: https://youtu.be/wT__Q80ptOw
