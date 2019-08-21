## Queue In Data Structure & Algorithm

Queue ကတော့ stack နဲ့ဆင်တယ်။ stack နဲ့မတူတာကကျ stack က one ended ကိုပဲ data အသွင်းအထုတ်ရတယ်။ queue ကကျတော့ တစ်ဖက်ကဝင် တစ်ဖက်ကထွက်ပုံစံမျိုး။ insert လုပ်ဖို့အတွက်ကို enqueue လို့ခေါ်ပြီးတော့ remove လုပ်ဖို့ကိုကျ dequeue လို့ခေါ်တယ်။ stack တုန်းက LIFO (last in first out) structure အတိုင်း ဆိုပေမဲ့ queue မှာတော့ FIFO(first in first out) ပဲ၊ အရင်ဝင်လာတဲ့ process က အရင်ပြန်ထွက်တယ်၊ နောက်မှဝင်လာတဲ့ ကောင်က နောက်မှ ထွက်ရမယ်။ real world example အနေနဲ့ ပြောရရင် starbucks မှာ ကော်ဖီ မှာဖို့တန်းစီ ပြီး စောင့်နေတဲ့ လူတွေမျိုး၊ အရင်ရောက်တဲ့ လူက အရင်မှာတယ်။ ပြီးရင် ထွက်သွားတယ်။

ဒီ article မဖတ်ခင် stack algorithm ရဲ့ article ကိုအရင်ဖတ်ဖို့ recommend လုပ်ချင်ပါတယ်။

Stack လိုပဲ queue ကို array တွေ linked lists တွေသုံးပြီးတော့ ဆောက်လို့ရတယ်။ queue process မှာ queue ဆောက်တာတို့  stack မှာလိုပဲ ထိပ်ဆုံး element ကို access လုပ်ဖို့ဆို peek ဆိုတာကိုသုံးတာတို့၊ queue က ပြည့် နေပြီးလား empty ဖြစ်နေလားစတာတွေကို စစ်တဲ့ function တွေလဲရှိတယ်။ အဓိက အသုံးများတာကတော့ အပေါ်မှာပြောထားတဲ့ function နှစ်ခုဖြစ်တဲ့ enqueue နဲ့ dequeue ပဲ။ queue အတန်းကြီးတစ်ခုရှိတယ်ဆိုပါစို့၊ ညာဘက်(အနောက်ဘက်) ကို queue ထည့်ဖို့ (enqueue) လုပ်ဖို့သုံးတယ်၊ queue ရဲ့ ဘယ်ဘက်(အရှေ့ဘက်)ကို queue remove လုပ်ဖို့သုံးတယ်၊ attach လုပ်ထားတဲ့ပုံနဲ့ တွဲကြည့်လိုက်ရင်တော့ ပိုမြင်သွားပါလိမ့်မယ်။

### A Queue
![Images of queue](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/queue/understanding%20queue/whatisqueue.png)

### Enqueue
![Images of queue](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/queue/understanding%20queue/enqueue.png)

### Dequeue
![Images of queue](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/queue/understanding%20queue/dequeue.png)

Queue တွေဘယ်လိုထည့်လဲဆိုတော့ (enqueue operation)
-	အသစ်ထည့်တော့မယ်ဆို queue ပြည့်နေပြီလားစစ်တယ်
-	ပြည့်နေတယ်ဆို သက်ဆိုင်တဲ့ msg ပြန်ပြီးတော့ exit လုပ်တယ်
-	ထပ်ထည့်လို့ရသေးတယ်ဆို stack မှာလိုမျိုးပဲ top element ကို access လုပ်တဲ့ top pointer queue မှာလဲ access လုပ်လို့ရတဲ့ rear pointer ဆိုတာရှိတယ်၊ အဲ့ဒီ pointer ကို +1 လုပ်ပြီး နောက်ဝင်လာမယ့် process အတွက် empty space ကို ထောက်ပေးထားတယ်
-	နောက်တစ်ဆင့် အနေနဲ့ rear pointer ထောက်ထားတဲ့ empty space ကို value ထည့်တယ်
-	Operation success ဖြစ်တဲ့ အကြောင်း return ပြန်တယ်

### Adding Queue
![Images of queue](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/queue/understanding%20queue/adding%20queue%20instruction.png)

### Removing Queue
![Images of queue](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/queue/understanding%20queue/removing%20queue%20instruction.png)

ဒီနေရာမှာ stack နဲ့ မတူတာကျ stack က one ended ဆိုတော့ ထည့်တာရောထုတ်တာရော တစ်ဖက်တည်းကသွားတာဖြစ်တဲ့ အတွက်ကြောင့် pointer က တစ်ခုပဲရှိစရာလိုတယ်။ နှစ်ဖက်လုံးအလုပ်လုပ်တဲ့ queue မှာတော့ enqueue အတွက် ဆို rear (back pointer) နဲ့ dequeue အတွက် front pointer ဆိုပြီး ခွဲထားတယ်။

Queue တွေဘယ်လိုထုတ်လဲဆိုတော့ (dequeue operation)
-	queue က empty ဖြစ်နေလားအရင်ကြည့်တယ်
-	Empty ဖြစ်နေတယ်ဆို သက်ဆိုင်တဲ့ msg ပြန်ပြီးတော့ exit လုပ်တယ်
-	Empty မဖြစ်ဘူးဆိုရင် လက်ရှိ front pointer ထောက်ထားတဲ့ data ကို access လုပ်တယ်။
-	နောက်တစ်ဆင့် အနေနဲ့ front pointer ကနေ backward သွားပြီး နောက် data element တစ်ခုကို access လုပ်ပြီး ရှေ့ ကဟာကို queue ထဲကနေ ထုတ်လိုက်တယ်
-	Operation success ဖြစ်တဲ့ အကြောင်း return ပြန်တယ်

 Queue algorithm ကိုဘယ်နေရာတွေမှာသုံးလဲဆိုတော့ ဥပမာ အနေနဲ့ ပြောရမယ်ဆိုရင် web server ကိုလာတဲ့ request တွေ handle လုပ်တဲ့ နေရာမှာသုံးလို့ရတယ်၊ request တစ်သိန်းလာတယ်၊ ဒါပေမဲ့ server က တစ်ခါ process လုပ်ရင် တစ်ထောင်ပဲရတယ်၊ ကျန်တဲ့ request တွေကို queue ထဲထည့်ထားပြီးတော့ first come first serve ပုံစံမျိုးနဲ့ အလုပ်လုပ်သွားတယ်၊ web server request မှရယ်မဟုတ်ဘူး၊ ကျန်တဲ့ batch request တွေကို လည်း queue သုံးပြီး manage လုပ်လို့ရပါတယ်။ တစ်ခြားသော scheduling case တွေမှာလဲ သုံးလို့ရတယ်၊ round robin scheduling တို့ Job scheduling တို့ စသည်ဖြင့် FIFO (first in first out) order နဲ့ သွားတဲ့ logic မှန်သမျှကို queue နဲ့ implement လုပ်လို့ရတယ်။ အခုနောက်ပိုင်းဆို Redis queue ဆိုရင် program တွေ တော်တော်များများ ထဲမှာ integrate လုပ်လာကြပါတယ်။တစ်ခြား multitasking လုပ်တဲ့ feature တွေမှာလည်း queue ကိုအသုံးပြုလို့ရပါတယ်။

 photos credit to Udemy
