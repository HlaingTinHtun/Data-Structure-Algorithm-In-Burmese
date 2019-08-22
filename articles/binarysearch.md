## Binary Search Algorithm

Binary search ကတော့ strong ဖြစ်တဲ့ searching algorithm တစ်ခုဖြစ်ပြီးတော့ divide & conquer algorithm အပေါ်မှီငြမ်းထားပြီးအလုပ်လုပ်ပါတယ်။
Binary search intro နဲ့ time complexity အကြောင်းဖတ်ရန် - http://bit.ly/2KHIOhy
Divide & conquer အကြောင်းဖတ်ရန် - http://bit.ly/2H8MIOb

Binary search algorithm အလုပ်လုပ်ဖို့ဆိုရင် data value တွေက sorted form နဲ့ရှိထားရပါတယ်။ ဘာလို့လဲဆိုတော့ သူအလုပ်လုပ်ပုံက data collection ထဲကနေ middle item ကိုလှမ်းထောက်တယ်၊ ရလာတဲ့ key နဲ့ ရှာမယ့် key ကိုတိုက်စစ်ပြီး ငယ်တယ်ဆို ဘယ်ဘက်ကိုရွေ့ ပြီး mid item ထပ်ရှာ၊ ကြီးတယ်ဆို ညာဘက်ရွေးပြီး mid item ထပ်ရှာ၊ တူတာတွေ့ပြီဆို ရင်တော့ process ပြီးပြီပေါ့၊ မတွေ့သေးသမျှတော့ middle most node ကို ထောက်ထောက်ပြီးတော့ အလုပ်လုပ်သွားတယ်။ ဒါကြောင့်မို့လို့ data collection တွေက တိုက်စစ်ပေးနိုင်ဖို့အတွက် sorted form ဖြစ်နေရမယ်ပြောတာ။

ကျနော်တို့ example တစ်ခုအနေနဲ့ binary search ကိုသုံးပြီး ရှာကြည့်ကြရအောင်။ Photo attach တွဲပေးထားတာကိုကြည့်ပါ။

![Images of linked list](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/Binary-Search.png)

Array 10 ခုပါတဲ့ data collection တစ်ခုမှာ 23 ပါတဲ့ array key ကိုရှာကြမယ်ဆိုပါစို့။
ပထမဆုံး အဆင့် အနေနဲ့ medium node ကို အရင်ရှာပါတယ်၊ ဒီ formula နဲ့ ရှာလို့ရပါတယ်။
mid = low + (high - low) / 2
mid = 0 + (9 - 0 ) / 2 = 4 လို့ပဲယူထားလိုက်ပါမယ်။(integer value of 4.5)

arrray key 4 ဖြစ်တဲ့ value 16 ရပါတယ်။ ကျနော်တို့ရှာမယ့် 23 က16ထက်ကြီးတယ်ဆိုတော့ ညာဘက် sub collection ကိုထပ်ရွေးပြီးတော့ medium ထပ်ရှာပါမယ်။ ကြီးတဲ့ညာဘက် ကိုသွားမယ်ဆို
low = medium + 1
mid = 5 + (9 - 5 ) / 2 = 7 ရပါတယ်။

array key 7 ဖြစ်တဲ့ 56 ကိုရပါမယ်။ ကျနော်တို့ ရှာတဲ့ 23 မရသေးပါဘူး။ 23 က 56 ထက်ငယ်တာဖြစ်တဲ့အတွက် ဘယ်ဘက် sub collection ကိုထပ်ရွေးပြီးတော့ medium ထပ်ရှာပါမယ်။ ငယ်တဲ့ဘယ်ဘက်ကို သွားမယ်ဆို
high = medium -1
mid = 5 + (6-5)/2 = 5 ရပါမယ် (integer value of 5.5)

array key 5 ဖြစ်တဲ့ 23 ကိုရပါပြီ၊ ကျနော်တို့ ရှာချင်တဲ့ array key ကိုရှာတွေ့သွားတာပဲဖြစ်ပါတယ်။

#### Pseudo code sample
```
Function search(root, node)
 if (root == null) //failed search
   return null;
 if (node == root.key) //succesfull search
   return root;
 if (node < root.key) //node in left branch
   return Search(root.left, k);
 else //node > root.key, i.e. node in right branch
   return Search(root.right, k);
```
photos credit to geeksforgeeks
