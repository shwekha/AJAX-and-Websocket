# AJAX and Websockets

## Content

1. What is AJAX?

2. What is XML?

3. What is JSON?

4. XML Vs JSON

5. What is Websocket?

## 1. What is AJAX?

> AJAX = Asynchronous Javascript and XML.

“AJAX က programming language တစ်ခု မဟုတ်ဘူး အဲ့တာက web development technique တစ်မျိုးဖြစ်ပြီးတော့ AJAX ကို သုံးပြီး web application တွေက sever တစ်ခုကနေအချက်အလက်များကို ပေးပို့နိုင်သလို ထုတ်ယူနိုင်သည်”

“AJAX ရဲ့ main purpose က web content တွေကို တစ်ပြိုင်နက်ထဲ ပြင်ဆင်မွမ်းမံလို့ ရပြီး web browser ရဲ့ web page တစ်ခုလုံးကို အစကနေ ပြန်လည်ပြုပြင်ရေးစရာမလိုပဲ web page ပေါ် က အကြောင်းအရာ အနည်းငယ်သာ ပြင်ဖို့ လိုအပ်သည်”

---------

### **How does AJAX Work?**

1. Web page ပေါ်မှာ အကြောင်းအရာတစ်ခုကို တင်ထားသည်

2. Request တစ်ခုကို javascript နဲ့ ဖန်တီးလိုက်သည်
3. အဲ့ဒီ request ကို web sever ဆီကို ပေးပို့သည်
4. Sever က request ကို လက်ခံရရှိသည်
5. Sever က web page ကို response တစ်ခု ပြန်ပေးသည်
6. အဲဒီ response ကို javascript နဲ့ ဖတ်ရှု သည်
7. သက်ဆိုင်တဲ့ action ပြန်ပေးသည်

![AJAX photo](https://github.com/shwekha/AJAX-and-Websocket/raw/master/images/Ajax2.PNG)

**AJAX က Javascript နဲ့ အလုပ်လုပ် ပုံ**

```javascript
function loadDOC() {
    const xhttp = new XMLHTTPRequest();
    xhttp.onload = function() {
        document.getElementByID("demo").innerHTML
        = this.responseText;
    }
    xhttp.open("GET", "ajax_info.txt", true);
    xhttp.send();
}
```

-------

## 2. What is XML?

> XML =  eXtensible Markup Language

"XML က HTML လိုမျိုး markup language တစ်ခုဖြစ်သည် သို့သော် HTML သည် ဒေတာကို ပြသရန် ဒီဇိုင်းထုတ်ထားပြီး
XML သည် ဒေတာကို သိမ်းဆည်းရန် နဲ့ ပို့ဆောင်ရန် ဒီဇိုင်းထုတ်ထားသည်"

"Computer System တွေမှာ တွဲသုံးလို့ မရတဲ့ format data တွေ ရှိတယ်
သဟဇာတ မဖြစ်တဲ့ system များ အကြား data ဖလှယ်ခြင်းသည် web developer တွေ အတွက် အချိန်ကုန်စေတဲ့ အလုပ်ဖြစ်တယ်
Data အများအပြားကို လွှဲပြောင်းရမှာဖြစ်ပြီး တွဲသုံးမရသော data များ မကြာခဏ ဆုံးရှုံးရတတ်တယ်"

"XML က plain text format နဲ့ data ကို သိမ်းပြီး independent ဖြစ်တဲ့ Hardware Software နည်းလမ်းနဲ့ data တွေကို သိမ်းဆည်းခြင်း ပေးပို့ခြင်း နဲ့ မျှ‌ေ၀ခြင်း တို့ကို ထောက်ပံ့ မေးတဲ့အတွက် ဒေတာ မဆုံးရှံးပဲ new app နဲ့ new browser တွေကို update လုပ်လို့ ရပါသည်"

 __XML ရဲ့ သမိုင်းကြောင်း__

* XML သည် SGML မှဆင်းသက်လာသည်။
* XML ဗားရှင်း 1.0 ကို ဖေဖော်ဝါရီ 1998 တွင် ထုတ်ဝေခဲ့သည်။
* ဇန်နဝါရီ ၂၀၀၁-IETF အဆိုပြုထားသော စံသတ်မှတ်ချက်သည် XML ​​မီဒီယာ အမျိုးအစားများဖြစ်သည်။
* XML သည် Extensible Markup Language ဖြစ်သည်။
* 1970 - Charles Goldfarb၊ Ed Mosher နှင့် Ray Lorie တို့သည် GML ကိုတီထွင်ခဲ့သည်။
* XML ၏ဖွံ့ဖြိုးတိုးတက်မှုသည် Sun Microsystem တွင် 1996 ခုနှစ်တွင်စတင်ခဲ့သည်။

-------

## 3. What is JSON?

> JSON = Javascript Object Orientation

“JSON က data representation format တစ်ခုဖြစ်ပြီး XML နဲ့ Yaml တို့နဲ့ အတော်လေး ဆင်တူတယ် ။ JSON ကို single APIs and games တွေ အဖြစ် internet တစ်ခွင်မှာ ကျယ်ကျယ်ပြန့်ပြန့် အသုံးပြုကြသည်။”

__JSON ရဲ့ သမိုင်းကြောင်း__

* Douglas Crockford သည် 2000 ခုနှစ်အစောပိုင်းတွင် JSON ဖော်မတ်ကို ဖော်ပြခဲ့သည်။
* တရားဝင်ဝဘ်ဆိုဒ်ကို ၂၀၀၂ ခုနှစ်တွင် စတင်ခဲ့သည်။
၂၀၀၅ ဒီဇင်ဘာတွင် Yahoo! JSON တွင် ၎င်း၏ဝဘ်ဝန်ဆောင်မှုအချို့ကို စတင်ကမ်းလှမ်းသည်။
* JSON သည် 2013 ခုနှစ်တွင် ECMA နိုင်ငံတကာစံဖြစ်လာခဲ့သည်။
* အဆင့်အမြင့်ဆုံး JSON ဖော်မတ်စံကို 2017 ခုနှစ်တွင် ထုတ်ဝေခဲ့သည်။


*JSON က အောက်ပါ အချက်တွေကြောင့် ကျော်ကြားတယ်*

    * Data Representation Format
    * Commonly used for APIs and Configs
    * Lightweight and Easy to Read/Write
    * Integrates Easily with more Languages

*JSON Datatypes*

1. Strings
2. Numbers
3. Booleans
4. Null
5. Arrays
6. Objects
------
## 4. XML Vs JSON

__(1). JSON သည် XML ထက် ပိုကောင်းပါသလား?__
	
	JSON သည် XML ထက် ပိုရိုးရှင်းသော်လည်း XML သည် ပိုအစွမ်းထက်သည်။ အသုံးများသော အပလီကေးရှင်းများအတွက် JSON ၏ တိုတောင်းသော ဝေါဟာရများသည် လိုက်နာရန် ပိုမိုလွယ်ကူသော ကုဒ်ကို ဖြစ်ပေါ်စေသည်။ လုပ်ငန်းတွင်း ကဲ့သို့သော ရှုပ်ထွေးသော ဒေတာဖလှယ်မှု ပတ်၀န်းကျင်ရှိ လိုအပ်ချက်ရှိသော အပလီကေးရှင်းများအတွက်၊ XML ၏ အစွမ်းထက်သော အင်္ဂါရပ်များသည် ဆော့ဖ်ဝဲအန္တရာယ်ကို သိသိသာသာ လျှော့ချနိုင်သည်။

__(2). XML နှင့် JSON မည်သို့ကွာခြားသနည်း?__

	JSON သည် ဒေတာဖလှယ်မှုဖော်မတ်တစ်ခုဖြစ်ပြီး ဒေတာကုဒ်သွင်းခြင်းဆိုင်ရာ သတ်မှတ်ချက်တစ်ခုသာဖြစ်သည်။ XML သည် စိတ်ကြိုက် markup ဘာသာစကားများကို သတ်မှတ်ရန် ဘာသာစကားတစ်ခုဖြစ်ပြီး ဒေတာဖလှယ်ခြင်းထက် အများကြီးပိုပေးပါသည်။ ၎င်း၏ တင်းကျပ်သော အတွေးအမြင်များဖြင့်၊ XML သည် မည်သည့် XML အမျိုးအစားခွဲမဆို XML စာရွက်စာတမ်းများ၏ အချက်အလက်ခိုင်မာမှုကို အခိုင်အမာအတည်ပြုရန် စံတစ်ခုသတ်မှတ်ခဲ့သည်။

__(3). JSON နှင့် XML ကို မည်သည့်အချိန်တွင် အသုံးပြုသင့်သနည်း?__

	JSON သည် ရိုးရှင်းသော အပလီကေးရှင်းများအတွက် အကောင်းဆုံးဖြစ်ပြီး၊ ပတ်ဝန်းကျင်ရှိ ဒေတာဖလှယ်ခြင်းဆိုင်ရာ ရိုးရှင်းသောလိုအပ်ချက်များကို ဖြည့်ဆည်းပေးရန်အတွက် တီထွင်ထုတ်လုပ်ထားပါသည်။ XML သည် လုပ်ငန်းတွင်းကဲ့သို့ ရှုပ်ထွေးသော ဒေတာဖလှယ်မှုဝန်းကျင်ရှိ လိုအပ်ချက်များရှိသည့် အပလီကေးရှင်းများအတွက် အကောင်းဆုံးဖြစ်သည်။

__(4). JSON သည် XML ထက် ပိုလုံခြုံပါသလား?__

	JSON နှင့် XML သည် အခြားအရာများထက် ပိုမိုလုံခြုံသည်မဟုတ်ပါ။နှစ်ခုလုံးအတွက် security က message layer ရဲ့အထက် physical layer မှာ လုပ်ဆောင်သည်။

__(5). JSON က XML ထက် ပိုမြန်ပါသလား?__

	JSON သည် ဒေတာဖလှယ်မှုအတွက် အထူးဒီဇိုင်းထုတ်ထားသောကြောင့် ပိုမိုမြန်ဆန်ပါသည်။ JSON ရဲ့ encoding က တိုတောင်းပြီး၊ အကူးအပြောင်းအတွက် bytes နည်းပါးသည်။ JSON သည် ရှုပ်ထွေးမှု နည်းပြီး၊ လုပ်ဆောင်ချိန်နှင့် မန်မိုရီသည်လည်း နည်းသည်။ XML သည် ဒေတာဖလှယ်ရုံထက် အများကြီးပို၍ ဒီဇိုင်းထုတ်ထားသောကြောင့် နှေးကွေးသည်။

-----

## 5. What is Websocket?

WebSocket သည် single TCP မှ full duplex communication ကို ပံ့ပိုးပေးသည့် ကွန်ပျူတာဆက်သွယ်ရေးပရိုတိုကောတစ်ခုဖြစ်သည်။ WebSocket ပရိုတိုကောကို IETF မှ 2011 ခုနှစ်တွင် RFC 6455 အဖြစ် စံသတ်မှတ်ခဲ့သည်။ ဤပရိုတိုကောကို ဝဘ်အပလီကေးရှင်းများတွင် အသုံးပြုခွင့်ပေးထားသော လက်ရှိ API သတ်မှတ်ချက် WebSockets ဟုခေါ်သည်။

"WebSocket ကို real-time web application မှာ အသုံးပြုသည်။
client ရေးပြီးသွားတာနဲ့ data ကို backend sever ဆီကို ချက်ချင်း ‌ပေးပို့လိုက်တယ်။
Websocket မှာ တူညီတဲ့ connection ကြားမှာ data ကို အဆက်မပြတ် ပေးပို့တဲ့ အနေနဲ့ အသုံးပြုနိုင်သောကြောင့် Websocket က application လုပ်ဆောင်ချက်တွေမှာ လျှင်မြန်ပြီး တိုးတက်လာပါသည်"

___For Example,__

* Gaming application: Game app တွေမှာ အဓိက သတိထားရမဲ့ အချက် က sever ကို data အဆက်မပြတ် ပို့ပေးနိုင်ဖို့နဲ့ Ul မှာ refresh မလုပ်ပဲ screen ပေါ်မှာ ပြောင်းလိုက်တဲ့ action ပေါ်လာ ဖို့ လိုအပ်သည်။Ul သည် ချိတ်ဆက်မှု အသစ်ကို မတည်ဆောက်ပဲ အလိုအလျောက် refresh လုပ်နိုင်တဲ့ အတွက် gaming မှာ အလွန်အသုံး၀◌င်သည်
* Trading website or bitcoin trading: စေ◌ျးနှုန်း အတက်အကျနဲ့ data စီးဆင်းလှုပ်ရှားမှုကို ဖော်ပြရန် အတွက် Websocket ကို အသုံးပြုခြင်းဖြင့် ပိုပြီး မြန်ဆန် လာပါသည်
* Chat application: ချတ်အပလီကေးရှင်းများသည် စာရင်းသွင်းသူများကြားတွင် မက်ဆေ့ချ်ဖလှယ်ခြင်း၊ ထုတ်ဝေခြင်းနှင့် ထုတ်လွှင့်ခြင်းအတွက် ချိတ်ဆက်မှုကို တစ်ကြိမ်သာ တည်ဆောက်ရန် WebSockets ကို အသုံးပြုပါသည်။ ၎င်းသည် မက်ဆေ့ချ်ပေးပို့ခြင်းနှင့် လက်ခံခြင်းနှင့် တစ်ခုမှတစ်ခုသို့ မက်ဆေ့ချ်လွှဲပြောင်းခြင်းတို့အတွက် တူညီသော WebSocket ချိတ်ဆက်မှုကို ပြန်လည်အသုံးပြုသည်။

![Websocket](https://github.com/shwekha/AJAX-and-Websocket/blob/master/images/Ajax1.PNG)

**အခြား HTTP ပရိုတိုကော နှင့် websocket ကြား က ကွာခြားမှု**

**Other HTTP Protocal:**

*New request:*
* Client sends request : Server , Do you have new notification ?
* Server sends response : Client , NO
connection ends

*New request :*
* Client sends request : Server , Do you have new notification ?
* Server sends response : Client , NO
connection ends

*New request :*
* Client sends request : Server , Do you have new notification ?
* Server sends response : Client , NO
connection ends

*New request :*
* Client sends request : Server , Do you have new notification ?
* Server sends response : Client , Yes here you are
connection ends

__ဒီနေရာမှာ request တွေကို မလိုအပ်ပဲ ထပ်ခါထပ်ခါ မေးနေရတာကို သင်တွေ့ပါသလား__

**web-socket**

*connection established :*

* client says : Server , Do you have new notification ?
after xx time passed
* Server says : Yes I have
after xx time passed
* Server says : Yes I have
Client says : Server , send new email if I have

*after xx time passed*

* Server says : now you got new email

__Websocket နဲ့ဆိုရင် request တောင်းတာနဲ့ response ပြန်လို့ အချိန်ကုန်သက်သာပြီး မလိုအပ်တဲ့ အဆင့်တွေ လျှော့ချနိုင်ပါသည်__


