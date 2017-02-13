
.. _h2164242e4c6048506f23311549231654:

蒙提霍爾問題
************

蒙提霍爾問題（Monty Hall problem ）來自於一個贈獎遊戲，主持人蒙提霍爾有三個門讓你選，其中一個門後面是汽車，另兩扇門是摃龜門，你選中那扇汽車門，門後汽車就是你的。你選定之後，主持人會開啟另外兩扇門當中的一扇摃龜門，剩下你選的那一個跟另一個可能是汽車也可能是摃龜的門，這時候，你可以決定是否要更換選擇。主持人可能會誘導你選擇摃龜那一扇，也可能不會。問題是，換門或不換哪一個比較好？

這個問題有趣的地方是，它違反直覺。直覺上，一開始三個門後是汽車的機率都是1/3，主持人開啟一個門之後，剩下兩扇門後的機率變成是1/2。換不換門應該不影響中獎機率，但是，實際上，你沒選中的那扇門後是汽車的機率竟然是2/3，也就是說，換門會更可能中獎。這表示你一開始不論是猜哪一扇門，都是比較爛的選擇，怎麼會這樣？

科學Online高瞻自然科學教學平台上這篇「\ |LINK1|\ 」文章內有詳細的說明，用機率說明為什麼換門會更好，以數學來講，這是條件機率的緣故。

.. _h1634483c7822441972316c7301545:

模擬
====

可是，我覺得這件事情還沒有結束。我想應該繼續追究的問題是，到底直覺錯在哪裡？於是，我寫了一段Python的小程式，模擬這個遊戲的過程。


.. code-block:: python
    :linenos:

    #! -*- coding:utf-8 -*-
    # test.py
    #
    # Simulation of "Monty Hall problem"
    # See http://highscope.ch.ntu.edu.tw/wordpress/?p=47158 for details.
    #
    # By Iap, Singuan
    # Feb 13, 2017 
    #
    import random
    class Question(object):
        options = ['A','B','C']
        def __init__(self,idx):
            self.idx = idx
            self.answer = self.options[random.randint(0,len(self.options)-1)]
            self.choice = ''
            self.originChoice = ''
            self.openedOption = ''
            self.win = None
        def choose(self,c):
            self.choice = c
            self.originChoice = c
        def openDoor(self):
            options = self.options[:]
            options.remove(self.answer)
            if self.answer != self.choice:
                options.remove(self.choice)
            self.openedOption = options[random.randint(0,len(options)-1)]
        def switchChoice(self):
            options = self.options[:]
            options.remove(self.choice)
            options.remove(self.openedOption)
            self.choice = options[random.randint(0,len(options)-1)]
        def finish(self):
            self.win = self.choice == self.answer
    
    def generateQueustion(n=10):
        questions = []
        for i in range(n):
            questions.append(Question(i))
        return questions
    
    def main():
        options = Question.options
        n = 10
        questions = generateQueustion(n)
        winCount = 0
        switchCount = 0
        optionsLength = len(options)
        for question in questions:
            question.choose(options[random.randint(0,len(options)-1)])
            question.openDoor()
            #if random.randint(0,1)==0: ## 換不換門的機率一半一半
            if random.randint(0,1)<optionsLength: ## 一定換門
            #if random.randint(0,1)>optionsLength: ## 一定不換門
                question.switchChoice()
                switchCount += 1
            question.finish()
            if question.win: winCount += 1
    
        lines = ['\t'.join(('次數','中獎門','初次選擇','最終選擇','中獎與否'))]
        for question in questions:
            line = [question.idx,question.answer, question.originChoice, question.choice, question.win]
            lines.append('\t'.join(map(lambda x: str(x),line)))
        switchPercent = int(100*float(switchCount)/len(questions))
        lines.append('總次數:%s, 中獎次數:%s, 中獎機率:%s%%, 換門(次數:%s, 比率:%s%%)' % (len(questions),winCount,int(100*float(winCount)/len(questions)), switchCount, switchPercent))
        print '\n'.join(lines)
    
    
    if __name__ == '__main__':
        main()

執行結果如下圖：

\ |IMG1|\ 

在程式的53-56行，可以切換不同的策略。執行幾次之後，的確顯示出換門是比較好的策略。但是，這不是重點，因為在機率計算下，本來就應該這樣，如果不是的話，是程式有BUG。這也不是「用程式證明了數學推導」畢竟用的只是尋常的random函式而已，不能算是嚴格的模擬。

這個程式的重點在於它揭露了「直覺出錯」的原因。或者是說，在寫程式的過程中，我領悟了為什麼（我的）直覺會出錯。關鍵處在於我的直覺沒有考慮到「主持人決定開哪一扇門」這個情境。請看程式中第23行附近的 openDoor 子函數。

.. code:: 

        def openDoor(self):
            options = self.options[:]
            options.remove(self.answer) #不能開中獎門
            if self.answer != self.choice: #不能開你已選擇的那個門
                options.remove(self.choice)#移除此門之後，只剩下一個門可以開
            self.openedOption = options[random.randint(0,len(options)-1)]

當主持人選擇要開啟哪一扇摃龜門的時候，他的選擇很有限，首先一定不能是你選的那一個，其次，一定不能是中獎的那一個，所以，他開門的行為遵守「一定不能開中獎門」的規則，為此系統（我承認無法明確定義此處的「系統」，此處所稱的「系統」係來自直覺）注入一個明確的資訊使得「他不開的那一個是汽車」的機率大增。


.. bottom of content


.. |LINK1| raw:: html

    <a href="http://highscope.ch.ntu.edu.tw/wordpress/?p=47158" target="_blank">蒙提霍爾問題（一）決勝21點</a>


.. |IMG1| image:: static/MontyHallProblem_1.png
   :height: 250 px
   :width: 566 px
