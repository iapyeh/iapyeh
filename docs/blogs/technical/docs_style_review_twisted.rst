
.. _h83f632e497d4f3c53644e345d5f6e13:

Python Script風格
#################

仿照Twisted的Script風格整理而成。\ |LINK1|\ 

\ |IMG1|\ 

* #3-4: 版權聲明簡單扼要，只有兩行。第一行聲明Copy right holder，第二行請讀者去看另一份LICESE文件。這兩行是以#開頭，不是放在三引號(""")之中。

* #5:空一行

* #6-23: module docs 使用三引號("""), 

    * 第一段讓讀者明瞭這個script的目的與用途。(what and why)

    * 第二段說明這個script在整體系統中運作的要點(how it works)

    * 第三段是提醒使用者時要注意的事項

        * 有可能來自作者的猜測或事後的增補

    * 第四段是說明具體的使用方式(usage)

    * 每一段都空一行，即便只有一行。

    * 在 #19最後是兩個冒號 (::)，這是reStructruedText的語法，會在使得下方的段落內縮。因為下方是一個程式範例。

    *  #21行顯示關於範例的格式開頭是 (內縮）$ （空白）python（空白)

    * 文字多的段落，例如前面兩段，每一行約以80個字元為限。

    * 並不是每一份script內都需要寫很多，如第一、二、三段，視情況而定。也有很簡單的，例如 \ |LINK2|\ 

\ |IMG2|\ 

* system imports、其他module的import 放前面，自己package的import放後面

\ |IMG3|\ 

從#35 -#73, 會看到幾種不一樣的風格。

* 我們來看兩個問題：

    * 是不是每一個class都要寫 class docs?

    * class docs 跟 class 宣告那一行之間要不要有一行空白？

* 這一段有三個class，第一個沒有class docs，第二個class有，但緊貼著class 定義那一行，第三個class也有，但與class宣告那一行之間有一行空白。也許寫這個script的工程師沒有嚴格遵守關於風格的規定，也許是根本就沒有規定。這兩種方式python都能正確解析出 class docs.

* 但是class docs跟下面的段落之間都有空白行。

* 然而，#42-45 的function docs 跟下面的段落之間並沒有空白行。

* #49 , def 宣告跟 return 寫在同一行。

* #58的 __init__,並沒有 docs，function docs並非每一個function都要寫。本段反而使用comment註解其下的程式行。

* #53跟#79都是一行內容，然而#79分成三行來寫。

* 一個class之內每一個區段之間都有空白行。區分 class docs、class property、及每一個method區塊。

\ |IMG4|\ 

..  Hint:: 

    * 寫文件時，「哪些要寫」不需要硬性規定，必要寫的時候才寫即可。
    
    * 關於風格，python對於docs是有規則，但只要能被python解析為docs即可，形式與空行與否無硬性規定。
    
    * docs（宣告下方的三引號）用來做該物件的意義性說明，而comment是用來做程式碼的說明。

\ |LINK3|\ 

版本沿革

* 2018年01月28初版


.. bottom of content


.. |LINK1| raw:: html

    <a href="https://github.com/twisted/twisted/blob/trunk/docs/words/examples/cursesclient.py" target="_blank">原稿</a>

.. |LINK2| raw:: html

    <a href="https://github.com/twisted/twisted/blob/trunk/src/twisted/python/logfile.py" target="_blank">logfile.py</a>

.. |LINK3| raw:: html

    <a href="https://github.com/twisted/twisted/blob/trunk/docs/conf.py" target="_blank">另一種風格的conf.py</a>


.. |IMG1| image:: static/Python_原始碼風格_1.png
   :height: 470 px
   :width: 612 px

.. |IMG2| image:: static/Python_原始碼風格_2.png
   :height: 232 px
   :width: 618 px

.. |IMG3| image:: static/Python_原始碼風格_3.png
   :height: 777 px
   :width: 613 px

.. |IMG4| image:: static/Python_原始碼風格_4.png
   :height: 364 px
   :width: 554 px
