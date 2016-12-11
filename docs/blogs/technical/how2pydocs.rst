
.. _ha4453f335a47156e62516a9564b36:

如何寫Python文件
****************

本文說明寫Python程式碼作系統開發時，如何完成一個\ |LINK1|\ 網站。本文預設的讀者是軟體工程師、研發部秘書、產品經理等與程式碼相關的工作者。本文討論與程式碼及其應用系統之文件的格式、製作流程、工具的問題，不討論系統文件內容該有哪些段落、該如何管理與審查、該撰寫哪些條目、該怎麼聲明版權，也不是討論文件內容的措詞、風格、引用格式等等內容的問題。

.. _h1634483c7822441972316c7301545:

前言
====

口語上「寫程式」跟「寫系統」界線模糊，在本文中，寫程式是指開一個文字檔輸入程式碼，寫系統是指用寫程式的方式完成查成某個用途。因為系統可大可小，或許這就是造成語意模糊的地方，本文不以大小區別這兩者，一個系統可能只需要一個程式碼檔案，也可能需要數千個程式碼檔案、圖檔、音樂檔等等。只要程式碼不是用完就丟，而是有寫成文件需求的，都可以算是本文所說的系統，本文的目的在說明如何替系統完成系統文件的製作。

一開始學習寫Python程式，不會遇到寫系統文件的問題，甚至會覺得註解（Comment）沒什麼用途，多半是公司強制要求後才開始勉強寫些註解，寫註解是很多工程師的死穴，甚至會有工程師因為不擅長寫註解反而把公司要求寫文件當成是對他的羞辱。然而，身為一個工程師作系統開發寫程式，無法避免會遇到寫文件的問題。

.. _h1634483c7822441972316c7301545:

註解
====

很多工程師即使接受了寫程式就得寫文件的觀念，但誤以為寫註解就等於寫文件，註解是文件的一個重要的基礎，然而註解只是文件的一部分，註解對於文件，就像ABC字母對於英文單字一樣，單字還要組成句子，而一個系統的文件包含註解，但比註解還要多很多。

高階的程式語言幾乎都會有寫註解的語法。註解是夾在程式碼當中的一段文字描述。有的單獨成一行，有的與程式碼在同一行，有的橫跨數行成為一個區塊。Python的註解有兩種，一種是＃開頭，一種是前後三個雙引號包夾的區塊。註解的內容沒有限制，只要符合註解的語法，不會跟程式碼的其他邏輯部分混淆就可以，也可以說，註解是一塊讓工程師任意發揮的作文區。

這些註解的內容不在程式的邏輯流程當中，基本上註解是寫給人看的。看似無用的註解其實有大用。大用在於，註解也可以給機器看，「系統文件」便是機器去閱讀註解而自動建構起來的\ [#F1]_\ 。

.. _h4b4065777285b5e5d6a11592c71525f:

標注（Markups）
===============

所謂給機器看，就是讓另一個程式從程式碼中的註解產生一份文檔的意思。這種文檔，稱為API 文件（API Document）。這個轉換程式，姑且稱為「文件產生器」。

文件產生器無法從漫無格式的作文當中產生文件，寫註解的工程師必須遵守一定的規則，轉換程式才能取得當中的資訊。遵守這個規則來寫註解的行為稱為「標注」，這個規則稱為「（標注）語法」。

Google在他的Python\ |LINK2|\ （Google Python Style Guide）中，規定了標注語法的要求。標注語法不是程式語法，所以算是一種風格，Python的知名的套件（程式庫）Numpy對於標注語法也訂了一份屬於它自己的風格\ |LINK3|\ 。

風格歸風格，風格之間還是有相同的特性。請想像你是寫文件產生器的工程師，文件產生器的最終目標是產生HTML格式的檔案，你需要從註解文字中區別兩種標注者要傳達的資訊：

（A）標注格式：標注者希望呈現的樣貌、版型(layout)，例如加粗、斜體字、超連結、圖片等。

（B）標注意義：關於註解內容的意義，例如函數名稱，參數名稱，類型等資訊。這些資訊會用來建構文件之間的結構、區分群組、產生選單與文件之間的連結，最終也會套用特定的版型，然後產生HTML。

換回你原來扮演的標注者角色，你的義務是提供這兩種資訊給文件產生器。這樣文件產生器才能替你工作。讓我們更深入了解這兩種標注面向的內涵。

.. _h174fb648377959437b5c1f697c1c40:

標注格式
--------

Python慣例使用reStructruedText作為標注格式。在網路上，可能比較常見的標注格式是 Markdown。Markdown是一種比較具有彈性的標注格式，Github替你自動產生的README.md以及它的Gitbook使用的是Markdown，台灣的Logdown網站是世界知名的部落格編輯網站，也是使用Markdown格式的標注。

關於reStructruedText的討論比較少見，如果你已經知道Markdown, 只要以相同的方式理解reStructruedText即可，這兩者的功能定位是一樣的。reStructruedText只是比較少討論並不表示用得人少，好比家家都有瓦斯，但人們不會天天把瓦斯當話題。粗略地講，reStructruedText的規定比較嚴格，它甚至像Python一樣對於內縮(indentation)有自閉的堅持，相對來講Markdown比較隨和些，Markdown最被稱讚的是它允許直接使用HTML\ [#F2]_\ 。彈性是一種雙面刃，在格式標注上的彈性可能在意義標注上產生各自為政的情況

由於HTML純是為了機讀而設計的，reStructruedText跟Markdown當初是為了能有一種兼具人與機器可讀的目的而產生。

.. _h174fb648377959437b5c1f697c1c40:

標注意義
--------

標注意義主要常見在程式碼註解內，用於產生API文件，尤其是關於模組、物件、函數、參數的意義、用途、類型、待辦事項（TODO）的資訊。下圖是一個使用reStructuredText標注的範例：

\ |IMG1|\ 

此範例示範一個名稱為 example_generator的函式如何在註解中表達函式的功能、參數、參數的意義及回傳值。函式名稱會由文件產生器根據程式語言的語法自動識別，人工標注是其中的 Args:, Yields:, Examples: 這是屬於意義標注，意義標注內容偶爾也會包含有格式標注，例如第二行的\`\`Yields\`\` 則是reStrcturedText的格式標注。你可以\ |LINK4|\ ，或者是這份\ |LINK5|\ 。

.. _bookmark-id-s4syqf18lhw3:

.. _h572187820253c7294643631303029:

文件產生器
----------

「標注意義」跟「標注格式」都是相對於文件產生器而言，上面的案例使用的是Sphinx這個文件產生器。也就說，如果你根據要求的方式寫完之後，將它丟給Sphinx處理，就可以產生可預期的結果。

為了讓你更了解這個概念，請看以下這個範例：

\ |IMG2|\ 

這是一個在javascript程式碼當中，為JSDocs文件產生器而標注的註解。函式的參數是用＠param標注，而上面的Python案例中則使用Args:逐行標記。這個案例取自\ |LINK6|\ 。這種標注的差異並不是Javascript與Python的語言差異，而是這份文件的目的是為了能用JSDoc文件產生器從程式碼產生API文件。換言之，如果你將來預備讓Sphinx替你的javascript產生文件，你也可以在Javascript程式碼當中使用Sphinx可以接受的標注方式，然後由Sphinx產生API文件\ [#F4]_\ 。


..  Note:: 

    如果把Sphinx處理API文件的過程說的更詳細一點，關於意義標注的風格，並不是由Sphinx的核心功能直接處理的，而是由擴充功能先作前處理，把這些註解內容轉換成reStructuredText相對應的標注，然後再由Sphinx作處理，這種流程設計可以讓Sphinx的核心單純化也更彈性化\ [#F5]_\ 。

.. _h572187820253c7294643631303029:

如何寫文件
==========

有上述的基礎概念之後，現在你應該已經了解「如何寫文件的問題」也就等同於「選擇哪一種文件產生器」的問題。一旦決定了使用哪一種文件產生器，只需根據該文件產生器的規定寫文件\ [#F6]_\ 就成了。在Python，目前主流選項是前面提到的Sphinx。如果你去Google 「python document generator」會發現還有其他的文件產生器，例如老牌的pydoc，但為何Sphinx能制霸這個領域呢

因為，系統文件不是只有API文件。

還有「專案文件」，這個概念我們很少談，少到連名字都還沒固定稱法，暫時稱為專案文件，凡是非API的文件，不是用來說明你的程式有哪些模組、有哪些函數呼叫的，都屬於這一類。

舉例而言，\ |LINK7|\ 網站，有一個「首頁」說明這個專案（GGeditor）是什麼、有什麼特性，還有其他為了讓使用者了解如何使用這個工具的Tutorial（導引）, User Guide（使用手冊）, How To（如何）, Examples（範例）等等都不是API文件而是專案文件。GGeditor只是一個小工具，大型系統的專案文件是多如牛毛，而且經常需要改版再改版，不只文字跟圖案，甚至還有影音。程式設計師不只是寫程式，也不只是寫API文件，還要負責撰寫這些專案文件，在人力充沛的開發團隊也許會有PM或秘書負責，然而不論是誰負責，系統文件包括專案跟API文件這兩種是不變的。

這些專案文件該怎麼寫沒有強制規定或國際標準可以遵循，既然最終是用網頁呈現，你直接寫HTML也行。然而，慢慢地你會發現，只有HTML是不夠的，還要有PDF才行，不然要把整份文件列印下來還挺麻煩的。到頭來終究會同意：如果可以只寫一份，然後由那一份去產生其他的格式，是一種比較好的作法。這時候，Sphinx跟reStructuredText又出場了，你用reStructruedText的格式寫一份，然後由Sphinx轉成HTML、PDF、LaTex等各種格式。如此一來，不論是API文件還是專案文件，都用reStructruedText的格式寫註解，都用Sphinx作轉換，寫系統文件只要這一套組合就可以完成，這是比較經濟實惠的作法。

以上所談論的觀念可以總結為以下的圖形表示。

\ |IMG3|\ 

到此，你應該已經了解要寫Python的文件，你必須學會兩件事：

#. reStructuredText的格式要怎麼寫。

#. 如果你負責寫程式的話，還要知道Style Guide的規則是什麼。

如果研發團隊能作做到這兩件事情，剩下的就是Sphinx的事了。


..  Tip:: 

    如果你使用IDE作開發，你的IDE可能有協助使用者使用某些特定風格（規格）寫API文件的功能，可以為你省下不少心力。但身為工程師，你需知道IDE提供給你的風格是哪一種，適用於哪一個文件產生器，並讓團隊成員使用相同的風格，避免將來產生轉檔失敗，必須重寫的問題。

But ! 一旦你開始動手之後，你會發現事情沒那麼簡單。

.. _h76f1d1a949307d363741501d2b5c69:

RTD and Github
==============

Sphinx只是一個應用程式，要有人學習如何使用，還要安裝、執行，然後還要架一個網站把它產生的HTML檔案及附圖放上去。幸好，Sphinx只要用pip安裝就可以輕鬆完成。比較大的困擾是，如果不是資源豐沛的公司，要架設網站是挺耗時費力的，頻寬、網址申請、VM管理還有惱人的資安問題要有對策。如果這件事情有人代勞，而且免費，那該多好？如果你也有這樣的問題，那麼\ |LINK8|\  (RTD)跟Github就能幫助你。

你把文件commit到Github去，RTD的後台就可以從你的Github repository中用Sphinx產生你的系統文件，而且還能全文檢索。也就是說，RTD是一個hosting技術文件的網站。它是免費的\ [#F8]_\ 。使RTD跟Github之後，文件的架構就會變成這樣：

\ |IMG4|\ 


..  Note:: 

    在Github中，檔名以.rst結尾的reStructruedText檔案只能部分性的顯示，所以你在Github看到的.rst檔案內容會有點怪異，讀起來好像很多奇怪的符號，圖形大小也有點不協調。那是正常的現象。

然而，要commit什麼樣的文件呢？不外是上面提到的那兩種：

第一、API文件的部分，commit原始程式碼。

第二、專案文件的部分，commit reStructuredText格式的文字檔。

關於第一點API文件的部分，因為Sphinx是從原始程式檔案中產生文件，你要commit到Github的程式檔。那些程式碼可以自由選擇遵守Google或NumPy制定的註解風格，這兩者風格Sphinx都支持。你可以不提供程式碼內關於運算邏輯的部分，只提供程式碼的註解部分，換言之，只提供interface性質的檔案是可以的。值得一提的是，如果要讓RTD也替你產生API文件，你要在設定檔(conf.py)中宣告，細節可以參考GGeditor提供的\ |LINK9|\ 。

關於專案文件，你只需寫成reStructuredText的格式就行了，是的「只」需要寫成reStructuredText的格式，真的「只」需要寫成reStructuredText的格式！

.. _ha50657a67374f257533a67c68622:

reStructuredText
================

相信你現在已經了解reStructuredText是寫文件這件事情的最後關鍵，因為hosting、轉換等等例行公事全部都有工具跟免費的資源可以幫助你，系統是你的，程式碼是你寫的，只有你自己知道要寫什麼內容，當然是你，肯定是你要寫，這最後一哩就等你把reStructuredText的文件生出來了。那麼 reStructuredText長得什麼樣子呢？

本文並不是reStructuredText的教學，在此僅提供以下幾份相關文件給您參考：

* reStructuredText是Docutils專案下發展出來的，\ |LINK10|\ 。

* 如果覺得讀上面的規格很煩，可以看這一份濃縮版 \ |LINK11|\ 。

* A ReStructuredText Primer的\ |LINK12|\ ，你可以看看reStructruedText長什麼樣子。

* 如果上面的濃縮版還是很難讀，這裡還有\ |LINK13|\ 

* 最完整的資訊在\ |LINK14|\ 

.. _hd1b83d48586e1b393a624e28544946:

練習題
------

在繼續往下讀之前，筆者我建議你實際動手寫看看reStructruedText。有一個很棒的網站，可以實際體會寫reStructuredText的快感！\ |LINK15|\ ，以下是一個小作業，你可以當作練習。


.. admonition:: 練習題

    下圖有三句話，請在\ |LINK16|\ 上用reStructuredText寫看看。\ |IMG5|\ 這三句話中包含一個單行的段落以及兩個清單項目(list item)，清單項目包含純文字以及超連結。

（我在這裡先暫停一個禮拜等你完成練習題）

.. _h174fb648377959437b5c1f697c1c40:

習題解答
--------

這位同學，我希望你是功課寫完之後才來看解答，但我猜你一定沒寫就直接跳看解答。如果是這樣的話，恭喜，你的進度已經超前那些還在寫作業的同學一個禮拜以上。事實上，如果有同學從零開始，根據網路上的reStructuredText資料，一個禮拜內完成的話，我認為這位同學必定是天才\ |IMG6|\ 。

本文正是用reStructuredText發佈在 RTD上的，\ |LINK17|\ ，參考的答案在裡面。不論你有沒有做功課，請點選連結打開來，用五秒鐘的時間捲動看一看，想一想，你可以用什麼工具把你的使用手冊等等系統文件用reStructuredText寫出來。

如果你正在猜想「筆記本、Notepad++、Sublime、Atom、VIM哪一個比較好」的問題，再多告訴你一點關於用reStructuredText寫表格的語法。以下這個表格：


+------+------+
|標題列|標題列|
+======+======+
|HELLO |WORLD |
+------+------+

它的reStructuredText原始碼在此：

.. code-block:: python
    :linenos:

    +---------+---------+
    |標題列   |標題列   |
    +=========+=========+
    |HELLO    |WORLD    |
    +---------+---------+

建議你貼到線上體驗版上去玩一玩，請注意，第二行的中文字不整齊不是錯誤，是它該當如此。

你現在對於「筆記本、Notepad++、Sublime、Atom、VIM哪一個比較好」有答案了嗎？

.. _h28105e656d4d48041184d771d3b4a1a:

GGeditor
========

如果你認真寫過練習題，相信你已經透徹了解用reStructuredText寫文件那種彷彿每根手指骨折裹著石膏的沈重感，那麼哪一種文字編輯器比較好的答案就當然是「以上皆非」。既然你能把這篇長文看到這裡，相信你真心想把文件寫好。認真的人最有福氣！介紹你一個工具，可以節省至少一個月的時間，一個不必懂reStructuredText就可以完成系統文件的工具，GGeditor。

GGeditor是Google Docs的Add-on，它從Google Docs文件產生reStructuredText格式的檔案，你在Google Docs裡面寫文章、寫條列項目、畫表格、貼圖、註腳，然後GGeditor把它轉成reStructuredText。你可以完全不懂reStructuredText。

GGeditor不只是一個reStructuredText的轉換器，還能把產生的reStructuredText檔案Commit到Github。然後RTD就會自動更新你的文件網站。

用Google Docs寫文件有很多好處：

#. Google Docs的協同作業、多人同時編輯、統計圖等功能也都可以利用。

#. Google Docs有很多Add-on可以用，如果你要寫英文文件，Google Docs有拼字檢查，還有作英文Proof-Reading的Add-on可以使用，資源豐富。反觀Gitbook只能寫Markup，而Markup無法作拼字跟文法檢查，所以使用Google Docs寫文件會寫得比較好。

#. 不需要學習Markup語法，就可以立刻上手。寫作的時候不會產生好不容易寫完懶得再修改的問題，可以鼓勵工程師邊做邊寫。

GGeditor可以讓你做到：

* 將段落、連結、表格、項目清單、圖形、註腳直接轉成reStructruedText

* 在文件中呈現Admonition，Directive等模擬區塊，不必記憶成reStructruedText語法

* 直接Commit到Github

下圖為GGeditor插入各種Admonition的選取畫面

\ |IMG7|\ 

下圖使用GGeditor直接把產生的reStructuredText Commit到Github的操作畫面

\ |IMG8|\ 

GGeditor還有一個好處是它可以同時用來產生專案文件與API文件。由於API的說明要放在程式註解中，產生API文件的方式並不是用Google Docs編輯程式碼，而是利用GGeditor的產生reStructruedText後把產生的內容複製到程式碼中貼上。這聽起來有點麻煩，但操作起來熟能生巧，如果你有一邊寫程式一邊寫文件的好習慣，Google Docs本來就已經開好，把每一個函式說明各自放在一個1x1的Google Docs的表格（Table）中，當你把游標放在表格裡面時，GGeditor只轉換該表格的內容而且轉成適合內嵌於註解中的Inline格式，此時你再用單鍵複製到剪貼簿上，貼回IDE中的程式碼就可以。複製到剪貼簿時GGeditor可以替每一行加上# 等程式碼註解的慣用符號(prefix)。

\ |IMG9|\ 

除了放在表格裡面之外，你也可以把要轉換的段落選擇起來，當有選擇區存在時，就跟把游標放在Table裡面一樣，GGeditor只會轉選擇區的部分。

這是\ |LINK18|\ ，以及\ |LINK19|\ 。如果你是RTD的初學者，文件網站上有How To文件引導你\ |LINK20|\ ，讓你的RTD文件網站跟Github可以連動。文件網站上也有How To文件，引導你\ |LINK21|\ ，讓你只要把程式碼Commit到Github，你在RTD的API文件也就自動完成更新。

.. _h1634483c7822441972316c7301545:

總結
====

Python的文件是用下圖所示的方法完成的。這張圖把reStructuredText，Sphinx都隱藏起來了，因為透過這一個程序，你不需要知道底層的技術細節，就可以完成你的系統文件。

\ |IMG10|\ 

附註：這篇在RTD上的長篇大論，當然不是用reStructuredText雕刻出來的，而是用GGeditor轉換的，\ |LINK22|\ 。

.. bottom of content


.. |LINK1| raw:: html

    <a href="http://ggeditor.readthedocs.io/en/latest/index.html" target="_blank">像這樣的文件</a>

.. |LINK2| raw:: html

    <a href="http://google.github.io/styleguide/pyguide.html" target="_blank">程式碼風格指南</a>

.. |LINK3| raw:: html

    <a href="http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_numpy.html" target="_blank">Numpy的規則</a>

.. |LINK4| raw:: html

    <a href="https://github.com/iapyeh/GGeditor/blob/master/backend/apidocsample.py" target="_blank">按這裡看完整的示範程式檔</a>

.. |LINK5| raw:: html

    <a href="http://docutils.sourceforge.net/docutils/statemachine.py" target="_blank">官方版的示範程式檔</a>

.. |LINK6| raw:: html

    <a href="http://google.github.io/styleguide/jsguide.html#jsdoc-tags" target="_blank">Google Javascript 風格指南（Google Javascript Style Guide）</a>

.. |LINK7| raw:: html

    <a href="http://ggeditor.readthedocs.io/en/latest/index.html" target="_blank">GGeditor的文件</a>

.. |LINK8| raw:: html

    <a href="https://readthedocs.org" target="_blank">readthedocs.org</a>

.. |LINK9| raw:: html

    <a href="http://ggeditor.readthedocs.io/en/latest/ApiDoc.html" target="_blank">How to Create API Docs</a>

.. |LINK10| raw:: html

    <a href="http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html" target="_blank">標準規格文件在此</a>

.. |LINK11| raw:: html

    <a href="http://docutils.sourceforge.net/docs/user/rst/quickstart.html" target="_blank">A ReStructuredText Primer</a>

.. |LINK12| raw:: html

    <a href="http://docutils.sourceforge.net/docs/user/rst/quickstart.txt" target="_blank">原始reStructuredText檔</a>

.. |LINK13| raw:: html

    <a href="http://docutils.sourceforge.net/docs/user/rst/cheatsheet.txt" target="_blank">單張版</a>

.. |LINK14| raw:: html

    <a href="http://docutils.sourceforge.net/rst.html" target="_blank">官方網頁</a>

.. |LINK15| raw:: html

    <a href="http://rst.ninjs.org/" target="_blank">請點這裡開啟線上體驗</a>

.. |LINK16| raw:: html

    <a href="http://rst.ninjs.org/" target="_blank">線上體驗版</a>

.. |LINK17| raw:: html

    <a href="https://raw.githubusercontent.com/iapyeh/incubator/master/docs/how2pythondocs.rst" target="_blank">這是本文的reStructruedText檔</a>

.. |LINK18| raw:: html

    <a href="https://chrome.google.com/webstore/detail/ggeditor/piedgdbcihbejidgkpabjhppneghbcnp" target="_blank">GGeditor的安裝網頁</a>

.. |LINK19| raw:: html

    <a href="http://ggeditor.readthedocs.io/en/latest/index.html" target="_blank">GGeditor的文件網站</a>

.. |LINK20| raw:: html

    <a href="http://ggeditor.readthedocs.io/en/latest/ApiDoc.html" target="_blank">如何完成RTD要求的Github設定</a>

.. |LINK21| raw:: html

    <a href="http://ggeditor.readthedocs.io/en/latest/ApiDoc.html" target="_blank">如何設定你的API文件</a>

.. |LINK22| raw:: html

    <a href="https://docs.google.com/document/d/1z67wTux_78RNeA6Mkl2MPyD68h1oX70lv_UY7-B_WiA/edit?usp=sharing" target="_blank">這裡是Google Docs的原始文件</a>



.. rubric:: Footnotes

.. [#f1]  有些編譯器也利用註解標注變數型別進行效能優化。
.. [#f2]  reStructuredText也可以用HTML，但不是「直接使用」。
.. [#f3]  因為這種情況而有了Commondown
.. [#f4]  AutoJs -  https://github.com/lunant/sphinxcontrib-autojs
.. [#f5]  sphinxcontrib-napoleon - https://pypi.python.org/pypi/sphinxcontrib-napoleon
.. [#f6]  這句話有語病。萬不得已的情況下，當然也可以作markup格式之間的轉換。
.. [#f7]  不說sphinx最好是怕阻礙了其他頗為創新的方式，詳見 http://stackoverflow.com/questions/1125970/python-documentation-generator
.. [#f8]  Hosting的部分主要是由佛心來的 `Rockspace <https://www.rackspace.com>`__ 買單。

.. |IMG1| image:: static/how2pydocs_1.png
   :height: 421 px
   :width: 588 px

.. |IMG2| image:: static/how2pydocs_2.png
   :height: 348 px
   :width: 585 px

.. |IMG3| image:: static/how2pydocs_3.png
   :height: 305 px
   :width: 545 px

.. |IMG4| image:: static/how2pydocs_4.png
   :height: 229 px
   :width: 473 px

.. |IMG5| image:: static/how2pydocs_5.png
   :height: 88 px
   :width: 681 px

.. |IMG6| image:: static/how2pydocs_6.png
   :height: 40 px
   :width: 53 px

.. |IMG7| image:: static/how2pydocs_7.png
   :height: 316 px
   :width: 301 px

.. |IMG8| image:: static/how2pydocs_8.png
   :height: 316 px
   :width: 509 px

.. |IMG9| image:: static/how2pydocs_9.png
   :height: 277 px
   :width: 697 px

.. |IMG10| image:: static/how2pydocs_10.png
   :height: 150 px
   :width: 697 px
