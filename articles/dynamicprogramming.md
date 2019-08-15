## Dynamic Programming

Dynamic programming approach ကလည်း အရှေ့မှာ ရေးထားခဲ့တဲ့ greedy နဲ့ divide & conquer ပုံစံတွေနဲ့ဆင်ပါတယ်။ divide & conquer လိုမျိုး sub problem တွေခွဲချပြီး recursion လုပ်ပြီးပြန်ပေါင်းတယ်။ greedy လိုမျိုး optimum solution ရဖို့အတွက်လည်း လုပ်ထားတယ်။ ဘယ်လို လုပ်ထားလဲဆိုတာ တစ်ချက်လောက်ကြည့်လိုက်ရအောင်။ ဒီ article မဖတ်ခင် divide & conquer နဲ့ greedy ကို အရင်ဖတ်ကြည့်ဖို့ အကြံပေးချင်ပါတယ်။ အောက်က link တွေမှာ ဝင်ဖတ်လို့ရပါတယ်။

Divide & conquer
https://www.facebook.com/permalink.php?story_fbid=862512540771458&id=100010381592688
Greedy
https://www.facebook.com/permalink.php?story_fbid=861903050832407&id=100010381592688

Dynamic programming မှာ problem တစ်ခု ရှိလာတဲ့အခါမှာ divide & conquer approach ပုံစံမျိုးပဲ sub problem တွေအဖြစ်ခွဲချလိုက်တယ်။ ခွဲပြီးတာနဲ့ အဲ့ဒီ sub problem တွေကို solution လုပ်တယ်၊ sub problem တွေခွဲတဲ့ အချိန်က နေပြီးတော့ solution formula ထွက်တဲ့အထိ dynamic programming approach က memorized လုပ်ထားတယ်။ နောင်တစ်ချိန် ဒီလို မျိုး sub problem တွေ့ပြီဆို ပြန်ပြီးတော့ သုံးလို့ရအောင်လို့ပါ။

ဥပမာ ကျနော်တို့ sub problem တစ်ခုမှာပေ့ါ၊ x ကိုရှာတဲ့ solution ကိုရထားတယ်။ နောက်တစ်ခါ x ရဲ့တန်ဖိုးကိုထပ်ရှာရမယ့် sub problem မျိုး ရှိလာခဲ့ရင် ကျနော်တို့မှာ x ရဲ့ တန်ဖိုးကို ရှာနိုင်တဲ့ formula ကို memorized လုပ်ထားတဲ့အတွက် နောက်တစ်ခေါက်ထပ်ရှင်းစရာ မလိုတော့ဘဲ optimum ဖြစ်တဲ့ solution ကိုရတယ်။ ဥပမာ နောက်တစ်ခု အနေနဲ့ ထပ်ရှင်းအောင် ပြောရမယ်ဆိုရင် 3+4+5 ဆို 12 ရမယ်။ အဲ့ဒါကို 1 ထပ်ပေါင်းမယ်ဆိုပါစို့ ၊ 13 လို့တန်းပြောနိုင်တယ်။ ဘာလို့လဲဆိုတော့ ကျနော်တို့ က 1 ကိုပဲထပ်ဆင့် ပေါင်းလိုက်တာ 3+4+5 ပေါင်းတာကို ထပ်မတွက်တော့ဘဲ memorized လုပ်ထားတဲ့ 12 နဲ့ 1 ကိုပဲပေါင်းလိုက်တဲ့အတွက် solution က မြန်မြန်ဆန်ဆန် ထွက်လာတာပါ။

ဆိုတော့ dynamic programming ကိုဘယ်နေရာတွေမှာ apply လုပ်လို့ရလဲဆိုတော့ problem တွေကို sub structure အဖြစ်ခွဲချလို့ရမယ်၊ ပြီးတော့ sub problem တွေက overlap ဖြစ်လာမယ်ဆိုရင် memorized လုပ်ထားတဲ့ solution ကိုအစားထိုးပြီးတော့ optimize ဖြစ်အောင်လုပ်တယ်။

Divide & conquer မှာတုန်းကတော့ sub problem တွေကို ပြန်ပေါင်းပြီးတော့ over all solution တစ်ခုထုတ်တယ်။ dynamic programming ကတော့ sub problem တစ်ခုခြင်းဆီရဲ့ formula ကို memorized လုပ်ထားပြီးတော့ နောက်တစ်ဆင့် နောက်တစ်ဆင့် problem တွေအတွက် optimized လုပ်နိုင်ဖို့ကို ပိုပြီး အာရုံစိုက်ထားတယ်။ CPU ရဲ့ computing power ကိုလည်း သက်သာစေတာပေါ့။

Greedy မှာတုန်းကတော့ local optimization အတွက် အဆင်ပြေပြီးတော့ dynamic programming ကကျ local အတွက်တင် မဟုတ်ဘဲ overall problem တစ်ခုလုံးအတွက် အဆင်ပြေအောင် address လုပ်ထားတယ်။

ဒီလောက်ဆိုရင်တော့ ဖြင့် dynamic programming အကြောင်းကို theory အရ အကြမ်းဖျင်း နားလည်သွားလောက်ပြီထင်ပါတယ်။


![Image of dynammicprogramming](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/assets/dynamicprogramming/dynamicprogramming.png)
