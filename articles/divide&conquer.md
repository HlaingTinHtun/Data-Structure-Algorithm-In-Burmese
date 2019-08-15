## Divide and Conquer Algorithm

Greedy လို algorithmic paradigm တစ်ခုပဲ။ သူက ဘာလုပ်လဲဆိုတော့ problem တစ်ခုရလာပြီဆိုရင် အဲ့ problem ကို sub problem တွေအဖြစ်ခွဲချလိုက်တယ်။ အဲ့ဒီ sub problem တွေကိုလည်း နောက်ထပ် sub problem တွေအဖြစ်ခွဲချလိုက်လို့ရသေးတယ်။ လုံး၀ နောက်ထပ် ထပ်ခွဲထုတ်လို့ မရနိုင်တော့တဲ့ အခြေအနေတစ်ခု အထိ ခွဲချလိုက်တာ တစ်နည်းအားဖြင့် ဆိုရမယ်ဆို problem ကို တစ်ဆင့်ခြင်းဆီ break down လုပ်လိုက်တယ်ပေါ့။ နောက်တစ်ဆင့် အနေနဲ့ ဘာလုပ်လဲဆိုတော့ အဲ့ဒီ ခွဲထားတဲ့ Sub problem လေးတွေတစ်ခုခြင်းဆီကို solution ရှာတယ်။ ရှာပြီး တော့မှ ခုနက ဖြိုခွဲထားတဲ့ အတိုင်း အဆင့်ဆင့် ပြန်ပေါင်းလိုက်တယ်။ ခွဲထားတုန်းကလည်း recursive approach အနေနဲ့ sub problem တွေ ခွဲထားတယ်၊ ပြန်ပေါင်းတော့လည်း recursively ပဲ အဆင့်ဆင့်ပြန်ပေါင်းတယ်။

အပေါ်မှာပြောထားခဲ့သလိုပဲ divide & conquer က step ၃ ခုနဲ့အလုပ်လုပ်တယ်။

### Divide
Problem တွေကို breaking down အရင်လုပ်တယ်။ recursive approach ကိုသုံးပြီးတော့ problem တစ်ခုကို sub problem တွေအဖြစ်ခွဲချတယ်၊ နောက်ထပ် sub တွေခွဲချလို့မရတော့တဲ့ အထိပေ့ါ၊

### Conquer
Sub problem တွေကို solving လုပ်တဲ့အဆင့်ပေါ့၊ ခွဲချထားတဲ့ problem တစ်ခုခြင်းဆီကို solve လုပ်လိုက်ပါတယ်။

### Combine
Conquer stage မှာ solved လုပ်ထားတဲ့ sub solution တွေကို recursively ပြန် merge လုပ်ပြီးတော့ နဂို ခွဲချလိုက်တဲ့ မူရင်း problem အတွက် solution ထုတ်ပါတယ်။

ဒီလောက်ဆိုရင်တော့ divide & conquer အကြောင်းကို အကြမ်းဖျင်းအားဖြင့် နားလည်လောက်ပြီ ထင်ပါတယ်။

ဘယ်လိုနေရာတွေမှာ apply လုပ်လဲဆိုတော့ problem ကို divide လုပ်တာတို့ ၊ recursively run တာတို့ လုပ်တဲ့ sorting algorithms တွေဖြစ်တဲ့ quick sort တို့ ၊ merge sort တို့ မှာသုံးတယ်၊ Binary search algorithm မှာလဲ apply လုပ်ထားတယ်။ sorting algorithm တွေနဲ့ binary search အကြောင်းလဲ နောက် articles တွေမှာ algorithm code sample တွေနဲ့အတူ ရေးပေးသွားပါမယ်။

photo credits to khanacademy

![Image of dividenconquer](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/assets/dividenconquer/dividenconquer.png)
