## Hash table - Open addressing (Double Hashing)

Hash table အကြောင်းရေးနေတဲ့ series ထဲ က open addressing မှာသုံးတဲ့ probing function တစ်ခုဖြစ်ပါတယ်။ အရင် article တွေ ဖတ်ပြီးမှ ဒီ article ဖတ်တာ ပိုအဆင်ပြေပါမယ်။

Hash table (hashing)
http://bit.ly/2NCd4MH

Hash table (Separate Chaining)
http://bit.ly/2KSdJaN

Hash table (Open Addressing)
http://bit.ly/2ZkEdL8

Hash table – Open addressing (Linear Probing)
http://bit.ly/2ZCjbTx

Hash table – Open addressing (Quadratic Probing)
http://bit.ly/2HDVYKe

double hashing လို့ဆိုပေမဲ့ အရှေ့က article တွေလိုမျိုးဖြစ်တဲ့ probing function တစ်ခုပဲဖြစ်ပါတယ်။ သူကတော့ probing formula ထုတ်တဲ့ အချိန်မှာ hashing နောက်တစ်ခုထပ်ထည့်ပြီး probing လုပ်လိုက်သလိုပေါ့။ ဥပမာ
P(key,value) = value*H(key) . H(key)ဆိုတာကတော့ ကျနော်တို့အခုပြောတဲ့ secondary function ပဲဖြစ်ပါတယ်။
Hash table နဲ့သူ့နဲ့ ပတ်သတ်တဲ့ အကျိုးအကြောင်းတွေကိုတော့ ရှေ့ က article တွေမှာ တော်တော်များများပြောပြီးသွားပြီဆိုတော့ ဒီ double hashing article မှာ cycle issue ဖြစ်တဲ့အချိန် ဘယ်လိုကိုင်တွယ်မလဲ နဲ့ အခုသုံးတဲ့ double hasing ကိုဘယ်လိုလုပ်လဲဆိုတာပါပဲ။ ကျန်တာတွေကတော့ ရှေ့ က probing function တွေလုပ်ထုံးလုပ်နည်းနဲ့ အတူတူပါပဲ

Cycle issue ကိုဖြေရှင်းနည်းက linear probing မှာ ရှင်းတာနဲ့ဆင်ပါတယ်။ GCD အားကိုးနဲ့ပါပဲ။ အရင်ဆုံး delta value တစ်ခုထုတ်တယ်။
Delta = 2ndhashfunction mod N , ဒီနေရာမှာ table size N က prime number ဖြစ်နေရပါမယ်။ delta ကို 0 ထွက်လို့မရပါဘူး။ 0 ထွက်ရင် equation ထဲ ထည့်သုံးလိုက်ရင် cycle issue ထဲရောက်မှာကျိန်းသေပါတယ်။ ဆိုတော့ delta value က greater than or equal to 1 and less than N ဖြစ်ရပါတယ်။ ဆိုတော့ နောက်တစ်ဆင့် အနေနဲ့ GCD တန်ဖိုးကိုတွက်တော့မယ်ဆို GCD(delta,N) နဲ့တွက်ပါမယ်။ table size N က prime number ဖြစ်နေတဲ့အတွက် ရလဒ်က 1 ထွက်ပါမယ်။ GCD တန်ဖိုး 1 ရမယ်ဆိုရင် cycle issue ကိုဖြေရှင်းပြီးသားဖြစ်သွားပါလိမ့်မယ်။

Hashing ကိုပြောရမယ်ဆိုရင် double hash လုပ်တဲ့နေရာမှာ လုပ်ရမယ့် value တွေက fundamental blocks တွေပဲဖြစ်ပါတယ်။ ဥပမာ integer, strings, real number စသည်ဖြင့်ပေ့ါ။ fundamental blocks တွေအတွက် hash function သုံးတော့မယ်ဆိုရင် universal hash functions တွေထဲက လှမ်းဆွဲသုံးပါတယ်။ အောက်မှာ wiki link ပါပါတယ်။
https://en.wikipedia.org/wiki/Universal_hashing

![Images of hashtable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/open%20addressing/doublehashing.jpg)
photo credits to udemy

resizing လုပ်တဲ့ technique ကလည်း ကျန်တဲ့ quadratic function တွေနဲ့အတူတူပါပဲ။ ဒါဆိုရင်တော့ hash table ရဲ့ open addressing မှာ popular ဖြစ်တဲ့ probing function သုံးခုလုံးပြီးသွားပြီ။ လက်ရှိမှာတော့ hash table ထဲကို key value တွေ insert လုပ်တဲ့ case နဲ့ပဲပြောထားတာဆိုတော့ နောက် article မှာ removing case ကိုရေးပေးသွားပါမယ်။
