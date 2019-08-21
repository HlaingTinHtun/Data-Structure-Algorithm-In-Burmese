## Stack Algorithm

Stack ဆိုတာက သူ့ကို ပေးထားတဲ့နာမည် အတိုင်းပဲ အစုလိုက်ထပ်ထပ်ဆင့်ထားတဲ့ ပုံစံမျိုးကို ဆိုလိုတဲ့ structure တစ်ခုပဲ၊ LIFO (last in first out) or FILO(first in last out) ဆိုတဲ့ order အတိုင်းအလုပ်လုပ်တယ်။ ပြောရမယ်ဆိုရင် စာအုပ်တွေထပ်ပြီးတင်ထားတယ်၊ နောက်ဆုံးတင်တဲ့ တစ်အုပ်ကိုပဲ  အရင်ပြန်ယူတယ် (last in first out) ၊ ပထမဆုံး ထားလိုက်တဲ့စာအုပ်ကို နောက်ဆုံးမှ ထုတ်လို့ရတယ် (first in last out) ၊ အဲ့ဒီ သဘောတရားပါပဲ။

stack ကို array နဲ့ပဲဖြစ်ဖြစ် linked list နဲ့ပဲဖြစ်ဖြစ် ဆောက်လို့ရတယ်၊ fixed sized ရော dynamic size ရော ကြိုက်သလိုဆောက်လို့ရတယ်၊ ဆောက်တဲ့ program ပေါ်ပဲမူတည်တယ်။ stack မှာ operations တွေအမျိုးမျိုးရှိပေမဲ့ အဓိက သုံးတာက တော့ push နဲ့ pop ပဲ။ push ဆိုရင် stack ထဲကို data လာထည့်မယ်။ pop ဆို ထုတ်မယ်၊ push လုပ်လုပ် pop လုပ်လုပ် အပေါ်ဆုံးက data value ကိုပဲ လုပ်လို့ရမယ်။ တစ်ခြား သုံးတဲ့ function တွေလည်း ရှိတယ်၊ ဥပမာ ထိပ်ဆုံး ကို element ကို access လုပ်ဖို့ဆို peek ဆိုတာကိုသုံးတာတို့၊ stack က ပြည့် နေပြီးလား empty ဖြစ်နေလားစတာတွေကို စစ်တဲ့ function တွေလဲရှိတယ်။ ဒီနေရာမှာတော့ ကျနော် push နဲ့ pop ကိုပဲ အဓိက ထားပြီး ပြောလိုက်မယ်၊ ဒါဆိုရင် ကျန်တဲ့ဟာတွေလဲ ခြုံငုံပြီးတစ်ခါတည်း ပြောပြီးသားဖြစ်သွားပါလိမ့်မယ်။

stack တစ်ခုထဲကို data တစ်ခု push (ထည့်) လုပ်တော့မယ်ဆိုရင်
-	အရင်ဆုံး stack က ပြည့်နေလားအရင်ကြည့်တယ်
-	Stack က ပြည့်နေတယ်ဆို သက်ဆိုင်တဲ့ msg ပြန်ပြီးတော့ exit လုပ်တယ် (dynamic size အတွက်ဆိုရင်တော့ သူ့ဘာသာ resizing လုပ်သွားတယ်)
-	Stack က ထည့်လို့ရသေးတယ်ဆိုရင် top pointer ကို နောက်ထပ်ဝင်လာမယ့်နေရာအတွက်ဦးထားပေးလိုက်တယ် (top pointer ဆိုတာလက်ရှိ stack ထဲမှာ အပေါ်ဆုံးမှာရှိနေတဲ့ data ကိုထောက်ထားတဲ့ pointer, push operation လုပ်တော့မယ်ဆို top pointer ကို +1 ပုံစံယူပြီး နောက်ဝင်လာမယ့် နေရာအတွက် empty space ကိုထောက်ပေးထားတယ်။)
-	နောက်တစ်ဆင့်အနေနဲ့ top pointer ထောက်ထားတဲ့ နေရာကို data ဝင်လာတယ်
-	Operation success ဖြစ်တဲ့ အကြောင်း return ပြန်တယ်

Stack Pushing
![Images of stack](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/stacks/stack%20pushing.png)

Stack Popping
![Images of stack](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/stacks/stack%20poping.png)

Stack ထဲကနေ pop operation (stack ထဲကနေ data ထုတ်တော့မယ်ဆိုရင်)
-	Stack က empty ဖြစ်နေလားအရင်ကြည့်တယ်
-	Empty ဖြစ်နေတယ်ဆို သက်ဆိုင်တဲ့ msg ပြန်ပြီးတော့ exit လုပ်တယ်
-	Empty မဖြစ်ဘူးဆိုရင် လက်ရှိ top point ထောက်ထားတဲ့ data ကို access လုပ်တယ်။
-	Top pointer ကို အောက်တစ်ထစ်ဆင်းလိုက်ပြီး ခုနက access လုပ်ထားတဲ့ data ကို stack ထဲကနေထုတ်လိုက်တယ်
-	Operation success ဖြစ်တဲ့ အကြောင်း return ပြန်တယ်

ဒီ algorithm ကို ဘယ်လို နေရာတွေမှာ အသုံးချလဲဆိုတော့ LIFO သဘောတရားရှိနိုင်တဲ့ နေရာမှန်သမျှမှာ apply လုပ်လို့ရတယ်။ ဥပမာ ပြောရမယ်ဆိုရင် IDE တွေမှာ undo လုပ်တဲ့ process တို့ ၊ browser တွေမှာ back သွားတဲ့ process တို့ ၊ expressions တွေ convert လုပ်တဲ့နေရာ စတဲ့ နေရာတွေမှာသုံးလို့ရတယ်၊ ဘယ်လိုနေရာတွေမှာ ထပ်သုံးထားလဲသိချင်ရင် အောက်က link မှာ ဝင်ကြည့်လို့ရပါတယ်။
http://jcsites.juniata.edu/faculty/kruse/cs240/stackapps.htm

photos credit to Udemy
