## Hash table (hash function)

Hash table အကြောင်းပြောတော့မယ်ဆိုတော့ hash table ဆိုတာ ဘာလဲကနေစတာပေါ့။
Hash table ဆိုတာ hashing ဆိုတဲ့ technique တစ်ခုကိုသုံးထားပြီးတော့ key နဲ့ value ကို mapping (တွဲ) ထားပေးတဲ့ structure တစ်ခုလို့ ဆိုနိုင်ပါတယ်။ frequency value တွေကို သူ့ရဲ့ associated key တွေနဲ့ တွဲပြီးတော့လည်း သိမ်းပါတယ်။ ကျနော်အရင်က priority queue article ရေးတုန်းက priority queue တွေကို hash table နဲ့ တွဲပြီးအလုပ်လုပ်ပုံကိုလည်းရေးပေးထားပါသေးတယ်။ အောက်က link မှာဝင်ဖတ်ကြည့်လို့ရပါတယ်။ hash table ဘာကြောင့်သုံးရတာလဲ ၊ ဘယ်လိုအသုံးဝင်လဲဆိုတာတွေကို အဲ့ဒီ article ဖတ်လိုက်ရင်နားလည်သွားပါလိမ့်မယ်။
http://bit.ly/2Nfd5Wl

ဒီနေ့တော့ hash table မှာသုံးတဲ့ technique တစ်ခု ဖြစ်တဲ့ hashing အကြောင်းကို ဆွေးနွေးပေးသွားမှာပဲဖြစ်ပါတယ်။

Hash table မှာ key & value map လုပ်မသွားခင်မှာ hashing အရင်လုပ်ရပါတယ်။ ပြောရမယ်ဆိုရင်တော့ key ကို hash လုပ်တာပေါ့၊ hash လုပ်တဲ့နေရာမှာ modulus နဲ့ hash လုပ်ကြည့်တာပေါ့၊ size 10 ခုရှိတဲ့ table မှာဆို hash ကိုတွက်တဲ့ formula ပြီးတိုင်း mod by 10 ဆိုပြီးလုပ်ပြီး တွက်တာပေါ့။ ဥပမာ - key of x ကို hash မယ်ဆိုရင်
F(x) = (square of x - 6x + 9) mod 10 ဆိုပြီး ိhash လုပ်ကြည့်လို့ရပါတယ်။ x နေရာမှာ integer value တွေထည့်ပြီးတွက်ထုတ်ကြည့်မယ်ဆို ၁ ကနေ ၁၀ အတွင်း value တွေထွက်လာလိမ့်ပါမယ်။ တစ်ကယ်တော့ integer မှရယ် hash လုပ်လို့ရတာ မဟုတ်ပါဘူး၊ တစ်ခြား data type တွေကိုလည်း hash လို့ရပါတယ်၊ ဥပမာ string ဆိုရင် သူ့ရဲ့ ASCII value ထုတ်လိုက်မယ်ဆို integer value ပြန်ရပါမယ်၊ hashing function ထဲ ထည့်တွက်လို့ရပါတယ်။

Hash function မှာလည်း သူ့ရဲ့ ကိုယ်ပိုင် properties တွေရှိပါတယ်။
-	အကယ်လို့ F(x) နဲ့ F(y) ရဲ့ result တွေက တူတယ်ဆိုရင် x နဲ့ y ရဲ့ တန်ဖိုးတွေက တူကောင်းတူနိုင်ပါတယ်လို့ ဆိုနိုင်ပေမဲ့ f(x) နဲ့ f(y) result ကမတူဘူးဆိုရင် x and y ရဲ့ value တွေက လုံးဝတူမှာမဟုတ်ပါဘူး။ (ဒီ property ကဘာအသုံးဝင်လဲဆိုတော့ ထားပါတော့ x and y က size ကြီးတဲ့ ဖိုင်တွေပဲထားပါတော့ compare လုပ်ဖို့လိုလာပြီဆို x and y ကိုတိုက်ရိုက် ထိမယ့်အစား သူတို့ရဲ့ hash value ကို compare လုပ်လိုက်တာ ပိုမြန်ပါတယ်။)
-	Hash လုပ်လိုက်တဲ့ value က အမြဲတမ်း deterministic ဖြစ်ရပါမယ်။ ဆိုလိုချင်တာက f(x) ရဲ့ hash value က y ထွက်တယ်ဆို အမြဲတမ်း y ပဲထွက်ရပါမယ်၊ တစ်နည်းအားဖြင့်ဆို constant ဖြစ်ရမယ်လို့လဲဆိုလိုပါတယ်။

ဒါပေမဲ့ တစ်ခုရှိတာက collision ဖြစ်နိုင်တဲ့ case ပါ၊ အပေါ်က ကျနော်ပြထားတဲ့ hash တွက်တဲ့ function မှာဆို (F(x) = (square of x - 6x + 9)) , x ရဲ့ တန်ဖိုးကို 4 နဲ့ 2 နဲ့ ထည့်မယ်ဆို ရလာမယ့်အဖြေက 1 ချင်းတူနေပါတယ်။ ဒီလို case မျိုးဆို collision ဖြစ်တယ်လို့ ပြောရမယ်ပေါ့။ ဒီလိုမျိုး collision တွေဖြစ်လာပြီဆိုရင် ဖြေရှင်းနိုင်ဖို့အတွက်လည်း solution တွေထုတ်ထားပါတယ်။အဲ့ထဲကမှ popular ဖြစ်တာတွေက တော့ separate chaining နဲ့ open address ဆိုပြီးရှိပါတယ်။ နောက် article တွေမှာ အဲ့ဒီ solution အကြောင်းတွေရေးပေးသွားပါမယ်။

Stay Tune!

![Images of hastable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/hash%20function/fig1.%20hash%20function.png)

![Images of hastable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/hash%20function/fig2.%20hash%20function.png)


photos credit to tutorialpoint
