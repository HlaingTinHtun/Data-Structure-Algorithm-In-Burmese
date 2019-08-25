## hash table (separate chaining)

ပြီးခဲ့တဲ့နေ့က hash table အကြောင်းကို intro ဝင်ပြီးသွားပြီ။ hash table မှာ issue ဖြစ်နေတဲ့ collision အကြောင်းလည်းရေးခဲ့ပါတယ်။ ဒီနေ့တော့ အဲ့လို collision တွေကို ဖြေရှင်းတဲ့ နည်းလမ်းထဲက popular အဖြစ်ဆုံးနဲ့ နားလည်ရလွယ်တဲ့ method တစ်ခုဖြစ်တဲ့ separate chaining အကြောင်းကို ဆွေးနွေးသွားပါမယ်။ ရှင်းရှင်းပြောရင် separate chaining က linked list algorithm ပေါ်ကို မှီငြမ်းပြီးတော့ အလုပ်လုပ်ထားတယ်လို့လဲပြောလို့ရပါတယ်။
ဆိုတော့ ဒီ article ကိုမဖတ်ခင် hash table ရဲ့ introduction နဲ့ linked list အကြောင်းကို ဖတ်ဖို့အကြံပေးချင်ပါတယ်။
##### hashtable -  http://bit.ly/2NCd4MH
##### linked list - http://bit.ly/33LGBsA

Data structure ကိုတစ်ဖြည်းဖြည်းလေ့လာရင်းနဲ့ သိလာရမှာက data structure တစ်ခုနဲ့ တစ်ခုမှာ မှီခိုနေတာကိုတွေ့လာရပါလိမ့်မယ်။ ဥပမာအနေနဲ့ပြောရရင် priority queue မှာ hash table ကိုထည့်သုံးသလို အခုရေးမယ့် separate chaining မှာလည်း linked list ကိုသုံးထားတယ်၊ စသည်ဖြင့် တစ်ခြား အများကြီးရှိပါသေးတယ်။

စကားဦးတွေလည်းများပြီမို့ separate chaining စလိုက်ရအောင်၊ hash table မှာဖြစ်လေ့ရှိတဲ့ collision issue ကိုဖြေရှင်းနိုင်မယ့် strategy တွေထဲကတစ်ခုပဲ ၊ သူ့ရဲ့ ထူးခြားချက်က ဝင်လာသမျှ data node အားလုံးကို တစ်ခုမှဖျက်မပစ်ဘဲနဲ့ collision လည်းမဖြစ်အောင် hash table ရဲ့ data structure လည်းမပျက်အောင် ဖန်တီးပေးထားနိုင်တယ်၊ linked list algorithm ကို အခြေခံပြီး ဖြေရှင်းပေးထားပါတယ်။

ဖြေရှင်းနည်းကတော့ ရှင်းတယ်။ ကျနော်တို့ ပုံမှန်အတိုင်း hash table ထဲကို hash လုပ်တယ်၊ value တွေထည့်တယ်။ hash လုပ်လိုက်တဲ့ result က table ထဲမှာရှိပြီးသားဆိုရင် collision ဖြစ်တော့မယ်ပေါ့၊ အဲ့အချိန်ကျရင်လည်း table ထဲက hash result တူတဲ့ node ရဲ့ နောက်မှာပဲ link တွဲပြီးတော့ ထည့်လိုက်တယ်၊ linked list က data insertion လုပ်ပုံနဲ့ အတူတူပါပဲ။ insertion လုပ်တဲ့ case အတွက် ပုံနှစ်ပုံ attach တွဲပေးထားပါတယ်။ ကြည့်ကြည့်ပါ။

### fig 1 example
![Images of hastable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/separate%20chaining/fig1.%20insertion%20as%20linked%20list.png)

### fig 2 example

![Images of hastable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/separate%20chaining/fig2.%20insertion%20as%20linked%20list.png)

Insert လုပ်ပြီးသား data node တွေကို ပြန် ဆွဲထုတ်မယ် (lookup) လုပ်တော့မယ်ဆိုလဲရှင်းတယ်၊ data ကို hash လုပ်မယ်၊ hash result က 4 လို့ရလာပြီပဲဆိုပါတော့၊ no 4 slot မှာသွားကြည့်မယ်၊ သွားကြည့်တာတော့ ဟုတ်ပါပြီ၊ ကျနော်တို့ လိုချင်တဲ့ node မှန်းဘယ်လိုသိနိုင်မလဲပေါ့၊ hash value ကလည်းတူနေတာဆိုတော့ ၊ ကြည့်လို့ရပါတယ်၊ ဘာလို့လဲဆိုတော့ insert သွင်းတုန်းက hash value တစ်ခုတည်းသွင်းလိုက်တာ မဟုတ်ပါဘူး၊ တစ်ခြားတန်ဖိုးတွေလဲပါပါတယ်၊ ဥပမာ- လူတစ်ယောက်ရဲ့ data ဆို name, age, nrc စသည်ဖြင့် ရှိနိုင်တဲ့အတွက် အဲ့ဒီ param တွေနဲ့ပါတိုက်စစ်လို့ရပါတယ်။ ပုံတွဲပေးထားပါတယ်။

### fig 1 example

![Images of hastable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/separate%20chaining/fig1.%20selecting%20the%20node.png)

### fig 2 example

![Images of hastable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/separate%20chaining/fig2.%20selecting%20the%20node.png)

Remove လုပ်မယ်ဆိုလဲ lookup လုပ်တဲ့အတိုင်းပဲ သွားပြီးတော့ lookup လုပ်မယ့် option အစား linked list ကို ဖျက်ချလိုက်ရုံပါပဲ။ separate chaining မှာ linked list မှရယ်မဟုတ်ဘူး၊ တစ်ခြား algorithm တွေနဲ့လဲ အစားထိုးလို့ရတယ်၊ like array, binary tree စသည်ဖြင့် သုံးလို့ရတယ်၊ ဒါပေမဲ့ complexity level က linked list ထက်စာရင် ပိုရှုပ်တဲ့ အတွက် linked list ကိုပဲ အသုံးပြုကြတာ များပါတယ်။

photos credit to udemy
