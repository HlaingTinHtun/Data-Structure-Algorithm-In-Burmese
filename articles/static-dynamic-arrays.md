## Static & Dynamic Arrays

Static တွေ dymanic တွေ မပြောခင် မှာ array အကြောင်းကို အရင်ပြောရအောင်။ array ကတော့ အားလုံးနဲ့ လည်း မစိမ်းလောက်ဘူး ၊ data value တွေကို collection လုပ်ထားတဲ့ sequence လို့လဲပြောလို့ရတယ်။ ဆိုလိုချင်တာ က data တွေ store လုပ်ဖို့ ပြန်ပြီး retrieve လုပ်ဖို့အတွက် အဆင်ပြေ အောင်ဖန်တီးထားတဲ့ data structure တစ်ခုလို့ဆိုနိုင်တယ်။ array တစ်ခုမှာ element ရှိတယ် ၊ index ရှိတယ်။ element ဆိုတာကတော့ array ထဲမှာ သိမ်းထားတဲ့ data value၊ အဲ့ array ထဲမှာ သိမ်းထားတဲ့ element တစ်ခုခြင်းရဲ့ memory ထဲမှာ numeric key တစ်ခု တွဲပေးထားတယ်၊ အဲ့ဒီ key ကို index လို့ခေါ်တယ်။ element value ကို index key သုံးပြီး လှမ်းဆွဲထုတ်လို့ရတယ်။

Array နဲ့ မသိမ်းဘဲ value တစ်ခု ခြင်းဆီ ကို variable တစ်ခုပေးပြီးလည်း သိမ်းလို့ရတယ်။ ဒါပေမဲ့ value တွေများလာတဲ့ အခါ တစ်ခုခြင်းဆီကို variable set လုပ်ပေးဖို့လည်း မလွယ်ဘူး၊ space လည်း ပိုယူတယ်။ တစ်ဖက်က coding ပိုင်းက ကြည့်မယ်ဆိုရင်လည်း data တွေ manage လုပ်ရတာ အဆင်မပြေတော့ဘူး။ array ထဲကို value တွေအများကြီး ထည့် set လုပ်လိုက်ခြင်းအားဖြင့် declare လုပ်ရတာ က လည်း တစ်ခါပဲ လုပ်ရမယ်။ ပြီးရင် data တွေ ပြန်ဆွဲထုတ် တဲ့ နေရာမှာလည်း index key နဲ့ အဆင်ပြေပြေဆွဲထုတ်လို့ရတယ်။

Static array ကတော့ fixed length ဖြစ်တယ်၊ ပြောချင်တာက array အခန်း ၄ ခု ဆို ၄ခုကိုပဲ memory မှာ preset လုပ်ထားလိုက်တယ်။ value တွေဆွဲထုတ်တဲ့နေရာမှာ ထုံးစံအတိုင်းပဲ index key သုံးပြီးဆွဲထုတ်တယ်။ static array မှာ element value တွေကို manage လုပ်လို့ မရဘူးတော့ မဟုတ်ဘူး၊ လုပ်လို့ရတယ်။ ဒါပေမဲ့သူအလုပ်လုပ်တဲ့ ပုံစံက၊ ဆိုပါတော့ element value ၄ ခုပါတဲ့ array တစ်ခုရှိတယ်၊ နောက်ထပ် value တစ်ခုထပ်ထည့်ချင်တယ်ဆိုရင် fixed length ဖြစ်နေတဲ့အတွက်ကြောင့် direct သွားထည့်လို့မရဘူး၊ memory ပေါ်ကို static array အသစ် တစ်ခုထပ်ကြေညာတယ်၊ ထပ်ထည့်ချင်တဲ့ value အတွက် array တစ်ခန်းအပိုနဲ့ပေါ့၊ ပြီးတော့ မှ အရင် array ကို copy paste လာလုပ်တယ်၊ နောက်ထပ် value တစ်ခု ကို တစ်ခါတည်း ထပ်ထည့်တယ်၊ အဲ့ဒီ process ပြီးမှ previous array ကို remove လုပ်တယ်။ ဆိုလိုချင်တာက static array ပေါ်မှာ element value တွေကို manage လုပ်လာပြီဆို memory consumption များလာတဲ့အတွက် မကောင်းဘူး။ အဲ့ဒီ issue ကိုဖြေရှင်းနိုင်ဖို့အတွက် dynamic array ကို သုံးလာကြတယ်။

Dynamic array ကလည်း စစချင်း တော့ static array လိုပဲ array တစ်ခု create လုပ်ရတာပဲ။ ဒါပေမဲ့ သူက assign လုပ်ထားတဲ့ element value တွေကို manage လုပ်နိုင်တယ်။ သူ manage လုပ်ပုံက array ၄ခန်းရှိတယ်။ assign လုပ်ထားတဲ့ element တွေကို ၄ ခုလုံးရှိတယ်။ အခန်းလွတ်မရှိဘူး။ နောက်တစ်ခုထပ်ထည့်ချင်တယ်ဆို နေရာလွတ်မရှိတော့တဲ့အတွက် လက်ရှိရှိပြီးသား array size ရဲ့ နှစ်ဆယူပြီး အရင် array ကို copy လုပ်တယ်။ element တွေထပ်ထည့်တယ်။ array resize လုပ်တယ်လို့လည်း ခေါ်တယ်။ array အခန်းပြည့် ပြီး နောက်ထပ် value assign လုပ်ချင်တဲ့ အချိန်ရယ်၊ assign value တွေ remove လုပ်ရင်း array အခန်းလွတ်တွေများပြီး space တွေယူနေတယ်လို့ ယူဆရတဲ့ အချိန်တွေရယ် resize လုပ်ပါတယ်။

Static array ကတော့
-	လိုအပ်တဲ့ memory amount ကိုပဲသုံးပြီး data manage လုပ်တဲ့ နေရာမှာကောင်းတယ်။
-	Dynamic array ထက်စာရင် element တွေ access လုပ်ရတာပိုမြန်တယ်။
-	Data တွေ manage operation (CRUD) လုပ်ရမယ်ဆို resource waste ဖြစ်တယ်။
-	Fixed size ဖြစ်ပြီးတော့ ၊ array စဆောက်တဲ့ အချိန်မှာ assign value တွေမပါသေးရင်တာင်မှ memory ယူထားရတယ်။

 dynamic array က တော့
-	data တွေ ခဏခဏ manage လုပ်တဲ့မယ်ဆို အသုံးဝင်တယ်။
-	size က flexible ဖြစ်တယ်။
-	array resize လုပ်တဲ့ အချိန်မှာ လိုအပ်တဲ့ resources တွေကို runtime မှာပဲ တစ်ခါတည်းသုံးသွားတဲ့အတွက် resources တွေ waste မဖြစ်တော့ဘူး။
-	static array နဲ့ယှဉ်ရင်တော့ element တွေ access လုပ်ရတာပိုနှေးတယ်။

photos credit to Udemy
![Images of arrays](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/static%20%26%20dynamic%20arrays/static%20array.png)

![Images of arrays](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/static%20%26%20dynamic%20arrays/dynamic%20array.png)
