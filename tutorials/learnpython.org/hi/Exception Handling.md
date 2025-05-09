जब प्रोग्रामिंग करते हैं, तो गलतियाँ होती हैं। यह जीवन का एक तथ्य है। शायद उपयोगकर्ता ने गलत इनपुट दिया। हो सकता है कि कोई नेटवर्क संसाधन उपलब्ध न हो। हो सकता है कि प्रोग्राम की मेमोरी खत्म हो गई हो। या प्रोग्रामर ने भी गलती कर दी हो!

Python की त्रुटियों का समाधान अपवाद हैं। आपने पहले अपवाद देखा होगा।

    print(a)
    
    #error
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'a' is not defined

ओह! 'a' वेरिएबल को मान असाइन करना भूल गए।

लेकिन कभी-कभी आप नहीं चाहते कि अपवाद पूरी तरह से प्रोग्राम को रोक दें। आप कुछ विशेष करना चाह सकते हैं जब कोई अपवाद उत्पन्न होता है। यह *try/except* ब्लॉक में किया जाता है।

यहाँ एक साधारण उदाहरण है: मान लीजिए कि आप एक सूची का अनुक्रमण कर रहे हैं। आपको 20 संख्याओं पर अनुक्रमण करने की आवश्यकता है, लेकिन सूची उपयोगकर्ता इनपुट से बनी है, और उसमें 20 संख्याएँ नहीं हो सकती हैं। सूची के अंत में पहुँचने के बाद, आप बस बाकी संख्याओं को 0 के रूप में समझाना चाहते हैं। आप यह इस तरह कर सकते हैं:

    def do_stuff_with_number(n):
        print(n)
    
    def catch_this():
        the_list = (1, 2, 3, 4, 5)
    
        for i in range(20):
            try:
                do_stuff_with_number(the_list[i])
            except IndexError: # Raised when accessing a non-existing index of a list
                do_stuff_with_number(0)
    
    catch_this()

देखा, यह बहुत कठिन नहीं था! आप किसी भी अपवाद के साथ ऐसा कर सकते हैं। अपवादों को संभालने के अधिक विवरण के लिए, [Python Docs](http://docs.python.org/tutorial/errors.html#handling-exceptions) से आगे नहीं देखें।

Exercise
--------

सभी अपवादों को संभालें! पिछले पाठों को याद करें ताकि अभिनेता का अंतिम नाम वापस किया जा सके।