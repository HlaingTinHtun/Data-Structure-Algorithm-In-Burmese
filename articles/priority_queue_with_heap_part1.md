## Priority Queue With Heap (Part 1)

Priority Queue ကို heap နဲ့ ဆောက်ရတဲ့ အကြောင်းအရင်းက လောလောဆယ်မှာ time complexity အတွက် အသင့်တော်ဆုံးဖြစ်နေသေးလို့ပါ။ တစ်ခြား ဆောက်လို့ရတဲ့ algorithm တွေလဲရှိတယ်၊ ဥပမာ unsorted list တို့ဘာတို့နဲ့ ဆောက်လို့ရတယ် ဒါပေမဲ့ time complexity အတွက်အဆင်မပြေသေးဘူး။ ဒါကြောင့်မို့ heap ကိုပဲ သုံးဖြစ်နေကြတာပါ။

ဒီ article ကိုမဖတ်ခင်မှာ Priority Queue ရဲ့ article ကိုအရင်သွားဖတ်ဖို့လိုအပ်ပါတယ်(must)။ Heap အကြောင်းကို Introduction လုပ်ထားတာလဲပါပါတယ်၊ ဒီ article ရှည်သွားမှာဆိုးလို့ထပ် မထည့်တော့ပါဘူး။ အောက်က link မှာသွားဖတ်နိုင်ပါတယ်။
https://www.facebook.com/permalink.php?story_fbid=856781714677874&id=100010381592688

ဒီ article မှာ ပုံတွေလည်း တစ်ဆင့်ခြင်းဆီအတွက် attach တွဲပေးထားတယ်။ စာချည်းပဲ ဖတ်ရင် နားလည်ရခက်မှာဆိုးတဲ့ အတွက် ပုံတွေနဲ့ တွဲကြည့်ဖို့ suggest လုပ်ပါတယ်။

Priority Queue ဆောက်ဖို့ အတွက် Heap ထဲမှာလည်း
-	Binary heap
-	Fibonacci heap
-	Binomial heap
-	Pairing heap အစရှိသည်ဖြင့် အမျိုးအစား အမျိုးမျိုး ရှိတယ်။ လောလောဆယ်တော့ Binary heap ကိုသုံးပြီးတော့ ရှင်းပြပေးသွားပါမယ်။

Heap တိုင်းကတော့ tree structure ပဲ သူ့ရဲ့ heap rules တွေကိုလည်းလိုက်နာတယ်။ Binary heap ဆိုတော့ သူ့နာမည်အတိုင်းပဲ binary tree structure ဖြစ်တယ်။ Node တစ်ခုခြင်းဆီတိုင်းမှာလည်း child element နှစ်ခုစီနဲ့ tree structure ဆောက်ထားတယ်။

### What Is Binary Heap
![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%201.%20what%20is%20binary%20heap.png)

ကျနော် အောက်မှာပုံတွေလည်း attach တွဲပေးထားတယ်၊ တစ်ချို့ စာတွေက ကျပုံတွေနဲ့ တွဲပြီးကြည့်မှ ပိုပြီးထင်သာမြင်သာရှိမှာမို့လို့ပါ။ အခု အရင်ဆုံးအနေနဲ့ binary heap ရဲ့ data represent လုပ်ပုံကို ကြည့်ရမယ်ဆိုရင် သူ့ရဲ့ data node တွေကို array index တွေအတိုင်းမှတ်ထားလို့လည်း ရတယ်၊ ဥပမာ data node value 6 က array index key number 3 မှာရှိတယ် ၊ အဲ့လိုမျိုး present လုပ်လို့လဲရပါတယ်

### Binary Heap Representation
![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%202.%20binary%20heap%20representation.png)

နောက်တစ်ခုအနေနဲ့ parent node တစ်ခုရဲ့ အောက် က child element တွေရဲ့ array index key ကိုလည်း တွက်ထုတ်လို့ရတယ်၊ parent node ရဲ့ array key က 2 လို့ဆိုပါစို့ ၊ child element တွေ ဆွဲထုတ်မယ်ဆို binary tree ဖြစ်တဲ့အတွက် left &  right child element ဆိုပြီးရှိမယ်။ left child အတွက်ဆို (2(current_node_key) + 1) = 5 ရမယ်၊ right child အတွက်ဆို (2(current_node_key)+2)=6 ရပါမယ်။

### Binary Heap Representation
![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%203.%20binary%20heap%20representation.png)

Binary heap မှာ data element insert လုပ်တော့မယ်ဆိုရင် သူ့ရဲ့ tree structure အရ အမြဲတမ်း left to right သွားပါတယ်။ insert လုပ်ပြီဆို အောက်ခြေ row ကနေ စပါတယ်။ အောက်ဆုံးအတန်းကနေ left to right ပေါ့။ တစ်ခုရှိတာက ထည့်ပြီးတာနဲ့ ပြီးမသွားဘူး၊ သူ့ရဲ့ heap invariant (အရင် article မှာရေးထားပါတယ်) အတွက်စစ်ရသေးတယ်။ အဆင်မပြေဘူးဆိုရင် တစ်ဆင့်ခြင်းဆီ heap invariant satisfy ဖြစ်တဲ့အထိ parent node နဲ့ replace လုပ်လုပ်သွားတယ်။ အဲ့လို တစ်ဆင့်ခြင်းဆီ တတ်တတ်သွားပြီး heap invariant satify လုပ်တာကို bubbling up လုပ်တယ်လို့လဲ ခေါ်ပါတယ်။

### Adding Elements To Binary Heap
![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%204.1.%20adding%20elements%20to%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%204.2.%20adding%20elements%20to%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%204.3.%20adding%20elements%20to%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%204.4.%20adding%20elements%20to%20binary%20heap.png)

Remove လုပ်တာကတော့ နှစ်မျိုးရှိတယ်။ ရိုးရိုး poll function နဲ့ ဖျက်ချင်တဲ့ value ကို ထည့်ပေးပြီး ဖျက်ရတဲ့ remove
Function ဆိုပြီး ရှိတယ်။ Poll function ကိုအရင်ပြောကြည့်ရအောင်။ ထည့်တုန်းက left to right order နဲ့သွားခဲ့ တာဆိုတော့ ဖျက်မယ်ဆိုရင် right to left ဖြစ်သွားမယ်။ မဖျက်ခင်မှာ ဖျက်ရမယ့် element နဲ့ root node နဲ့ ကို အရင် swap လုပ်တယ်။ ပြီးတော့မှ ဖျက်ချလိုက်တယ်။ root node နေရာမှာ ရောက်သွားတဲ့ element ကို တစ်ဆင့်ခြင်းဆီ heap invariant ဖြစ်အောင် child node တွေနဲ့ replace ပြန်လုပ်တယ်။ bubbling down လုပ်တယ်လို့လဲခေါ်တယ်။ invariant ဖြစ်ပြီးသားဆိုရင်တော့ လုပ်စရာမလိုဘူး။ bubbling down လုပ်ရင်တစ်ခု သတိထားရမှာက parent element တစ်ခုမှာ child ၂ ခုစီ ရှိတယ်။ child ၂ ခုမှာ ငယ်တဲ့ ဘက်ကိုပဲ ရွေးပြီး replace လုပ်ပါတယ်။ အကယ်လို့ နှစ်ခုလံးုက တန်ဖိုးတူနေတယ်ဆို ဘယ်ဘက်ကို ရွေးပါတယ်။

### Removing Elements From Binary Heap(Polling)
![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%205.1%20polling%20elements%20from%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%205.2%20polling%20elements%20from%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%205.3%20polling%20elements%20from%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%205.4%20polling%20elements%20from%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%205.5%20polling%20elements%20from%20binary%20heap.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%205.6%20polling%20elements%20from%20binary%20heap.png)

Remove(value param) ကကျတော့ သူ့မှာ ဖျက်ချင်တဲ့ value parameter ပါလာပြီဖြစ်တဲ့ အတွက် အဲ့ဒီ value ကို tree မှာတစ်ဆင့်ခြင်းဆီ လိုက်ရှာရပါတယ်၊ အပေါ်ဆုံးအတန်းကနေပြီးတော့ အောက်အထိ တစ်ဆင့်ခြင်းဆီ left to right ရှာပါတယ်။ အဲ့လို ရှာရတဲ့အတွက် Linear time ကြာတယ်လို့ဆိုရမှာပေါ့။ တွေ့ပြီဆိုရင် အဲ့ဒီ element နဲ့ လက်ရှိနောက်ဆုံး မှာရှိနေတဲ့ element ကို swap လုပ်တယ်။ swap လုပ်ပြီး နောက်ဆုံး element ကိုပဲဖြတ်တယ်။ ပြီးရင် heap invariant ဖြစ်အောင် ပြန်စီတယ်။ bubbling up or down ပြန်လုပ်တယ်ပေါ့။

### Removing Elements From Binary Heap
![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%206.1%20removing%20elements%20from%20binary%20heap%20with%20value%20parameter.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%206.2%20removing%20elements%20from%20binary%20heap%20with%20value%20parameter.png)

![Images of heap](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue%20with%20heap%20part%201/fig%206.3%20removing%20elements%20from%20binary%20heap%20with%20value%20parameter.png)

Part 2 မှာ hashtable ကို သုံးပြီးတော့ heap မှာ data ထည့်တာထုတ်တာတွေထပ်ပြောပြပေးသွားပါမယ်။ လက်ရှိမှာ တစ်ချို့ process တွေ က linear of time ကြာပါတယ်။ ဥပမာ remove operation ဆို ဖျက်ရမယ့် value ကို လိုက်ရှာနေရတယ်။ hashtable မှာတော့ အဲ့လို လိုက်ရှာနေစရာမလိုတော့ပဲနဲ့ manage လုပ်သွားနိုင်မှာပါ။

စစဖတ်ဖတ်ခြင်းတော့ နည်းနည်းရှုပ်နိုင်တယ် ၊ ၂ ခေါက် လောက်သေချာလေးဖတ်လိုက်ရင်ရှင်းသွားမှာပါ။

photos credit to Udemy
