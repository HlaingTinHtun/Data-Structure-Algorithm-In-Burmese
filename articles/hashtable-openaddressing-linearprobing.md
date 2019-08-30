## Hash table - Open addressing (Linear Probing)

ပြီးခဲ့တဲ့နေ့တွေက hash table နဲ့ collision ဖြစ်ရင်ဖြေရှင်းဖို့ technique တွေရေးခဲ့ပါတယ်၊ အဲ့ထဲက မှ open addressing ဆိုတဲ့ technique ကိုသုံးတဲ့နေရာမှာ လိုအပ်မယ့် function တစ်ခုဖြစ်တဲ့ linear probing အကြောင်းကို ဒီနေ့ဆွေးနွေးသွားမှာဖြစ်ပါတယ်။ open addressing မှာ ရှိတဲ့ cycle issue ကိုလဲတစ်ပါတည်း ဆွေးနွေးသွားမှာဖြစ်ပါတယ်။

linear function ကိုသုံးထားလို့ linear probing လို့ခေါ်တယ်။ example . p(x) = ax+b (a is !=0) . ဒါပေမဲ့ သတိတစ်ခုချပ်ထားရမှာက cycle issue ကိုပါပဲ၊ cycle issue ရှိနေရင်တော့ ဘယ် probing function မှ မှန်ကန်စွာ အလုပ်လုပ်နိုင်မှာ မဟုတ်ပါဘူး။ အခုပြောနေတာတွေနားမလည်ဘူးဆိုရင်တော့ အောက်မှာပေးထားတဲ့ article တွေအရင်ဖတ်ဖို့အကြံပေးချင်ပါတယ်။ hash table collision ဖြစ်တဲ့ scenario ၊ ဖြေရှင်းနည်းတွေနဲ့ cycle issue အကြောင်းတွေ နားလည်သွားပါလိမ့်မယ်။

Hash table (hashing)
http://bit.ly/2NCd4MH

Hash table (Separate Chaining)
http://bit.ly/2KSdJaN

Hash table (Open Addressing)
http://bit.ly/2ZkEdL8

cycle issue ကိုပြန်trace လိုက်ရမယ်ဆိုရင် cycle issue ဘယ်လိုအချိန်မှာဖြစ်လဲဆိုတာနဲ့ စလိုက်ရအောင်။ eg. အနေနဲ့ p(x) = ax+b ဆိုတဲ့ formula မှာ a ရဲ့ တန်ဖိုးနဲ့ table တစ်ခုရဲ့ size N ကိုယူပြီးတော့ GCD (greatest common denominator) = (GCD(N,a)) တန်ဖိုးကိုတွက်ထုတ်လိုက်လို့ 1 နဲ့ညီနေတယ်ဆိုရင် အဲ့ဒီ probing formula မှန်ကန်စွာအလုပ်လုပ်နိုင်မယ်။ 1 နဲ့ မညီရင်တော့ cycle issue တတ်ပါတယ်။ ဒီနေရာမှာ probing အတွက်ရေးနေတာမို့ GCD အတွက် သက်သက်ကြီးရေးမနေတော့ဘူး၊ GCD calculator လို့ရှာလိုက်ပြီးတွက်ကြည့်လို့ရပါတယ်။ အောက်မှာလဲ ပေးထားပါတယ်။
http://www.alcula.com/calculators/math/gcd/


ဥပမာ တွေနဲ့ စမ်းတွက်ကြည့်ရအောင်။

Table size = 9
Probing function = p(x) = 6x
Max load factor = 0.667 (6/9)
Threshold of the table = N*max load factor = 6 (table size 9 ခန်းရှိပေမဲ့ 6ခန်းပြည့်သွားရင် table resize ထပ်လုပ်ရပါမယ်။)

GCD တွက်ကြည့်လိုက်မယ်ဆို GCD(N,a) = GCD(9,6) = 3 ရပါတယ်။ 1 မဟုတ်တဲ့ အတွက် ဒီ probing function မှာ cycle issue တတ်ပါမယ်။ အောက်မှာကြည့်ရအောင်။

Formula က
p(x) = 6x
index = (h(k)+p(x))mod N ဆိုရင် h(k)ရဲ့ တန်ဖိုးကို 5 လို့သတ်မှတ်ပြီးတွက်ကြည့်ရအောင်
index = (5+0) mod 9 = 5
index = (5+6) mod 9 = 2
index = (5+ 12) mod 9 = 8
index = (5+18) mod 9 = 5
တွေ့တဲ့အတိုင်း cycle issue တတ်သွားမှာပဲဖြစ်ပါတယ်။ GCD တန်ဖိုးက 1 မဖြစ်နေလို့ပါ။
GCD တန်ဖိုးက 1 သာရခဲ့လျှင် cycle issue မရှိဘဲ empty slot တွေကိုရှာနိုင်သွားမှာပါ။ p(x) ရဲ့ ဆ တန်ဖိုး (a တန်ဖိုး) သာ 1 တို့ 4 တို့ဖြစ်ခဲ့မယ်ဆိုရင် GCD တန်ဖိုး 1 ရတဲ့အတွက် cycle issue မရှိနိုင်တော့ပါဘူး။

![Images of hastable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/open%20addressing/linear%20probing.png)

ဒီနေရာမှာနောက်တစ်ခုမှတ်ထားစရာရှိတာက table resizing ပါ၊ အပေါ်မှာရှိတဲ့ ကျနော်တို့ရဲ့ table Threshold က 6 ပါ။ ပြည့်သွားမယ်ဆိုရင် တော့ resize ထပ်လုပ်ဖို့လိုပါတယ်။ double resizing လုပ်လိုက်တယ်ဆိုပါစို့၊ resizing လုပ်ပြီးပြီဆို key and value ကို formula (table size N ကပြောင်းသွားပါပြီ) အတိုင်း ပြန်တွက်ပြီးပြန်ထည့်ပေးဖို့လိုပါတယ်။

နောက် article မှာ open addressing မှာသုံးတဲ့ quadratic function နဲ့အတူပြန်လာခဲ့ပါမယ်။
