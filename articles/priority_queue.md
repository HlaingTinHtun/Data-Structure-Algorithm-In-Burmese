## Priority Queue In Data Structure & Algorithm

Priority Queue ဆိုတာကတော့ ပုံမှန် regular queue data structure ကိုပဲ အခြေခံပြီးလုပ်ထားတဲ့  structure တစ်ခုပဲ၊ process တော်တော်များများကလည်း ပုံစံအတူတူပဲ၊ မတူပဲ ကွဲပြားသွားတာက ဘာလဲဆိုတာ Priority Queue (PQ လို့ပဲခေါ်သွားပါမယ်) မှာက သူ့ထဲမှာ ပါတဲ့ data node တစ်ခုခြင်းဆီ က priority order လေးတွေပါတယ်။ ဆိုလိုချင်တာက ဘယ် node က ဘယ် node ထက် အရေးကြီးတယ်ဆိုတာမျိုးကို ပြောနိုင်ဖို့အတွက် ကိုယ်ပိုင် priority value လေးတွေပါတယ်။ PQ ကိုယ်တိုင်ကလည်း comparable model ဖြစ်တယ်၊ အဲ့လို compare လုပ်နိုင်ဖို့အတွက် က data node တွေမှာ priority value တွေမဖြစ်မနေပါရမယ်၊ ဒါမှလည်း PQ က ဘယ် node က ပိုအရေးကြီးတယ်ဆိုတာခွဲလို့ရမှာဖြစ်တယ်။ queue algorithm ရဲ့ article ကိုတော့ အောက်က link မှာဖတ်နိုင်ပါတယ်။

https://www.facebook.com/permalink.php?story_fbid=855508051471907&id=100010381592688

PQ အလုပ်လုပ်ပုံက လွယ်မယောင်နဲ့ နည်းနည်းတော့ ခက်ပါတယ်။ ဘာလို့လွယ်တာလဲ ဆိုတော့ သူ့ရဲ့ အလုပ်လုပ်ပုံကရှင်းပါတယ်။ queue တစ်ခုထည့်တော့မယ်ဆို queue ရဲ့ data node နဲ့အတူ သူ့ရဲ့ priority value လည်းပါလာပါတယ်။ PQ က priority value အမြင့်ဆုံး data node ကို အရင် process လုပ်ပေးပါတယ်။ ဥပမာ ပြောရမယ်ဆိုရင် data node တွေရဲ့ priority value တွေက ဒီလိုတွေရှိမယ်ဆိုပါစို့ ၊

4,5,1,3,8,2,1,3,6,9 priority ဂဏန်း အနည်းဆုံး node ကို priority value အမြင့်ဆုံးလို့ သတ်မှတ်ပြီး process လုပ်ကြည့်လိုက်မယ်ဆို အောက်မှာရေးထားသလိုဖြစ်သွားမှာပါ။

1,1,2,3,3,4,5,6,8,9 . PQ က အဲ့လိုပြန် order လုပ်ပြီး run သွားမှာပါ။ ပြောချင်တာက priority value အများဆုံး node တွေကို အရင် run သွားတာပါ။ ဘာလို့ခက်တယ် ပြောတာလဲဆိုတော့ ဒီလိုပါ၊ ကျနော်တို့ က အခု ဘယ် priority value က မြင့်တယ် ဘာညာ ဆိုတာကို မျက်စိနဲ့ ကြည့်ပြီး စီလိုက်လို့ပါ၊ 1 က အမြင့်ဆုံး 9 က အနိမ့်ဆုံး ဆိုတာကို မျက်စိနဲ့ ကြည့်ပြီး တော့ ပဲဆုံးဖြတ်လိုက်တာပါ။ ဒါပေမဲ့ PQ မှာ ဘယ်သူ က မြင့်တယ် ၊ နိမ့်တယ် ဆိုတဲ့ order ကို ဘယ်လိုဆုံးဖြတ်မှာလဲ။ အဲ့လိုဆုံးဖြတ်ဖို့အတွက် data structure နောက်တစ်ခုကိုသုံးပါတယ်။ Heap လို့ခေါ်ပါတယ်။

PQ ဆောက်ဖို့အတွက် heap မှရယ် မဟုတ်ပါဘူး။ တစ်ခြား structure တွေနဲ့လည်း အသုံးပြုပြီး ဆောက်လို့ရတယ်၊ ဒါပေမဲ့ commonly အသုံးများတာကတော့ Heap ပါပဲ။ Heap ဆိုတာဘာလည်း ဆိုတော့ သူက tree based structure တစ်ခုပဲ၊ အဲ့ဒီ tree based structure မှာကိုမှ သူ့ရဲ့ rules တွေရှိတယ် (သူကတော့ heap invariant) လို့ခေါ်တယ်။ ဘာကိုဆိုလိုချင်တာလဲဆိုတော့ သူ့မှာ Min Heap & Max Heap ဆိုပြီး နှစ်မျိုးရှိတယ်။ min heap ဆိုရင်လဲ root node ကအသေးဆုံးဖြစ်ပြီး သူ့အောက် က child node တွေက သူ့ထက် ထပ်သေးသွားလို့မရတော့ဘူး။ max heap လည်း ထိုနည်းလည်းကောင်းပဲ အောက်က child nodes တွေက root ထက် ထပ်ကြီးသွားလို့မရတော့ဘူး။

ဒါဆိုလို့ရှိရင် heap ရဲ့ order အလိုက်စီထားတဲ့ structure နဲ့ PQ ရဲ့ priority value ဆက်စပ်ပုံကို တွေးမိလို့ရမယ်ထင်ပါတယ်။ heap ကလည်း min ဆိုရင် min အတိုင်းစီတယ်။ max ဆို max အတိုင်းစီတယ်။ PQ မှာလည်း priority value ရဲ့ အစဉ်အတိုင်း process လုပ်တယ်။

PQ ကိုသုံးပြီးတော့ implement လုပ်ထားတဲ့ algorithm တွေလည်း ရှိတယ်။ sorting algorithm ဖြစ်တဲ့ heapsort တို့ min key node တွေကို extract လုပ်တဲ့ prim algorithm တို့ load balancing မှာ traffic တွေ manage လုပ်တဲ့ နေရာတို့ စသည်ဖြင့်အသုံးပြုထားတာတွေအများကြီးလည်းရှိတယ်။ တစ်ကယ်လည်း strong ဖြစ်တယ်။

ဒီ article မှာတော့ PQ ကိုအဓိကထားပြီးပြောသွားတဲ့အတွက်ကြောင့် Heap အကြောင်းက Introduction အနေနဲ့ပဲပါသေးတယ်။ Heap ရဲ့ data operation အပိုင်းက နည်းနည်းလေး သေချာကြည့်ရတယ်။ နောက် article မှာ PQ မှာသုံးတဲ့ Heap အကြောင်းကို ထပ်ရေးပေးသွားပါမယ်။

photos credit to Udemy

Priority Queue & Its Instructions
![Images of priority queue](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue/what%20is%20pq%20and%20its%20instruction.png)

What Is A Heap
![Images of priority queue](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/priority%20queue/what%20is%20a%20heap.png)
