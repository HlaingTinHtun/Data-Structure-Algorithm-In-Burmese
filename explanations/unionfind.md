## Union Find Algorithm

Union Find ကို ရှင်းရှင်းလင်းလင်း ဖွင့်ဆိုရမယ်ဆိုရင် တစ်ကွဲတစ်ပြားစီရှိနေတဲ့ object တစ်ခုခြင်းဆီ ဒါမှမဟုတ် object အစုလိုက်ကို find လုပ်ပြီးတော့ တစ်စုတစ်စည်းတည်း ဖြစ်အောင် ပေါင်းလိုက်တာကို union process လို့ ပြောလို့ရပါတယ်။ Union Find ကတော့ အများကြီးပြောစရာမရှိပါဘူး၊ သူ့မှာ အဓိက သုံးတဲ့ function နှစ်မျိုးရှိတယ်၊ သိထားတဲ့ အတိုင်း find & union ပါပဲ။

### Find
ပုံမှန်ဆို object အစုလိုက်ဆိုလို့ရှိရင် parent node တစ်ခုရှိတယ်။ object ကတစ်ခုတည်း ဆိုလို့ရှိရင်လည်း သူ့ကိုယ်တိုင်ကိုပဲ parent node အဖြစ် သတ်မှတ်ထားတယ်။ Find က ဘာလုပ်မလဲဆိုတော့ object အချင်းချင်း မပေါင်းခင်(merge) မှာ သူတို့ရဲ့ parent node ကို လိုက်ရှာတယ်။ Union လုပ်မှာက parent node ကို အခြေခံပြီးလုပ်မှာဖြစ်တဲ့အတွက်ကြောင့်ပါ။

### Union
Find လုပ်ပြီး parent node ကို ရပြီဆိုတာနဲ့ Union လုပ်ပါတယ်။ parent node နှစ်ခုမှာပါတဲ့ objects တွေအားလုံးကိုတစ်ခုတည်း အဖြစ်ပေါင်းလိုက်ပြီး parent node ကိုလဲ တစ်ခုတည်း အဖြစ်သတ်မှတ်လိုက်ပါတယ်။ နှစ်ခုထဲက ဘယ်တစ်ခုကိုဖြစ်ဖြစ်သတ်မှတ်လို့ရပါတယ်။ objects ပိုများများရှိတဲ့ parent node ကိုယူလိုက်တာကတော့ ပိုကောင်းပါတယ်။

### Union Find With Magnet Examples
![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20magnet%20example%201.png)

![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20magnet%20example%202.png)

![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20magnet%20example%203.png)

ဒါပေမဲ့ တိုင်ပတ်တာ တစ်ခုတော့ ရှိတယ်။ အခု လက်ရှိလုပ်နေတဲ့ operation က efficient မဖြစ်ဘူး။ ဘာလို့လဲဆိုတော့ ကျနော်တို့ object နှစ်ခုပေါင်းပြီဆိုပါစို့ A နဲ့ B ပေါင်းတယ်။ A က parent node ဖြစ်သွားတယ်။(A<-B) ပေါ့။ နောက်ထပ် C ဆိုတဲ့ object တစ်ခု ထပ်ပေါင်းမယ်။ ဒီလိုဖြစ်သွားမယ် (A<-B<-C)၊ ဆိုတော့ ကျနော်တို့ C object နဲ့ နောက်ထပ် object တွေ union လုပ်တဲ့အခါ C ရဲ့ parent node ကိုရှာတဲ့ အခါ C ကနေမှတစ်ဆင့် A အထိသွားရှာရပါတယ်။ ဒါက သုံးခုပဲ ရှိသေးလို့ပါ၊ တစ်ကယ်ဆို အများကြီး ရှိနေတဲ့ အချိန်ဆို တစ်ခါတစ်ခါ union လုပ်တော့ မယ်ဆို parent node ကို တစ်ဆင့်ခြင်းဆီ သွားရမယ်ဆိုရင်တော့ သိပ်မဟုတ်တော့ပါဘူး။ ဒီလိုဖြစ်လာတဲ့အတွက် path compression ဆိုတဲ့ အရာကို apply လုပ်ထားပါတယ်။

Path compression ဆိုတာက တော့ သူ့နာမည်အတိုင်းပဲ သွားရမယ့် path ကိုချုံ့ လိုက်မှာ။ ဆိုလိုချင်တာက ကျနော်တို့အရင် priority queue article ရေးတုန်းက lookup table နဲ့ node value & position value တွဲပြီးတော့ သိမ်းထားသလိုပဲ ၊ ဒီမှာလဲ follower node ကို join မလုပ်တော့ဘဲ parent node ကို တိုက်ရိုက်သွား Join လိုက်တယ်။ ဆိုလိုချင်တာက ဒီလို (A<-B<-C) join မယ့်အစား (A<-B),(A<-C) ဆိုပြီး parent node ကိုပဲတိုက်ရိုက် join လိုက်မယ်။ အဲ့ဒါဆိုရင် parent node ရှာရတော့မယ့်အချိန်မှာ တစ်ဆင့်ချင်းစီ လိုက်ရှာနေစရာမလိုတော့ ဘဲ parent node ကို အလွယ်တကူတွေ့ပြီး Union လုပ်နိုင်မှာပါ။

### Union Find With Path Compression
![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20path%20compression.png)

ဘယ်နေရာတွေမှာ apply လုပ်လို့ရလဲဆိုရင် connectivity တွေကို unionized လုပ်ထားတဲ့ architecture တွေ algorithm တွေမှာ သုံးလို့ရပါတယ်။ ဥပမာ Kurskal algorithm ဆို node တစ်ခုချင်းဆီကို ascending structure နဲ့ union လိုက်လုပ်ပြီး minimum path ကိုရှာတယ်။ တစ်ခြား Network connectivity infra တွေမှာလည်း Union Find ကိုသုံးတာတွေရှိပါတယ်။

ကျနော် pseudo code နဲ့ algorithm sample လေးပါထည့်ပေးလိုက်ပါတယ်။

function find( x )
  if(x != x.parent)
    x.parent = find(x.parent)
    return x.parent
  else
    return x

function union(x,y)
  x = find( x ), y = find( y ) //find the root of each element
  if ( x is equal to y )
    return success
  else
    set x as y’s parent

photos credit to Udemy
