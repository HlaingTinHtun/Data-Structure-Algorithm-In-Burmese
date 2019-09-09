## Fenwick tree (Binary Indexed Tree)

Fenwick tree အကြောင်းစပြောတော့မယ်ဆိုရင်တော့ fenwick ကိုဘာကြောင့်သုံးတာလဲ fenwick ကဘာလဲဆိုတာနဲ့ စဆွေးနွေးကြရအောင်။

ဥပမာ တစ်ခုနဲ့ပြောရမယ်ဆိုရင် ကျနော်တို့မှာ array 10 ခန်းရှိတဲ့ data တစ်ခုရှိတယ်ဆိုပါစို့။ လိုချင်တာက range query ပုံစံမျိုးလိုချင်တာ။ (eg. Sum of array index 1 to 7, array အခန်း ၁ ကနေပြီးတော့ ၇ အထိပေါင်းခြင်းရလဒ်). ပေါင်းလို့ရလားဆိုတော့ ရတယ် လေ။ array ၁ ခန်းခြင်းဆီ လိုက်ထောက်ပြီးတော့ ပေါင်းရုံပဲ။ array 1 + array 2 + array 3 etc. ပုံစံမျိုးပေါ့။ ဒါပေမဲ့ တစ်ခုခြင်းဆီလိုက်ထောက်နေရတဲ့အတွက် linear time ကြာတယ်။ ဆိုလိုချင်တာက range သာကြီးလာမယ်ဆိုရင် performance ကလည်း ထပ်တူ နှေးလာလိမ့်မယ်။

အဲ့လို တစ်ခန်းခြင်းဆီလိုက်ထောက်မယ့်အစား prefix sum ဆိုတဲ့ array structure တစ်ခုဆောက်လိုက်မယ်။ array အခန်း ၁၁ ခန်းနဲ့ပေါ့။ အဲ့ဒီ ၁၁ ခန်းမှာ array index တွေကို တစ်ခန်းခြင်းဆီလိုက်ထောက်ပြီး ပေါင်းပြီးသား result တွေကို store လုပ်ထားမယ်။ sum range query လုပ်တော့မယ်ဆို ဥပမာ index 1 to 7 ရဲ့ ပေါင်းလဒ်ကိုလိုချင်ပြီဆို prefix sum လုပ်ထားတဲ့ array ဆီကနေ value of index 7 – value of index 1 ဆို လိုချင်တဲ့ အဖြေကိုရသွားမှာဖြစ်ပါတယ်။ array တစ်ခန်းခြင်းဆီထောက်ပြီးလဲ ပေါင်းစရာမလိုတော့ဘူးပေါ့။ attach တွဲထားတဲ့ example ကြည့်နိုင်ပါတယ်။

![Image of fenwick](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/fenwick(binary%20indexed%20tree)/fig1.%20fenwick%20tree.png)

ဒါဆို ကျနော်တို့မှာ လက်ရှိ normal array နဲ့ prefix sum လုပ်ထားတဲ့ array ဆိုပြီး နှစ်ခုရှိတယ်။ အဲ့ထဲကမှ normal array ထဲက value တစ်ခုကို change ချင်တယ်ဆိုပါစို့ ၊ change လုပ်မယ်ဆိုရင် prefix sum လုပ်ထားတဲ့ array ပျက်သွားပြီတော့ အစအဆုံး sum value တွေကို ပြန်တွက်ပေးဖို့လိုလာပါမယ်။ ဒီနေရာမှာ fenwick tree ဆိုပြီး ဝင်လာတာပါ။ range query တွေလဲဆွဲလို့ရမယ်။ key ကိုလည်း update လုပ်လို့ရမယ်၊ linear time မကြာဘဲနဲ့ performance ကောင်းကောင်းနဲ့ပေါ့။

ဒီ article မှာတော့ fenwick ကိုသုံးပြီးတော့ range query တွက်နည်း ရေးပေးသွားပါမယ်။ fenwick နဲ့ range query လုပ်တော့မယ်ဆိုတော့ least significant bit (LSB) အကြောင်းလေးပါထည့်ပြောသွားလိုက်ပါမယ်။ LSB ဆိုတာ binary number series မှာရှိတဲ့ lowest bit , ညာဘက်ကနေစပြီး count လုပ်ပါတယ်။ ဥပမာ 10001 ဆိုရင် ညာဘက်ကနေစ count ပြီး LSB က 1 နေရာမှာရှိပါတယ်။ 10010 ဆိုရင် 2 နေရာမှာရှိပါတယ်။ 10100 ဆိုရင် 3 နေရာ၊ 11000 ဆိုရင် 4၊ 10000 ဆိုရင် 5 ။ ဒီလောက်ဆိုရင် LSB သိပြီလို့ထင်ပါတယ်။

အပေါ်ကပြောထားတဲ့အတိုင်း ကျနော်တို့မှာ array 10 ခန်းပါတဲ့ data တစ်ခုရှိတယ်ဆိုပါစို့။ index 1 to 10 ကို binary နဲ့ အတူ range value တွေစမ်းတွက်ကြည့်ရအောင်။

Index 10 = 1010 , LSB = 2, ပြီးရင် 2 to the power of LSB - 1(fenwick မှာ base အတွက် 2 ကိုသုံးပါတယ်). ဆိုတော့ 2 to the power of LSB-1 = 2 ရပါတယ်။

Index 9 ဆိုရင် = 1001 , LSB = 1, 2 to the power of 1-1 = 2 power 0 = 1 ရပါတယ်။

အခုလိုဥပမာပေးပြီး တွက်ထုတ်ထားတဲ့ range value တွေကို range query ဆွဲတဲ့ နေရာမှာ ဘယ်လိုသုံးလဲဆိုတာကြည့်ရအောင်။ Index 7 ရဲ့ prefix sum value ကိုလိုချင်တယ်ဆိုပါစို့။

Sum = Index[7] + Index[6] + Index[4] ရပါတယ်။ ဘာလို့လဲဆိုတော့
Index 7 ရဲ့ range value က 1 ပါ။ ဆိုတော့ အောက်တစ်ထစ်ဆင်းပါတယ်။ Index[6] ရပါတယ်၊ သူ့ရဲ့ range value က 2 ရပါတယ်။ အောက်နှစ်ထစ်ဆင်းပါတယ်၊ index[4] ရပါတယ်။ index[4] ရဲ့ range value 4 ရတဲ့အတွက် 0 အထိဆင်းသွားပြီး end ဖြစ်သွားပါတယ်။ attach တွဲထားပေးတဲ့ example ကြည့်လို့ရပါတယ်။

![Image of fenwick](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/fenwick(binary%20indexed%20tree)/fig2.%20calculating%20range%20value.png)

နောက်တစ်ခုအနေနဲ့ index[4] ရဲ့ prefix sum ကိုတွက်ကြည့်ရအောင်။ index[4] ရဲ့ prefix sum က index[4] အတိုင်းပါပဲ။ တစ်ချက်ထဲနဲ့ ပြီးသွားပါတယ်။ efficient ဖြစ်တယ်ဆိုတာ ဒါမျိုးကိုပြောတာပါ။

ဒါဆိုရင် ကျနော်တို့ လိုချင်တဲ့ range query sum value ကိုဘယ်လိုတွက်မလဲရှင်းပါတယ်။ ဥပမာ index 3 to 8 sum value ကိုလိုချင်တယ်ဆိုပါစို့။ index 8 ရဲ့ prefix sum value ရှာမယ်။ index 3 ရဲ့ prefix sum value ရှာမယ်။ ပြီးရင် 8 ထဲက 3 ကိုနှုတ်လိုက်ရင် လိုချင်တဲ့ 3 to 8 range sum value ကိုရပါပြီ။

article ကိုတော့ အတတ်နိုင်ဆုံး နားလည်ရလွယ်အောင်ရေးထားပေးပါတယ်။ နားမလည်လို့ ဆွေးနွေးချင်တာရှိရင် လာပြောလို့ရပါတယ်။ နောက်နေ့ မှာ point update လုပ်တဲ့အကြောင်းရေးပေးသွားပါမယ်။

photos credit to udemy
