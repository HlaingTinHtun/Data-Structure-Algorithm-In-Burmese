## Linked lists Algorithm

Linked list ဆိုတာ ကကျ data node တွေကို sequence အတိုင်း link လုပ်ထားတာ။ မြင်အောင် ပြောရမယ်ဆိုရင် list စစချင်းမှာ head ရှိမယ်၊ အဆုံးမှာ tail ရှိမယ်၊ ကြားထဲမှာ data node တွေနဲ့ သူတို့ကို ချိတ်ဆက်ထားတဲ့ link တွေရှိမယ်။ attach တွဲထားတဲ့ ပုံတွေ ကြည့်လိုက်ရင်တော့ ပိုရှင်းသွားလိမ့်မယ်။

Linked lists တွေကိုပြန်ခွဲကြည့်မယ်ဆို
-	Singly linked list
-	Doubly linked list
-	Circular linked list
ဆိုပြီးရှိတယ်။

Singly linked list ကကျ တော့ data node တွေကြားမှာ ချိတ်ဆက်ထားတဲ့ link တွေက node တစ်ခုခြင်းဆီရဲ့ forward ကိုပဲ ချိတ်လို့ရတယ်၊ backward (previous node) ကို link ပြန်လုပ်ထားတာမရှိဘူး။

Doubly linked list ကတော့ node တွေအကုန်လုံးကို forward ရော backward ရော link လုပ်ထားတယ်၊ ဆိုတော့ ပိုပြီးတော့ အသုံးဝင် တယ်လို့ဆိုရမယ်။ previous data ကို ပါ လှမ်း access လုပ်လို့ရတာကိုး။

Circular linked list က သူ့ နာမည်အတိုင်းပဲ circular ပြန်လုပ်ပြီး link တယ်၊ singly linked list မှာဆို tail ကနေ head ဆီကို လှမ်းပြီး link လုပ်ထားတယ်။ doubly linked မှာက ကျ tail ကနေ head ကိုလည်း link တယ်၊ doubly ရဲ့ ထုံးစံအတိုင်း head ကနေလည်း tail ကို ပြန်ပြီး link လုပ်တယ်။

Singly Linked List
![Images of linked list](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/linked%20lists/singly%20linked%20list.png)

Doubly Linked List
![Images of linked list](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/linked%20lists/doubly%20linked%20list.png)


Operation လုပ်ပုံလုပ်နည်း ကလည်း နည်းနည်းဆီကွာတယ်။ insert လုပ်တဲ့ပုံကို အရင်ပြောကြည့်ရမယ်ဆိုရင်

Singly linked list မှာ 3rd node မှာ node အသစ်တစ်ခုထည့်မယ်ဆိုပါစို့။ node တစ်ခုခြင်းဆီကို traverse လုပ်တယ်၊ ဒုတိယမြောက်မှာ ရပ်လိုက်တယ်၊ထည့်မယ့် value node ကို create လုပ်တယ်၊ တတိယမြောက် node ကို pointer ထောက်တယ်၊ traverser ရပ်ထားတဲ့ ဒုတိယမြောက် element ကို သူနဲ့ ချိတ်တယ်၊ ပြီးတာနဲ့ insert လုပ်လိုက်တယ်။

Doubly linked list မှာလည်း insert operation မှာ singly နဲ့အတူတူပဲ ကွာသွားတာ က singly က link ချိတ်တဲ့ နေရာမှာ forward link ပဲချိတ်ရပေမဲ့ doubly မှာ previous ရော forward အတွက်ပါချိတ်ပေးရတယ်။

Singly Linked List Inserting Operation
![Images of linked list](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/linked%20lists/singly%20linked%20list%20inserting%20operation.png)

Doubly Linked List Inserting Operation
![Images of linked list](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/linked%20lists/doubly%20linked%20list%20inserting%20operation.png)

Remove operation မှာတော့ ပိုပြီးကွာတယ်။ singly မှာ remove operation လုပ်တော့မယ်ဆို traverser နှစ်ခုနဲ့သွားရတယ်။ trav1 & trav2 ပေါ့၊ remove လုပ်ရမယ့် node ကို trav2 ကတွေ့သွားပြီးဆို တွေ့သွားတဲ့ node ကို memory ထဲမှာ temporary allocate လုပ်လိုက်တယ်။ allowcate လုပ်ပြီးတာနဲ့ trav2 က နောက် node တစ်ခုကို ထပ်သွားတယ်၊ ပြီးတော့မှ temp allocate ထားတယ့် node ကို ဖြတ်ချပြီး deallocate ပြန်လုပ်လိုက်တယ်။ trav1 & 2 ကို လည်း linked ပြန်လုပ်လိုက်တယ်။

Doubly မှာတော့ traverser နှစ်ခုမလိုဘူး။ တစ်ခုနဲ့ ဆိုရတယ်။ ဘာလို့လဲဆိုတော့ သူ့မှာက previous ရော forward ရောချိတ်လို့ရတယ်။ singly မှာက မရှိတဲ့အတွက် reference key လိုလို့ traverser နှစ်ခုနဲ့ သွားရတာ။ ဖြတ်ရမယ့် node ရောက်ပြီဆို သူ့ရဲ့ ရှေ့ node နဲ့ နောက် node ကို forward & backward link ချိတ်ပေးပြီး ဖြတ်လိုက်တယ်။

Singly Linked List Removing Operation
![Images of linked list](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/linked%20lists/singly%20linked%20removing%20operation.png)

Doubly Linked List Removing Operation
![Images of linked list](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/linked%20lists/doubly%20linked%20removing%20operation.png)

နှစ်ခုလုံးမှာတော့ draw back တွေရှိတယ်။ singly က memory use တာနည်းပေမဲ့ previous element ကိုပြန်သွားလို့မရဘူး။ doubly က previous node ပြန်သွားလို့ရတယ်၊ memory လည်း နှစ်ဆပိုကုန်တယ်။

ဘယ်လိုနေရာတွေမှာ သုံးလည်း ဆိုတော့ sequentially linked လုပ်ထားတဲ့ process တော်တော်များများမှာ သုံးတယ်။ ဥပမာ file system တစ်ချို့ မှာ file locations တွေကို linked လုပ်ပြီး သိမ်းထားတာတို့ ၊ browser history မှာ သိမ်းထားတဲ့ page တွေမှာ back ပြန်သွားလို့ရတာမျိုးတို့ ၊ memory block တွေကို linked လုပ်ထားတဲ့ low level memory management system တို့မှာတို့ အစရှိတဲ့ နေရာတော်တော်များများမှာ သုံးထားတယ်။ linked list ရဲ့ သဘောတရားကို နားလည်သွားပြီဆိုရင် ဘယ်လို technology မှာ linked list algorithm သုံးထားလည်းဆိုတာ ခန့်မှန်းလို့ရသွားနိုင်မယ့် အပြင် ကိုယ်ကိုတိုင်လည်း develop လုပ်သွားနိုင်မှာပါ။

photos credit to Udemy
