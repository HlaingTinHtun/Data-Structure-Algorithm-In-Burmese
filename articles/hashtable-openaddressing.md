## Hash table (Open addressing)

Open addressing ဆိုတာကလည်း hash table မှာ collision ဖြစ်တဲ့အခါကျ ဖြေရှင်းနိုင်တဲ့ solving technique တစ်ခုပဲဖြစ်ပါတယ်။ ရှေ့ က article တွေမှာတော့ hash table အကြောင်းနဲ့ collision ဖြစ်ရင်ဖြေရှင်းနိုင်တဲ့ technique တစ်ခုဖြစ်တဲ့ separate chaining အကြောင်းကိုရေးပေးထားပါတယ်။ အောက်က link တွေမှာဝင်ဖတ်ကြည့်လို့ရပါတယ်။

Hash table (hashing)
http://bit.ly/2NCd4MH

Hash table (Separate Chaining)
http://bit.ly/2KSdJaN

ကျနော်တို့ hash table ထဲထည့်ဖို့အတွက် key ကို hash လုပ်တယ်။ hash result ထွက်လာပြီဆို အဲ့ဒီ result အတိုင်း table ထဲမှာ position ယူလိုက်တယ်။ hash result တူပြီး ကိုယ်ထည့်မယ့် position မှာ value ရှိပြီးသားဆို collision ဖြစ်ပြီ၊ ဒါကပုံမှန် process ပဲ။ open addressing ဘယ်လိုအလုပ်လုပ်လဲဆိုတော့ အဲ့ဒီ position က taken ဖြစ်နေတယ်ဆိုရင် နောက်ထပ် လွတ်မယ့် position တစ်ခုကိုဆက်ရှာဖို့ကြိုးစားတယ်။ ဘယ်လိုရှာလဲဆိုတော့ probing sequence formula တစ်ခုထုတ်ပြီးဆက်ရှာတယ်။ ပုံမှန်အတိုင်းဆို ပထမအဆင့်မှာ key ကို hash လုပ်ပြီးရလာတဲ့ result ကို position index အဖြစ်တန်းသတ်မှတ်ပြီးတော့ table ထဲမှာထည့်တယ်၊ probing sequence ကကျ hash result ရယ် မူလkey ရယ်ကို အသုံးပြုပြီးတော့ သူ့ရဲ့ formula ထဲမှာ နောက်ထပ် position index အသစ်တစ်ခုရနိုင်ဖို့အတွက်တွက်ထုတ်ပေးတယ်။

Probing sequence မှာလည်း အမျိုးမျိုးရှိတယ်။
-	Linear function နဲ့သုံးမယ်ဆို linear probing
-	Quadratic function နဲ့သုံးမယ်ဆို quadratic probing
-	နောက်တစ်နည်းကကျ ပုံမှန်သုံးထားတဲ့ hashing method လိုမျိုးကိုပဲ နောက်ထပ် ထပ်သုံးပြီး position index ကိုတွက်တာ ၊ double hashing လို့လဲခေါ်တယ်။
-	Random number တစ်ခုကို generate လုပ်ပြီးတွက်ထုတ်တဲ့ method မျိုးကိုလဲသုံးလို့ရပါတယ်။

ဒါပေမဲ့ probing sequence ကိုသုံးတဲ့ အချိန်မှာ issue ရှိနိုင်တဲ့ condition ရှိပါတယ်။ cycles issue လို့လဲခေါ်တယ်။ ဘယ်လို issue ဖြစ်တယ်ဆိုတာ ဥပမာတစ်ခု နဲ့ ယှဉ်ပြီးပြသွားပါမယ်။ probing sequence ကဘယ်လိုအလုပ်လုပ်တယ်ဆိုတဲ့ ပုံစံလည်းပြရင်းနဲ့ပေ့ါ။

ကျနော်တို့မှာ slot 12 ခန်းရှိတဲ့ structure တစ်ခုရှိတယ်ပဲဆိုပါစို့၊ (0 to 11)ပေါ့။ slot 0, 4, 8 မှာ data value တွေရှိပြီးသားတွေ။
အိုကေ၊ ပုံမှန်အတိုင်း key ကို hash လုပ်ပြီး data ထည့်တာပေ့ါ။ formula က H(key) = key mod 12 နဲ့ ဥပမာထားလိုက်ပါမယ်။ key ကို number 8 အဖြစ်နဲ့ ထည့်လိုက်မယ်ဆို hash result က 8 ထွက်လာမယ်။ data value က ရှိပြီးသားဖြစ်တဲ့ အတွက် probing sequence ကိုသုံးပြီးတော့ နောက်ထပ်နေရာလွတ်တစ်ခုကို ထပ်ရှာပါမယ်။

Probing sequence အတွက် P(x) = 4x ဆိုပြီး ဥပမာ formula တစ်ခုထားပြီးတော့ position index တွက်မယ့် formula ကို ဒီလို upgrade လုပ်လိုက်ပါမယ်။ x value ကို 0 ကနေ စပြီးတော့ +1 ပေါင်းသွားပြီး ရှာပါမယ်။

Index = H(k) + P(x) mod 12   
Index = 8+0 mod 12 = 8 (number 8 slot မှာ value ရှိတယ်၊ ထပ်ရှာ)
Index = 8+4 mod 12 = 0  (number 0 slot မှာ value ရှိတယ်၊ ထပ်ရှာ  Note: P(x) = 4x)
Index = 8+8 mod 12 = 4 (number 4 slot မှာ value ရှိတယ်၊ ထပ်ရှာ)
Index = 8+12 mod 12 = 8 (number 8 slot မှာ value ရှိတယ်၊ ထပ်ရှာ)

ရလာတဲ့ result ကိုကြည့်မယ်ဆို 8, 0, 4, 8 ဆိုပြီး cycle အတိုင်း loop ပတ်သွားတာကို တွေ့ရမှာပဲဖြစ်ပါတယ်။ ဆိုတော့ probing function မှာ ဒီလို issue တော့ ရှိတယ်၊ သူ့ကိုဖြေရှင်းနိုင်ဖို့အတွက် ကတော့ ကိုယ်သုံးမယ့် probing function မှာသတိထားပြီးတော့ ကြိုတင်တွက်ချက်ခန့်မှန်းထားဖို့လိုအပ်ပါတယ်။ နောက်နေ့ တွေမှာ linear , quadratic function နဲ့ double hashing article တွေနဲ့အတူ cycle issue ကိုပါဖြေရှင်းနည်းနဲ့  ပြန်လာခဲ့ပါမယ်။
