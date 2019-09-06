## Hash table – Removing elements (open addressing)

Hash table အကြောင်းရေးနေတဲ့ series ထဲ က hash table ထဲကနေ key တွေ remove လုပ်တဲ့ article ပဲဖြစ်ပါတယ်။ open addressing နဲ့ပဲ ဥပမာ ပြပြီးပြောသွားပါမယ်။ အရင် article တွေ ဖတ်ပြီးမှ ဒီ article ဖတ်တာ ပိုအဆင်ပြေပါမယ်။

##### Hash table (hashing)
http://bit.ly/2NCd4MH
##### Hash table (Separate Chaining)
http://bit.ly/2KSdJaN
##### Hash table (Open Addressing)
http://bit.ly/2ZkEdL8
#####Hash table – Open addressing (Linear Probing)
http://bit.ly/2ZCjbTx
##### Hash table – Open addressing (Quadratic Probing)
http://bit.ly/2HDVYKe
##### Hash table (Open Addressing - Double Hashing)
http://bit.ly/2ktCQGr

ကျနော်တို့ hash table မှာ key value တွေထည့်တော့မယ်ဆိုရင် hash လုပ်ပြီးထည့်တယ်။ collision တွေဖြစ်တဲ့အခါ separate chaining တို့ open addressing တို့ technique တွေသုံးပြီး ဖြေရှင်းကြပါတယ်။ ထည့်တဲ့အချိန်မှာလဲ hash လုပ်ပြီးထည့်တယ်ဆို remove လုပ်တဲ့ အချိန်မှာလည်း hash လုပ်ပြီးပဲremove လုပ်ပါတယ်။ ဆိုလိုချင်တာက hash table ထဲမှာထည့်ဖို့အတွက် key ကို hash လုပ်ပြီး position index ရှာတယ်။ remove လုပ်တဲ့ အချိန်မှာလဲ ဖျက်ရမယ့် position index ကို hash လုပ်ပြီးပဲရှာပါတယ်။ ဒါပေမဲ့လည်း remove လုပ်တာကဒီလောက်ကြီး မရိုးရှင်းပါဘူး။ အောက်မှာ scenario လေးတစ်ခုနဲ့ဆွေးနွေးသွားပါမယ်။

![Image of Abstraction](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/open%20addressing/removing.png)
photos credit to udemy

ကျနော်တို့မှာ table size 5 ခုပါတဲ့ အရာတစ်ခုရှိတယ်ဆိုပါစို့ ။ အခန်း 1(key1, val1) , 2(key2,val2) , 3(key3,val3) မှာ key&value တွေရှိတယ်။ key2 ကိုစမ်းဖျက်ကြည့်ရမယ်ဆို အရင်ဆုံး key2 ကို hash လုပ်ပြီးတော့ position index ကိုရှာပါမယ်။ အကယ်လို့ result က 2 ရတယ်ဆိုရင်တော့ အထဲကို ကြည့်ပြီး key2 သေချာတယ်ဆို ဖျက်မယ်။ အကယ်လို့ 2 မဟုတ်တဲ့ တစ်ခြားတစ်ခုရခဲ့မယ်ဆိုရင် အထဲကိုစစ်ကြည့်မယ်၊ key2 မဟုတ်ဘူးဆို မဖျက်ဘဲနဲ့ ဆက်ပြီးတော့ probing လုပ်ပြီးတော့ key2 ကိုရှာပြီးဖျက်ပါမယ်။ အိုကေ key2 ကိုရပြီ၊ ဖျက်လိုက်ပြီရင် အဲ့ slot index က null ဖြစ်သွားပါတယ်။

Null ဖြစ်သွားရင်ဘာဖြစ်လဲဆိုတော့ Hash table မှာ searching လုပ်တဲ့အချိန်မှာ issue ဖြစ်ပါတယ်။ ဆိုပါတော့ ကျနော်တို့ က key3 ကိုရှာချင်တယ်။ probing လုပ်ပြီးတော့ တစ်ဆင့်ချင်းဆီသွားတယ်။ index 1 ရတယ်၊ စစ်တယ် ၊ key1 တွေ့တယ်၊ probing ဆက်လုပ်တယ်၊ index2 မှာ null ကြီးဖြစ်နေတယ်။ hashtable ရဲ့ သဘောတရားက အဲ့လို null ကို အရင်တွေ့သွားပြီဆို သူ့တို့ရှာမယ့် key3 က မရှိတော့ဘူးလို့ယူဆလိုက်ပါတယ်။ ဆိုတော့ remove လုပ်တဲ့ case မှာ remove ပြီးတိုင်း null မထားဘဲနဲ့ unique marker တစ်ခုထားလိုက်ပါတယ်။

အဲ့ဒီ unique marker ကို tombstone လို့ခေါ်ပါတယ်။ remove လုပ်ပြီးတိုင်း အဲ့ဒီ slot index မှာ tombstone လေးတွေထားခဲ့တယ်။ ဒါဆိုရင် searching လုပ်တဲ့အချိန်မှာ tombstone တွေတွေ့ရင် skip လုပ်ပြီး probing ဆက်လုပ် ဆက်ရှာ၊ ဒါမျိုးလုပ်သွားလို့ရပါတယ်။ tombstone နဲ့ပတ်သတ်ပြီး မှတ်စရာ ၂ မျိုးရှိပါတယ်။

ဒါကတော့ table resizing လုပ်လိုက်တဲ့အချိန်ကျ tombstone တွေအကုန်ပျောက်ပါတယ်။ null တွေပြန်ဖြစ်တယ်ပေ့ါ။ resize လုပ်ပြီးသွားရင် key&value အကုန် hash လုပ်ပြီးပြန်ထည့်တဲ့အတွက် tombstone တွေမလိုတော့တဲ့အတွက်ကြောင့်ဖြစ်ပါတယ်။ နောက်တစ်ချက်က tombstone တွေကို key&value တွေနဲ့ အစားထိုးလို့ရပါတယ်။ ဥပမာပြောရရင် ကျနော်တို့ key တစ်ခုကို lookup (search) လုပ်တော့မယ်ဆိုပါစို့၊ probing လုပ်တယ်၊ စစချင်းမှာတင် tombstone တွေ့တယ်၊ ရှာတာမတွေ့သေးတဲ့ အတွက် probing ထပ်လုပ်ပြီး ထပ်ရှာတယ်။ ၄ ခေါက်မြောက်မှာ ကိုယ်ရှာတဲ့ key တွေ့ပြီးပဲဆိုပါစို့ ၊ lookup လုပ်တဲ့ process အပြီးမှာ ခုနတုန်းက ရှာတဲ့ process မှာ ကိုယ်ရှာတဲ့ key မတွေ့သေးချိန်မှာ တွေ့လိုက်တဲ့ tombstone ရှိတဲ့ slot နေရာမှာ သွားအစားထိုးထားလို့ရပါတယ်။ ဒါဆိုရင်နောင်တစ်ချိန် lookup ပြန်လုပ်တဲ့နေရာမှာ ၄ ကြိမ်ရှာစရာမလိုတော့ဘဲ first try မှာတင် ရှာတွေ့သွားမှာပဲဖြစ်ပါတယ်။

ဒါဆိုရင်တော့ hash table နဲ့ပတ်သတ်ပြီး article တွေစုံသွားပြီလို့ထင်ပါတယ်။ hash table နဲ့ပတ်သတ်တဲ့ article တွေပြန်ပြီး wrap up လုပ်ပေးလိုက်ပါမယ်။
