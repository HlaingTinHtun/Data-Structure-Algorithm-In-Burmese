## Big 0 Notation

Big 0 Notation ဆိုတာက program/algorithm တစ်ခုရဲ့ performance run time ကိုဆိုလိုတာပါ၊ ဒီ algorithm တစ်ခု က ဘယ်လောက်မြန်လဲ၊ ဘယ်လောက်နှေးလဲစသည်ဖြင့်ပေါ့။ တစ်နည်းအားဖြင့် ပြောရမယ်ဆိုရင် algorithm တစ်ခုရဲ့ ခက်ခဲမှု (complexity) လို့လဲပြောလို့ရပါတယ်။ ဒီနေ့မှာ ကျနော် big 0 notation ကို နားလည်ရလွယ်အောင် real world example တွေနဲ့ နှိုင်းယှဉ်ပြီး ပြောပြပေးသွားပါမယ်။

စာကြည့်တိုက်ကြီးတစ်ခုရှိတယ်ဆိုပါစို့၊ စာအုပ်တွေလည်း တော်တော်စုံတယ်။ စာအုပ်ပေါင်း အမျိုးအစား အားလုံးပေါင်းလိုက်ရင် 1million လောက်တောင် ရှိတယ်ပဲထားလိုက်ရအောင်။ ဒါပေမဲ့ စာကြည့်တိုက်မှာ စာအုပ်လာငှားတဲ့ လူက ဘယ်စာအုပ်လေးလိုချင်ပါတယ် ဆိုပြီး နာမည်တပ်ပြောလိုက်ရင် အဲ့ စာအုပ်ကို လိုက်ရှာဖို့က အချိန်တော်တော်ယူနေရတယ်။ ဒါနဲ့ပဲ စာအုပ်တွေကို ရှာမယ့် searching algorithm တစ်ခုရေးဖို့စဉ်းစားကြတယ်၊ မြန်နိုင်သမျှ မြန်မြန်လိုအပ်တဲ့စာအုပ်ကို ရနိုင်ဖို့ပေ့ါ။ algorithm မှာ နှစ်ခုရှိတယ်၊ simple search နဲ့ binary search ဆိုပြီး (main topic က big 0 အကြောင်းဆိုတော့ binary search ကိုမသိလဲရပါတယ်)။
Algorithm နှစ်ခုလုံး က တိကျပြီး မြန်မြန်ဆန်ဆန် နဲ့ ထွက်လာဖို့လိုပါတယ်။ binary search ကတော့ ပိုမြန်တယ်။

Algorithm တွေရဲ့ run time ကို သိဖို့အတွက် စာအုပ် ၁၀၀ ပေါ်မှာ အခြေခံပြီးတွက်ကြည့်ရအောင်။ စာအုပ်တစ်အုပ် ကို 1millisecond (1000ms = 1 sec) ကြာတယ်လို့ define လုပ်လိုက်ရအောင်။ simple search က စာအုပ် ၁၀၀ လုံးအတွက် လိုက်စစ်စရာလိုတဲ့ အတွက် simple search နဲ့ ရှာမယ်ဆို စာအုပ် ၁၀၀ အတွက် 100ms ကြာပါမယ်။ binary search နဲ့ဆို စာအုပ် ၁၀၀ မှာ လိုချင်တဲ့ result ထွက်လာဖို့ အတွက် စာအုပ် ၇ အုပ်စာလောက်ပဲ စစ်ရပါတယ်။ binary search ရဲ့ algorithm အရ (log2 100 ဆို 7 လောက်ရပါတယ်)။ ဆိုတဲ့အတွက် ကြောင့် binary search နဲ့ run မယ်ဆို 7ms ပဲကြာပါမယ်။ တစ်ကယ်တော့ ၁၀၀ ပဲ run ရမှာ မဟုတ်ဘူး။ 1million record ကို run ရမှာပါ။

Record 100 base အရ ထွက်လာတဲ့ run time (milliseconds) ပေါ်မူတည်ပြီး binary search က simple search ထက်စာရင် 14 ဆလောက်မြန်တယ်လို့မှတ်ယူထားပါတယ်။ Binary search နဲ့ record တစ်သန်းကို run လိုက်တဲ့ အချိန်မှာ 20sec လောက်ကြာပါတယ်။ simple search နဲ့ဆို 14 ဆ ဆိုတော့ 280sec လောက်ကြာမယ်လို့ခန့်မှန်းပါတယ်။

အဲ့မှာ စမှား တာပါ  တစ်ကယ်တော့ simple search နဲ့ဆို 16 mins ကျော်ကြာသွားမှာပါ။ ဘာလို့လဲဆိုတော့ algorithm နှစ်ခု က rate ခြင်းမတူကြပါဘူး။ ဆိုလိုတာက input size များလာတာနဲ့အမျှ run time လဲပိုပြီးကွာသွားမှာပါ။ 14 ဆပိုမြန်တယ်ဆိုပြီး ပုံသေတွက်လို့မရပါဘူး။ ဆိုလိုချင်တာက ဒါက record 1million ပဲရှိသေးတယ်။ 1 billion ဆို binary search နဲ့ဆို 30sec လောက်ပဲကြာပြီး simple search နဲ့ဆို 11 ရက်လောက်ကြာမှာပါ။ rate ကလည်း 33million လောက်ပိုမြန်မှာပါ။

Big 0 ရဲ့ အဓိက ဆိုလိုရင်းက လည်း အဲ့ဒါပါပဲ algorithm တစ်ခုရဲ့ run time ကိုပြတယ်။ ဒါပေမဲ့ အချိန် တွေ seconds တွေနဲ့ မဟုတ်ပဲနဲ့ operation နဲ့ပြတယ်။ simple search algorithm နဲ့ဆို အုပ်ရေ ၁၀၀ မှာ အခေါက် ၁၀၀ run ရပေမဲ့ binary search algorithm နဲ့ ဆို ၇ ခေါက် (7 operations) ပဲ run ရမယ်။ input size ကြီးလာတာနဲ့ အမျှ သူတို့ကြားထဲက ကွာခြားချက်ကလဲ ကြီးလာမှာပဲ။ ဘယ်လောက် ကွာခြားသွားလဲဆိုတာကို big 0 notation က formula တွေနဲ့ define လုပ်ပေးတယ်။

သတိချပ်စရာရှိတာက big 0 calculation တွက်ပြီးဆို wrost case တွေအထိစဉ်းစားပြီး တွက်ရတယ်။ ဥပမာ record 100 မှာရှာမယ်ဆို ကိုယ်ရှာတဲ့ key ကို ပထမဆုံးတင်တွေ့တယ်ဆိုပါစို့။ algorithm က entry တိုင်းကို သွားဖတ်စရာမလိုတော့တဲ့အတွက် ကိုယ့် algorithm က n time လား 1 time လားဆိုတာ သတိပြန်ချပ်သင့်ပါတယ်။ entry အကုန်လုံးကို run မှ big 0 of n ရလာမှာပါ။ ဒါကြောင့် လည်း အဆိုးဆုံး worst case အထိစဉ်းစားခိုင်းတာပါ။

Big 0 ရဲ့ run times တွေ အမျိုးမျိုးရှိတယ်။ အသုံးများတာတွေကို အောက်မှာ ရေးပေးလိုက်တယ်။ fastest to slowest order နဲ့။

O(log n), log time (eg binary search)
O(n), linear time (eg simple search)
O(n * log n), (fast sorting algorithm)
O(n2), (slow sorting algorithm)
O(n!) (pretty slow algorithm)

Run time တွေကို စမ်းကြည့်ချင်တယ်ဆို ကိုယ့်ဘာသာ calculator နဲ့တွက်ပြီး စမ်းကြည့်လို့ရတယ်။ ဥပမာ 1billion records မှာ log time နဲ့ဆိုဘယ်လောက်ကြာမလဲ၊ linear နဲ့ဆိုဘယ်လောက်လဲ စသည်ဖြင့်ပေါ့။

![Image of big0](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/big0.png)
