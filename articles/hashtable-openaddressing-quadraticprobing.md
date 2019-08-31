## Hash table - Open addressing (Quadratic Probing)

Hash table အကြောင်းရေးနေတဲ့ series ထဲ က open addressing မှာသုံးတဲ့ probing function တစ်ခုဖြစ်ပါတယ်။ အရင် article တွေ ဖတ်ပြီးမှ ဒီ article ဖတ်တာ ပိုအဆင်ပြေပါမယ်။

Hash table (hashing)
http://bit.ly/2NCd4MH
Hash table (Separate Chaining)
http://bit.ly/2KSdJaN
Hash table (Open Addressing)
http://bit.ly/2ZkEdL8
Hash table (Open Addressing - Linear probing)
http://bit.ly/2ZCjbTx

ဒီ article ကတော့ နည်းနည်းတိုသွားမယ်။ ဘာလို့လဲဆိုတော့ data collision ဖြစ်တာတို့ open addressing သုံးတဲ့ နေရာမှာ cycle issue ဖြစ်တာတွေအတွက် အရှေ့ က article တွေမှာ လုံလုံလောက်လောက်ရှင်းပြပြီးသွားပြီဖြစ်ပါတယ်။

Quadratic probing ကတော့ quadratic formula ကိုသုံးပြီး probing လုပ်တယ်။ eg. (a*square of x + bx +c). a != 0 ဖြစ်ရမယ်။ အရင် article တွေမှာ ပြောခဲ့သလိုပဲ probing function တွေမှာ cycle issue ရှိတတ်သလိုပဲ အခုပြောမယ့် quadratic probing မှာလည်း ဒီ issue ရှိပါတယ်။ ကျန်တဲ့ process တွေက linear probing နဲ့အတူတူပဲ။ မတူတဲ့ အချက်က linear probing မှာ cycle issue ကိုရှင်းနိုင်ဖို့အတွက် GCD တန်ဖိုးရှာပြီး ထိန်းသွားတယ်။ quadratic မှာတော့ ရှင်းနိုင်မယ့် formula တွေအများကြီးရှိတယ်။ အဲ့ထဲကမှ သုံးမျိုးလောက်ကို sharing လုပ်ပေးလိုက်ပါမယ်။ udemy course တစ်ခုကနေ မှီငြမ်းယူထားပါတယ်။

1.	P(x) = square of x , table size N number က prime ဖြစ်ပြီးတော့ 3 ထက်ကြီးရမယ်၊ max load factor ကလဲ less than or equal by 1/2 ဖြစ်ရမယ်။
2.	P(x) = (square of x + x)/2 , ပြီးတော့ table size N က power of 2 ဖြစ်ရပါမယ်။ ဥပမာ 2 power 2 = 4 , 2 power 3 = 8 စသည်ဖြင့်ပေ့ါ။
3.	P(x) = (-1 power of x) * square of x, ပြီးတော့ table size N က prime number ဖြစ်ပြီးတော့ 3 mod 4 နဲ့ identical ဖြစ်ရမယ်။ ဥပမာ size N က 23 (prime number) . 3 mod 4 ဆို 3 ရမယ်။ ထိုနည်းလည်းကောင်းပဲ 23 mod 4 ဆိုရင်လည်း 3 ရမယ်။ ဒီလိုမျိုးဖြစ်ရမယ်လို့ဆိုလိုတာပါ။

Number 1 , 2 နည်းကတော့ တွက်ရတာ ပိုလွယ်မယ်လို့ထင်ပါတယ်။ အပေါ်က ရေးထားတဲ့ formula တွေအတိုင်း probing ကိုတွက်မယ်ဆိုရင် cycle issue မဖြစ်နိုင်တော့ဘဲနဲ့ completely fill up လုပ်နိုင်သွားမှာပါ။

![Images of hashtable](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/hashtable/open%20addressing/quadratic%20probing.png)
photo credits to udemy

Table ရဲ့ threshold ပြည့်သွားလို့ table resizing လုပ်တဲ့ ပုံစံလည်း linear probing မှာလုပ်တာနဲ့ အတူတူပါပဲ။ cycle issue ကိုကိုင်တွယ်ပုံပဲကွာသွားမှာပါ။

နောက် article မှာ double hashing အကြောင်းရေးပေးသွားပါမယ်။ ဒါဆိုရင်တော့ hash table အကြောင်း လည်းတော်တော်စုံသွားပြီး လုံလောက်ပြီလို့ထင်ပါတယ်။
