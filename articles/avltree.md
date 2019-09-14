## AVL Tree

AVL tree ဆိုတာကတော့ binary tree ကို modify ထပ်လုပ်ထားတဲ့ balanced binary tree ကိုအခြေခံထားတဲ့ algorithm တစ်ခုပဲဖြစ်ပါတယ်။ Binary tree ရှိရဲ့ သားနဲ့ balanced binary ဆိုပြီး ဘာလို့ထပ်လာတာလဲမေးစရာရှိပါတယ်။ ရှင်းပါတယ်၊ binary tree ကမပြည့်စုံသေးလို့ပါ၊ ဘာလို့လဲဆိုတော့ binary tree ရဲ့ worst case တွေမှာ performance က linear time အထိ ပြန်နိမ့်ကျသွားလို့ပါ။ ဥပမာ 1, 2, 3, 4, 5, 6, 7 ကို binary tree နဲ့ စီထည့် လိုက်မယ်ဆို tree က right side ကိုပဲ တစ်ဖတ်သတ်ချည်းစီသွားလိုက်မယ်၊ ဘာလို့right side ကိုဆင်းသွားလဲဆိုတာမသိရင် binary tree articles တွေပြန်ဖတ်ဖို့လိုပါတယ်။ အောက်က link တွေမှာဖတ်ပါ။

Binary tree
http://bit.ly/2MpDLnX

Binary tree's operation
http://bit.ly/2YZiqIv

Binary tress's traversal
http://bit.ly/31L0oH1

Binary search
http://bit.ly/2KZCTDe

စကားပြန်ဆက်ရမယ်ဆို ဆိုလိုချင်တာက node တစ်ခု insert ထည့်တော့မယ်ဆို process က ၆ ခါလုပ်ရပါမယ်၊ ဆိုတော့ linear အတိုင်းပဲပြန်ကြာသွားပါလိမ့်မယ်။ အဲ့အတွက်ကြောင့် မို့လို့ binary tree တွေကို balanced ထပ်လုပ်ဖို့လိုအပ်လာတာပါ။ balanced လုပ်ထားတဲ့ tree ဆိုရင် linear time မကြာဘဲ နဲ့ process ကိုလျော့ချ နိုင်ပြီး performance အတွက်ပိုကောင်းပါတယ်။ attachment မှာ sample ကြည့်နိုင်ပါတယ်။

![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig1.1%20advantages%20of%20avl%20tree.png)

Balanced binary tree မှာ အခရာကျတာက binary tree ကို rules (ဘယ်ကငယ်၊ညာကကြီး) ကိုလိုက်နာနိုင်ဖို့နဲ့ နောက်တစ်ချက် က tree rotation ပါပဲ။ Tree rotation ဘယ်လိုလုပ်လဲဆိုတာ အောက်က attachment example ပုံလေးတွေမှာ တစ်ဆင့်ခြင်းဆီကြည့်လို့ရပါတယ်။

#### Tree Rotation Sample
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig2.1%20tree%20rotation%20sample.png)

#### Tree Rotation Example 1
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig2.2%20tree%20rotation%20sample.png)

#### Tree Rotation Example 2
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig2.3%20tree%20rotation%20sample.png)

#### Tree Rotation Example 3
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig2.4%20tree%20rotation%20sample.png)


AVL tree ဆိုတာလဲ balancing လုပ်ထားတဲ့ tree ပါပဲ။ avl မှာတော့ tree ရဲ့ height ကိုယူပြီးတော့ balance ဖြစ်အောင်လုပ်ပါတယ်။ height တွေကိုအခြေခံပြီး balance factor တွက်ပါတယ်။

BalanceFactor = height(left-sutree) − height(right-sutree).
Sub tree တစ်ခုမှာ balance factor ကို 1 ထက်ကြီးလို့မရပါဘူး။ ဆိုလိုချင်တာက difference 1 ပဲလက်ခံပါတယ်။ ဥပမာ -1,1,0 ဖြစ်မှသာ balance ဖြစ်ပါမယ်။ နမူနာပုံ attach တွဲပေးလိုက်ပါတယ်။

![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig3.1%20avl%20tree%20example.jpg)

Rotation 4 မျိုး ရှိပါတယ်။ စာနဲ့ရှင်းပြတာထက်စာရင် ပုံလေးတွေနဲ့ ပိုနားလည်လွယ်မယ်ထင်ရတဲ့ အတွက် tutorial point က ပုံလေးတွေယူပြီး reference လုပ်လိုက်ပါတယ်။

#### Left Rotation
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig3.2%20avl_left_rotation.jpg)

#### Right Rotation
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig3.3%20avl_right_rotation.jpg)

#### Left Right Rotation
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig3.4%20left_right_rotation.png)

#### Right Left Rotation
![Image of avl](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/AVL%20tree/fig3.5%20right_left_rotation.png)

Insert လုပ်တာ remove လုပ်တာတွေကတော့ binary tree အတိုင်းပါပဲ။ ပိုသွားတာက insert လုပ်တဲ့ အချိန်မှာ binary tree အတိုင်း insert လုပ်ပြီးရင် sub tree ရဲ့ balance factor ကိုပြန်စစ်ရတာပါပဲ။ balance factor မမှန်ရင် rotation လုပ်ပြီး balance ညှိရမှာမို့လို့ပါ။


Photos credit goes to
w3schools.in, udemy, tutorialspoint
