## Greedy algorithm

Greedy algorithm အကြောင်းအရင် မပြောခင်မှာ localized optimum solution နဲ့ globalized optimum solution ကို အရင်ရှင်းလိုက်ပါမယ်။ ကျနော် တို့ program တစ်ခု run တဲ့အခါ အဆင့်တစ်ဆင့်စီ တိုင်းမှာ အကောင်းဆုံး solution ကို ရွေးသွားတာကို localized optimum solution လို့ခေါ် ပြီးတော့ program တစ်ခုလုံးပြီးသွားလို့ နောက်ဆုံးမှာ အကောင်းဆုံး solution ရတာကို globalized solution လို့ခေါ်ပါတယ်။ Greedy algorithm ရဲ့ ရည်ရွယ်ချက်ကလည်း optimum solution ပေးဖို့အတွက်ပဲ၊ တစ်ဆင့်ခြင်းစီမှာ local optimum solution ကိုရှာပေးရင်းနဲ့ နောက်ဆုံးမှာ global optimum solution ကိုရနိုင်ဖို့အတွက်ပဲ။ ဒါပေမဲ့လည်း သူ့မှာ drawback တွေရှိနေတဲ့အတွက်ကြောင့် အမြဲတမ်း global optimum solution တော့မရနိုင်ဘူး။ ဘာလို့လဲဆိုတာကို အောက်မှာဆက်ကြည့်လိုက်ရအောင်။

Greedy က ဘယ်လိုအလုပ်လုပ်လဲဆိုတာ ကျနော် real world example နဲ့ ပြောပြပေးသွားပါမယ်။ ကျနော်တို့မှာ 2 ကျပ်တန် 3 ကျပ်တန် 10 ကျပ်တန် ဆိုပြီး ပိုက်ဆံလေးတွေရှိမယ်။ လိုချင်တာက 15 ကျပ်လိုချင်တယ်။ ဒါဆိုရင် greedy က ဘယ်လို run သွားမလဲဆိုတော့ ပထမဦးဆုံး local optimum ဖြစ်တဲ့ အကြီးဆုံး 10 ကိုယူတယ်၊ နောက်တစ်ခေါက်အတွက် 5ကျပ်ဖြည့်ဖို့ကျန်တဲ့အတွက်ကြောင့် 10 ထပ်ယူလို့မရတော့ဘူး၊ အဲ့အတွက် 3 ကိုယူတယ်။ 2 ကျပ်ထပ်ဖြည့်ဖို့ကျန်တယ်။ 3 ထပ်ယူလို့မရတော့ဘူး။ 2 ကို ထပ်ယူတယ်။ နောက်ဆုံးမှာ run သွားတဲ့ပုံစံက global optimum လည်း ဖြစ်တယ်။ တစ်ဆင့်ခြင်းဆီမှာလည်း local optimum solution တွေယူသွားနိုင်တယ်။ ဒါက satisfy ဖြစ်တဲ့ condition တစ်ခုပါ။

အကယ်လို့များ ကျနော်တို့ဆီမှာ ၁၀ ကျပ်တန် ရယ် ၇ ကျပ်တန်ရယ် ၁ကျပ်တန်ရယ်ပဲရှိတယ်ဆိုပါစို့၊ greedy ရဲ့ run နေကြပုံစံအတိုင်း ၁၀ကျပ်တန်ကို အရင်ယူမယ်။ ပြီးရင် ၅ကျပ်ထပ်ဖြည့်ဖို့ကျန်တယ်၊ ၇ထပ်လိုက်ရင်လည်းကြီးသွားမှာဖြစ်တဲ့အတွက်ကြောင့် ၁ကျပ်တန်ကို ၅ခါထပ်ဖြည့်ပါတယ်။ ၁၅ကျပ်တော့ ရသွားတယ်၊ ဒါပေမဲ့ သူ run သွားတဲ့ပုံစံက (၁၀+၁+၁+၁+၁+၁) ဖြစ်သွားတယ်။ process ကို ၆ ခေါက်လောက် run လိုက်ရသလိုဖြစ်သွားတယ်။ အမှန်ဆို (၇+၇+၁) ဆိုလည်း ၁၅ ရနိုင်ပါတယ်။ ဆိုတော့ greedy run သွားတဲ့ပုံစံက တစ်ဆင့်ခြင်းဆီမှာတော့ local optimum solution ကိုရှာသွားနိုင်ပေမဲ့ global အတွက်ကတော့ အဆင်မပြေဘူးဖြစ်သွားတယ်။

နောက်ထပ် real world example တွေလည်း ရှိသေးတယ်။ စာအရမ်းရှည်သွားမှာဆိုးလို့ ထပ်ထည့်မရေးတော့ပါဘူး။
Optimum solution ကိုရှာတဲ့ Huffman coding alogirthm တို့ ၊ minimum spanning Tree algorithm တွေဖြစ်တဲ့ prim တို့ Kruskal တို့မှာလဲ greedy algorithm ကိုသုံးကြပါတယ်။

Greedy algorithm ကို implement လုပ်ဖို့အတွက် program logic ကိုကျနော်ထပ်ရှင်းပြပေးပါမယ်။ ရေးရတာလွယ်တဲ့အတွက်ကြောင့် ကိုယ့်ဘာသာ စမ်းပြီး ရေးကြည့်ဖို့ suggest လုပ်ချင်လို့ပါ။

ဝင်လာတဲ့ input တွေကို order စီမယ်(optional ပါ)။ ပြီးရင် loop တစ်ခုလုပ်ပြီး destination value (ရချင်တဲ့ target value) နဲ့ compare လုပ်ပြီး input ထဲက ရနိုင်တဲ့ အကြီးဆုံး value တစ်ခုခြင်းဆီဆွဲထုတ်ပါ၊ ပြီးရင် destination value ကိုတော့ input ထဲက ဆွဲထုတ်ထားတဲ့ value နဲ့ နှုတ်ထားဖို့လိုပါတယ်။ conditional statement အနေနဲ့ကတော့ loop တိုင်းမှာ destination value or (နှုတ်ခံထားရတဲ့ လက်ကျန် destination value) ထက် input ဆွဲထုတ်မယ့် value ကကျော်သွားလို့မရပါဘူး။ နောက်ဆုံး destination value 0 ဖြစ်တဲ့အချိန် သို့မဟုတ် input ထဲမှာ destination value ထက် less than or equal ဖြစ်တဲ့ value မရှိတော့တဲ့အချိန်မှာ program ကိုအဆုံးသတ်လို့ရပါပြီ။

![Image of greedy](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/assets/greedy/Screen%20Shot%202019-08-10%20at%206.54.15%20PM.png)
