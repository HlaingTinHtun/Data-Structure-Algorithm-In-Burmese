## Binary Tree’s traversal

Binary tree မှာ traversal လုပ်တယ်ဆိုတာ tree ထဲမှာရှိတဲ့ node တွေကို visit လုပ်တာကိုဆိုလိုတာပါ။ tree ထဲမှာရှိတဲ့ level 2 က value 7 ရှိတဲ့ node ကိုလှမ်းထောက်ပါဆို ဒီတိုင်း plain ကြီး သွားထောက်လို့မရပါဘူး။ level 0 ဖြစ်တဲ့ root node ကနေစပြီးတော့ တစ်ဆင့်ခြင်းဆီ အဲ့ဒီ node ကိုရောက်ဖို့အထိ visit လုပ်ရပါတယ်။ အဲ့လို visit လုပ်တာကို traversal လုပ်တယ်လို့ခေါ်ပါတယ်။

Traversal လုပ်တဲ့ နေရာမှာ
-	In-order Traversal
-	Pre-order Traversal
-	Post-order Traversal
-	Level order Traversal
ဆိုပြီးတော့ ရှိပါတယ်။

### In-order Traversal

Inorder ကတော့ ascending order နဲ့သွားတယ်၊ ဘာလို့လဲဆိုတော့ သူ traversal လုပ်တာက left sub tree အရင်လုပ်တယ်၊ ပြီးတော့ မှ root ပြီးတော့မှ right sub tree ကိုလုပ်သွားတယ်။ ဆိုတော့ left to right သွားတဲ့ အတွက်ကြောင့် value တွေကလည်း အစဉ်သင့် ascending order နဲ့ sort ပြီးသားဖြစ်သွားပါတယ်။

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binarytree%20inorder%20traversal.png)

### Pre-order Traversal

Preorder မှာတော့ root ကိုအရင်ဆုံး visit လုပ်တယ်၊ ပြီးတော့မှ left sub tree ကို visit လုပ်ပြီး နောက်ဆုံးမှာမှ right sub tree ကို visit လုပ်တယ်။ root->left sub tree->right sub tree

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binarytree%20preorder%20traversal.png)

### Post-order Traversal

Postorder မှာတော့ root ကိုနောက်ဆုံးမှ visit လုပ်တယ်။ left sub tree ကို အရင် visit လုပ်တယ်၊ ပြီးတော့ right sub tree ၊ နောက်ဆုံးမှ root ဆီ visit လုပ်ပါတယ်။ left sub tree->right sub tree->root

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binarytree%20postorder%20traversal.png)

### Level Order Traversal

Level order ကတော့ tree ရဲ့ level နဲ့ အလိုက် visit လုပ်ပြီး print လုပ်ပါတယ်။ သူအလုပ်လုပ်က အပေါ်ကကောင်တွေလောက်မရိုးရှင်းဘူး၊ queue algorithm ကိုအသုံးပြုပြီးတော့ အလုပ်လုပ်ပါတယ်။ ဘယ်လိုအလုပ်လုပ်လဲဆိုတော့ root node ကနေ စပြီး အလုပ်လုပ်မယ်ဆိုရင် root node ကို အရင် queue ထဲမှာထည့်ထားတယ်၊ အဲ့ node ကို queue ထဲက ထုတ်ပြီး print လိုက်ပြီဆိုတာနဲ့ အဲ့ node ရဲ့ left and right child node တွေကို queue ထဲမှာထည့်ပါတယ်။ အဲ့လိုနည်း နဲ့ပဲ iterate လုပ်သွားပြီးတော့ level အလိုက် node တွေကို ရရှိလာပါတယ်။

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binarytree%20levelorder%20traversal.png)

photos credit to tutorialpoint
