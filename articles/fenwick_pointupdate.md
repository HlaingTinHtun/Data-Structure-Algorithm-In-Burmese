## Fenwick tree (Point Update)

အရှေ့က ရေးခဲ့တဲ့ topic မှာ fenwick tree ရဲ့ intro နဲ့ sum range query တွက်နည်းကိုပြောပြပေးခဲ့ပါတယ်။ အခု article မှာတော့ မူလရှိပြီးသား array မှာ array value ကိုပြောင်းချင်ရင် fenwick မှာဘယ်လိုလုပ်လဲဆိုတာကိုပြောပြပေးသွားပါမယ်။ အရင် article ကို အောက်က link မှာ ဖတ်လို့ရပါတယ်။
http://bit.ly/2lDTvaO

ဒီနေရာမှာပြောစရာရှိတာက range query ပဲတွက်တွက် point update ပဲလုပ်လုပ် range value တန်ဖိုးကိုအရင်တွက်ဖို့လိုပါတယ်။ တွက်နည်းကိုလည်း အရင် article မှာရေးပေးခဲ့ပါတယ်။ revision ပြန်တဲ့အနေနဲ့ ထပ်ရေးလိုက်ပါတယ်။

array 10 ခန်းပါတဲ့ data တစ်ခုရှိတယ်ဆိုပါစို့။ index 1 to 10 ကို binary နဲ့ အတူ range value တွေစမ်းတွက်ကြည့်ရအောင်။

Index 10 = 1010 , LSB = 2, ပြီးရင် 2 to the power of LSB - 1(fenwick မှာ base အတွက် 2 ကိုသုံးပါတယ်). ဆိုတော့ 2 to the power of LSB-1 = 2 ရပါတယ်။

Index 9 ဆိုရင် - 1001 , LSB = 1, 2 to the power of 1-1 = 2 power 0 = 1 ရပါတယ်။

အဲ့ဒီ range value တွေကိုသုံးပြီးတော့ prefix sum ကိုတွက်ပါတယ်။ index 7 ရဲ့ prefix sum ကိုလိုချင်တယ်ဆို

Prefix sum = Index[7] + Index[6] + Index[4] ရပါတယ်။ ဘာလို့လဲဆိုတော့
Index 7 ရဲ့ range value က 1 ပါ။ ဆိုတော့ အောက်တစ်ထစ်ဆင်းပါတယ်။ Index[6] ရပါတယ်၊ သူ့ရဲ့ range value က 2 ရပါတယ်။ အောက်နှစ်ထစ်ဆင်းပါတယ်၊ index[4] ရပါတယ်။ index[4] ရဲ့ range value 4 ရတဲ့အတွက် 0 အထိဆင်းသွားပြီး end ဖြစ်သွားပါတယ်။ အရင် article ကစာဖြစ်ပါတယ်။

အခုမှပြောချင်တာကိုရောက်ပါပြီ။ array တစ်ခုရဲ့ value ကို change ချင်ရင်ကျ prefix sum တွက်တာနဲ့ ပြောင်းပြန် အချိုးကျပါတယ်။ prefix sum မှာက range value ကိုတွက်ပြီး prefix sum အတွက် တစ်ဆင့်ခြင်းဆီ အောက်ဆင်းသွားပါတယ်။ point update လုပ်တဲ့နေရာမှာကျ range value အတိုင်း အပေါ်တတ်သွားရပါမယ်။ ဥပမာ တစ်ခုနဲ့ ကြည့်ကြည့်ရအောင်။

Array 16 ခန်းပါတဲ့ data structure တစ်ခုနဲ့ ပြောကြည့်ပါမယ်။ ကျနော်တို့ က index 9 မှာရှိတဲ့ value ကိုပြောင်းချင်ပါတယ်။ ဒါဆိုရင် range value တွေတွက်ပြီး တစ်ဆင့်ခြင်းဆီ အပေါ်တတ်သွားပါမယ်။ attachment image ပါကြည့်လို့ရပါတယ်

Index 9 ရဲ့ range value 1 ရပါတယ် = index 10
Index 10 ရဲ့ range value 2 ရပါတယ် = index 12
Index 12 ရဲ့ range value 4 ရပါတယ် = index 16
Index 16 မှာ end ဖြစ်သွားပါပြီ။ ဆိုတော့ index 9 မှာရှိတဲ့ value တစ်ခုကို ပြောင်းမယ်ဆို 9 to 16 အထိ လိုက်ပြောင်းနေစရာမလိုပါဘူး ။ index 9,10,12,16 ကိုပြောင်းလိုက်ရင်အဆင်ပြေသွားပါပြီ။

![Image of fenwick](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/fenwick(binary%20indexed%20tree)/fenwick-point%20update.png)
photos credit to udemy
