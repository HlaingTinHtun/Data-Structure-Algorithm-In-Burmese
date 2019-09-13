## Fenwick tree (Point Update)

Fenwick tree ရဲ့ range query တွက်နည်းရော point update လုပ်နည်းရော ပြောပြီးပြီဆိုတော့ နောက်ဆုံးအနေနဲ့ အရေးကြီးဆုံး fenwick tree ဘယ်လိုဆောက်လဲဆိုတာ ရေးပေးသွားပါမယ်။ range query တို့ point update တို့မလုပ်ခင်မှာ fenwick tree က အရင်ဆောက်ထားရမှာဖြစ်ပါတယ်။ fenwick tree ကို tree structure အတိုင်းလဲ ဆောက်သွားလို့ရတယ်။ ဒီ article မှာတော့ ဖတ်ရလွယ်အောင်နဲ့ နားလည်ရလွယ်အောင် linear structure နဲ့ ဆောက်သွားပြပါမယ်။

Attach တွဲပေးထားတဲ့ ပုံက ကျနော် နမူနာ ဆွဲပြထားတဲ့ fenwick tree ဖြစ်ပါတယ်။ ဘယ်လိုတွက်ပြသွားလဲဆိုတာ ရှင်းပြသွားပါမယ်။ စာနဲ့ ပုံနဲ့ တွဲပြီး ဖတ်ကြည့်လို့ရတာပေါ့။

![Image of fenwick](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/fenwick(binary%20indexed%20tree)/fenwick%20tree%20construction.png)

တွက်တဲ့နေရာမှာ range value တွေကိုတွက်ပြီးတော့ fenwick value တွေထုတ်သွားပါမယ်။ range value တွက်နည်းတွေကို ရှေ့က article တွေမှာပြန်ကြည့်နိုင်ပါတယ်။ စတွက်ကြည့်ရအောင်။

Range value of index 1 = 1, အပေါ် 1 ဆင့်တတ်ပြီးပေါင်း = 10+(-2) = 8 , index 2 = 8
Range value of index 2 = 2, အပေါ် 2 ဆင့်တတ်ပြီးပေါင်း = 8+ 5 = 13 , index 4 = 13
Range value of index 3 = 1, အပေါ် 1 ဆင့်တတ်ပြီးပေါင်း = 6+13 = 19, index 4 = 19
Range value of index 4 = 4, အပေါ် 4 ဆင့်တတ်ပြီးပေါင်း = 19+2 = 21 , index 8 = 21
Range value of index 5 = 1, အပေါ် 1 ဆင့်တတ်ပြီးပေါင်း = -3+1 = -2 , index 6 = -2
Range value of index 6 = 2, အပေါ် 2 ဆင့်တတ်ပြီးပေါင်း = -2+21 = 19 , index 8 = 19
Range value of index 7 = 1, အပေါ် 1 ဆင့်တတ်ပြီးပေါင်း = 4+19 = 23 , index 8 = 23
Range value of index 8 = 8, အပေါ် 8 ဆင့်တတ်လို့မရတော့တဲ့ အတွက် ignore
Range value of index 9 = 1, အပေါ် 1 ဆင့်တတ်ပြီးပေါင်း = -1+8 = 7 , index 10 = 7

Fenwick tree တွက်ပြီးပြီဆိုတော့ range query ဆွဲတာတို့ point update လုပ်တာတို့ စလုပ်လို့ ရပါပြီ။ မှန်မမှန် proof လုပ်တဲ့အနေနဲ့ sum query တစ်ခုလောက်ဆွဲကြည့်ပါမယ်။

Index 7 ရဲ့ prefix sum ကိုတွက်ကြည့်ရအောင်။ ပုံမှန်အတိုင်းတွက်မယ်ဆိုရင်.
10-2+6+5-3+1+4 = 21 ရပါမယ်

Fenwick နဲ့တွက်ကြည့်မယ်ဆို index 7 ရဲ့ prefix sum ကိုလိုချင်ရင်.
Prefix sum of index 7 = index(7)+ index(6) + index(4) . ps(နာမလည်ရင် ရှေ့ က article တွေပြန်ဖတ်ပါ။)
Prefix sum of index 7 = 4-2+19 = 21 ရပါမယ်။

ကိုယ့်ဘာသာ input data ကို တစ်ခြား ဂဏန်းတွေ စမ်းထည့်ကြည့်ပြီးလဲတွက်ကြည့်လို့ရပါတယ်။ ရေးထားတဲ့ fenwick articles ၃ ခုကိုလည်း ပြန် wrap up လုပ်ပေးလိုက်ပါမယ်။
