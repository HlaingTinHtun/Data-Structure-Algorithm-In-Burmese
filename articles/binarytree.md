## What is a tree & binary tree introduction?

Data Structure ရဲ့ အပိုင်းမှာ tree ဆိုတာက တော်တော်လေးအရေးပါတယ်။ algorithm တော်တော်များများကို tree တွေနဲ့ represent လုပ်ထားကြတဲ့အတွက်ကြောင့်ဖြစ်ပါတယ်။ ဒီနေ့မှာ ကျနော် tree ဆိုတာဘာလဲ ဆိုတဲ့အကြောင်းအရာကို အသုံးများတဲ့ binary tree နဲ့ ဥပမာ ပြုပြီးဆွေးနွေးသွားပါမယ်။

Tree ဆိုတဲ့ သဘောတရားကတော့ ရှင်းတယ်။ Node တစ်ခုနဲ့ တစ်ခု ကို tree structure အတိုင်း တစ်ဆင့်ခြင်းဆီ ချိတ်ဆတ်ထားတယ်၊ ဒါပေမဲ့ ချိတ်ဆက်ထားတဲ့ node တွေက circular ပုံစံဖြစ်သွားတယ်ဆို tree လို့ခေါ်လို့မရတော့ဘူး။ binary tree အကြောင်းကို ဆက်ကြည့်လိုက်မယ်ဆို tree ဆိုတာ ဘယ်လိုလဲဆိုတာ တိတိကျကျမြင်သွားပါလိမ့်မယ်။

Binary tree/binary search tree အတူတူပါပဲ၊ binary tree လို့ပြောလိုက်ပြီဆိုတာနဲ့ Node တစ်ခုမှာ child node နှစ်ခု လို့ ပြေးမြင်ထားလို့ရပါတယ်။ binary tree မှာလည်း သူ့ရဲ့ behavior လေးတွေလဲရှိတယ်။ Node တစ်ခုမှာ အများဆုံး child node နှစ်ခုပဲရှိရမယ်။ left child က parent node ထက် နည်းရမယ်၊ right child က parent node ထက် ကြီးရမယ်။

Tree structure မှာလည်း သူ့ရဲ့ အခေါ်အဝေါ်လေးတွေရှိတယ်။
Root - tree တစ်ခုလုံးရဲ့ ထိပ်ဆုံးက Node.
Parent - parent node ဆိုတာကတော့ သိတဲ့အတိုင်း sub tree (child node) တွေရှိ(ပိုင်ဆိုင်)တဲ့ node.
Child - node တစ်ခုရဲ့ အောက်မှာ sub tree အနေနဲ့ ရှိနေတဲ့ node.
Subtree – node တစ်ခုရဲ့ အောက်မှာရှိတဲ့ sub tree structure တစ်ခု(parent ရှိတယ်၊ child ရှိတယ်။).
Leaf - child node တွေမရှိတဲ့ node.
Tree structure မှာလည်း အဆင့်ဆင့် သတ်မှတ်ထားတဲ့ level တွေလည်း ရှိတယ်၊ ဥပမာ root node က level 1, root node ရဲ့ အောက်က level 2.
Tree structure မှာ search လုပ်တဲ့ အခါတို့ တစ်ခြား operation တွေလုပ်တဲ့ အခါမှာ node တွေတစ်ခုခြင်းဆီ ကို လိုက်ထောက်တာကို လည်း traversing လုပ်တယ်လို့ခေါ်ပါတယ်။

Binary Tree မှာ Basic Operations တွေကို ကြည့်မယ်ဆိုရင်
-	Inserting
-	Searching
-	Removing ရှိမယ်။
Node တွေကို Traversal လုပ်တဲ့ နေရာမှာဆိုရင်
-	Preorder Traversal
-	Inorder Traversal
-	Postorder Traversal
ဆိုပြီးရှိပါတယ်။

ဒီ လောက်ဆိုရင်တော့ tree ဆိုတာကဘာလဲနဲ့ binary tree အကြောင်းကို Introduction အနေနဲ့ လုံလောက်ပြီလို့ထင်ပါတယ်။ နောက်နေ့တွေမှာ Basic operation တွေအတွက် article တစ်ခု ၊ traversal လုပ်တဲ့ ပုံစံတွေအတွက် article တစ်ခု စီ သက်သက်ထပ်တင်ပေးသွားပါမယ်။

photo credits to tutorialpoint


![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binary_tree.jpg)
