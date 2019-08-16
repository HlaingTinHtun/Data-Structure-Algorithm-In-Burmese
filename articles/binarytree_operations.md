## Binary tree’s operation

ဟိုတစ်နေ့ကတော့ binary tree အကြောင်းကို ပြောပြပေးပြီးသွားပြီဆိုတော့ အခု binary tree ရဲ့ operation တွေအကြောင်းကို ပြောပြပေးသွားပါမယ်။ operation တွေကတော့ insert , search , remove ဆိုပြီးတော့ ရှိမယ်၊ တစ်ခုခြင်းဆီ ဘယ်လို အလုပ်လုပ်လဲဆိုတာနဲ့အတူ algorithm အတွက် pseudo sample တွေပါ ရေးပေးသွားပါမယ်။

Operation လုပ်တော့မယ်ဆို ကျနော်တို့ အရင်ဆုံး binary tree ရဲ့ property ကို တစ်ချက် remind လုပ်ရပါမယ်။ node တစ်ခုမှာ child နှစ်ခုရှိတယ်၊ left child က အဲ့ဒီ parent node ထက် ငယ်ရမယ်၊ right child က parent node ထက် ကြီးရမယ်။ ဒါကို မှတ်ထားဖို့လိုမယ်။ operation ဘယ်လိုလုပ်လဲကြည့်ရအောင်။

### Insert Operation

Node တစ်ခုစထည့်တော့မယ်ဆိုရင် သူ့ရဲ့ထည့်ရမယ့်နေရာကို စဉ်းစားရပါတယ်။ ဘာမှမရှိသေးတဲ့ tree ကို node တစ်ခုစထည့်ပြီဆိုရင်တော့ အဲ့ဒီ node က root node ဖြစ်သွားမယ်၊ နောက်ထပ်ထပ်ထည့်ပြီဆို ထည့်တော့မယ့် value က root/parent node ထက် ငယ်လား၊ကြီးလား ကြည့်ရမယ်၊ ငယ်တယ်ဆို ဘယ်ဘက်မှာထည့်၊ ကြီးတယ်ဆို ညာဘက်မှာထည့်ပါမယ်။

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binarytree%20insertion.png)
```
function insert(root , node) //node for new inserting element
  if (empty(root))
    return create Root(node);  //create root with newly inserted node
  if (node <= root.node) // if the inserting node is less than root node
    root.left = create(root.left , node) //insert in left side of the tree
  else  // if the inserting node is greater than root node
    root.right = create(root.right, node) //insert in right side of the tree
```
### Search Operation

Node တစ်ခုကို search တော့မယ်ဆိုရင် tree ရဲ့ root node ကနေပြီးတော့ စရှာတယ်။ ရှာမယ့် value က root node value ထက်ငယ်မယ်ဆို left side ကိုဆင်းပြီးထပ်ရှာတယ်၊ ကြီးတယ်ဆို right side ကိုဆင်းပြီးထပ်ရှာတယ်။ အဲ့လိုနဲ့ပဲအဆင့်ဆင့် node value တွေနဲ့ တိုက်ပြီး ကြီးရင် ညာ၊ ငယ်ရင် ဘယ် နဲ့ ရလဒ်တွေ့တဲ့ ထိရှာသွားတယ်။

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binarytree%20search.png)

```
function search(root, node)
 if (root == null) //failed search
   return null;
 if (node == root.node) //found
   return root;
 if (node < root.node) //if the node is less than root/parent node
   return Search(root.left, node); //continue searching on the left side of tree
 else //if the node is greater than root/parent node
   return Search(root.right, node); //continue searching on the left side of tree
```
### Removing operation
Remove လုပ်တဲ့ နေရာမှာတော့ insert တို့ search တို့လို မရိုးရှင်းဘူး၊ နည်းနည်း tricky ဖြစ်တယ်။ ဘာလို့လဲဆိုတော့ ဖျက်တဲ့ နေရာမှာ case က ၄ ခုဖြစ်နိုင်တယ်။
-	Case I. Leaf node ကိုဖျက်တဲ့case (အောက်က child node မရှိတော့တဲ့ node တစ်ခုကိုဖျက်တာ)
-	Case II. Child node အနေနဲ့ Left side node ပဲရှိတဲ့ node ကိုဖျက်တဲ့ case
-	Case III. Child node အနေနဲ့ right side node ပဲရှိတဲ့ node ကိုဖျက်တဲ့ case
-	Case IV. Child node အနေနဲ့ left ရော right ရောရှိတဲ့ node ကိုဖျက်တဲ့ case

Case II and III ကတော့ အတူတူပဲလို့ပြောလို့ရပါတယ်။

Case I ကိုဖျက်တဲ့နေရာမှာတော့ ရှင်းပါတယ်။ သူ့အောက်မှာ တစ်ခြား ဘာ child node မှမရှိတဲ့ အတွက် တန်းဖျက်လိုက်လို့ရပါတယ်။

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/binarytree%20removing%20case1.png)

Case II ကိုဖျက်တဲ့နေရာမှာတော့ ဖျက်ရမယ့် node အောက်မှာ left side node ထက်ရှိတယ်ဆိုရင် ဖျက်မယ့် node ကိုဖျက်ပြီး အဲ့ node အောက်က left side tree ရဲ့ parent node နဲ့ အစားထိုးလိုက်ရင်ရပါပြီ။ right side လည်း အဲ့နည်းအတိုင်းပါပဲ။

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/fig%201.binary%20tree%20removing%20case2and3.png)

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/fig%202.binary%20tree%20removing%20case2and3.png)


Case IV ကတော့ ပိုရှုပ်ပါတယ်။ ဖျက်မယ့် node တစ်ခု အောက်မှာ left ကော right ကော ရှိတယ်။ အဲ့လို node ကိုဖျက်တော့မယ်ဆို ပိုပြီးသတိထားရပါတယ်၊ binary tree ရဲ့ property မပျက်အောင် ဖျက်ရပါတယ်။ ဖျက်တော့မယ်ဆို left side ဘက်ကိုရွေးမယ်ဆို အကြီးဆုံး value ၊ right side ကိုရှာမယ်ဆို အငယ်ဆုံး value တို့ကို ရှာပြီးတော့ ဖျက်ရမယ့် node ဆီကို replace လုပ်ပြီးတော့ ဖျက်ပါမယ်။ left side ကိုရွေးတယ်ဆို အကြီးဆုံး value ကိုရှာရမှာဖြစ်တဲ့အတွက် tree ရဲ့ ညာဘက် အခြမ်းတွေကို ဆင်းပြီးတော့ right sub tree မရှိတော့တဲ့ node အထိဆင်းသွားမယ်ဆို left side ရဲ့ အကြီးဆုံးကိုရမှာဖြစ်ပြီးတော့၊ right side ကိုရွေးမယ်ဆို ဘယ်ဘက်ကိုတောက်လျောက်ဆင်းသွားပြီး left sub tree မရှိတော့တဲ့ node အထိဆို right side ရဲ့ အငယ်ဆုံး node ကိုရမှာဖြစ်ပါတယ်။ ရလာတဲ့ အငယ်ဆုံး OR အကြီးဆုံး value ကို ဖျက်ရမယ့် node နဲ့ replace လုပ်ပြီး အဲ့ဒီ ခုနက ရှာထားတဲ့ အငယ်ဆုံး OR အကြီးဆုံးရှိတဲ့ node ကိုဖျက်လိုက်ရင်ရပါပြီ။ အဲ့ဖျက်တဲ့ အချိန်မှာတော့ Case I OR case II & III နဲ့ဖျက်သွားလို့ရပါပြီ။

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/fig%201.binary%20tree%20removing%20case4.png)

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/fig%202.binary%20tree%20removing%20case4.png)

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/fig%203.binary%20tree%20removing%20case4.png)

![Image of binarytree](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese/master/assets/binary%20tree/fig%204.binary%20tree%20removing%20case4.png)

```
function delete(root, node)
  if (root == null) // failed search
    return null;
  if (node == root.node) // successful search
    return deletecasefour(root);
  if (node < root.node) // node in the left branch
    root.left = Delete(root.left, node);
  else // node > root.node, i.e., node in the right branch
    root.right = Delete(root.right, node);
  return root;
```
```
function deletecasefour(root)
  if root has two children
    p = Largest(root.left); // replace root with its immediate predecessor p
    root.node = p.node;
    root.left = Delete(root.left, p)
    return root;
  if root has only left child
    return root.left
  if root has only right child
    return root.right
  else root has no children
   return null
```
```
function Largest(Node root)
  if root has no right child
    return root
  return Largest(root.right)
```
photos credit to udemy
