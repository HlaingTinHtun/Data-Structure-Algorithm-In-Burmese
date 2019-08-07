## Union Find Algorithm

Union Find ကိုု ရွင္းရွင္းလင္းလင္း ဖြင့္ဆိုုရမယ္ဆိုုရင္ တစ္ကြဲတစ္ျပားစီရွိေနတ့ဲ object တစ္ခုုျခင္းဆီ ဒါမွမဟုုတ္ object အစုုလိုုက္ကိုု find လုုပ္ျပီးေတာ့ တစ္စုုတစ္စည္းတည္း ျဖစ္ေအာင္ ေပါင္းလိုုက္တာကိုု union process လိုု႔ ေျပာလိုု႔ရပါတယ္။ Union Find ကေတာ့ အမ်ားျကီးေျပာစရာမရွိပါဘူး၊ သူ႔မွာ အဓိက သံုုးတ့ဲ function ႏွစ္မ်ိဳးရွိတယ္၊ သိထားတ့ဲ အတိုုင္း find & union ပါပဲ။

### Find
ပံုုမွန္ဆိုု object အစုုလိုုက္ဆိုုလိုု႔ရွိရင္ parent node တစ္ခုုရွိတယ္။ object ကတစ္ခုုတည္း ဆိုုလိုု႔ရွိရင္လည္း သူ႔ကိုုယ္တိုုင္ကိုုပဲ parent node အျဖစ္ သတ္မွတ္ထားတယ္။ Find က ဘာလုုပ္မလဲဆိုုေတာ့ object အခ်င္းခ်င္း မေပါင္းခင္(merge) မွာ သူတိုု႔ရဲ႕ parent node ကိုု လိုုက္ရွာတယ္။ Union လုုပ္မွာက parent node ကိုု အေျခခံျပီးလုုပ္မွာျဖစ္တ့ဲအတြက္ေျကာင့္ပါ။

### Union
Find လုုပ္ျပီး parent node ကိုု ရျပီဆိုုတာနဲ႔ Union လုုပ္ပါတယ္။ parent node ႏွစ္ခုုမွာပါတ့ဲ objects ေတြအားလံုုးကိုုတစ္ခုုတည္း အျဖစ္ေပါင္းလိုုက္ျပီး parent node ကိုုလဲ တစ္ခုုတည္း အျဖစ္သတ္မွတ္လိုုက္ပါတယ္။ ႏွစ္ခုုထဲက ဘယ္တစ္ခုုကိုုျဖစ္ျဖစ္သတ္မွတ္လိုု႔ရပါတယ္။ objects ပိုုမ်ားမ်ားရွိတ့ဲ parent node ကိုုယူလိုုက္တာကေတာ့ ပိုုေကာင္းပါတယ္။

### Union Find With Magnet Examples
![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20magnet%20example%201.png)

![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20magnet%20example%202.png)

![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20magnet%20example%203.png)

ဒါေပမ့ဲ တုုိင္ပတ္တာ တစ္ခုုေတာ့ ရွိတယ္။ အခုု လက္ရွိလုုပ္ေနတ့ဲ operation က efficient မျဖစ္ဘူး။ ဘာလိုု႔လဲဆိုုေတာ့ က်ေနာ္တိုု႔ object ႏွစ္ခုုေပါင္းျပီဆိုုပါစိုု႔ A နဲ႔ B ေပါင္းတယ္။ A က parent node ျဖစ္သြားတယ္။(A<-B) ေပါ့။ ေနာက္ထပ္ C ဆိုုတ့ဲ object တစ္ခုု ထပ္ေပါင္းမယ္။ ဒီလိုုျဖစ္သြားမယ္ (A<-B<-C)၊ ဆိုုေတာ့ က်ေနာ္တိုု႔ C object နဲ႔ ေနာက္ထပ္ object ေတြ union လုုပ္တ့ဲအခါ C ရဲ႕ parent node ကိုုရွာတ့ဲ အခါ C ကေနမွတစ္ဆင့္ A အထိသြားရွာရပါတယ္။ ဒါက သံုုးခုုပဲ ရွိေသးလိုု႔ပါ၊ တစ္ကယ္ဆိုု အမ်ားျကီး ရွိေနတ့ဲ အခ်ိန္ဆိုု တစ္ခါတစ္ခါ union လုုပ္ေတာ့ မယ္ဆိုု parent node ကိုု တစ္ဆင့္ျခင္းဆီ သြားရမယ္ဆိုုရင္ေတာ့ သိပ္မဟုုတ္ေတာ့ပါဘူး။ ဒီလိုုျဖစ္လာတ့ဲအတြက္ path compression ဆိုုတ့ဲ အရာကိုု apply လုုပ္ထားပါတယ္။

Path compression ဆိုုတာက ေတာ့ သူ႔နာမည္အတိုုင္းပဲ သြားရမယ့္ path ကိုုခ်ဳံ႕ လိုုက္မွာ။ ဆိုုလိုုခ်င္တာက က်ေနာ္တိုု႔အရင္ priority queue article ေရးတုုန္းက lookup table နဲ႔ node value & position value တြဲျပီးေတာ့ သိမ္းထားသလိုုပဲ ၊ ဒီမွာလဲ follower node ကိုု join မလုုပ္ေတာ့ဘဲ parent node ကိုု တိုုက္ရုုိက္သြား Join လုုိက္တယ္။ ဆိုုလိုုခ်င္တာက ဒီလိုု (A<-B<-C) join မယ့္အစား (A<-B),(A<-C) ဆိုုျပီး parent node ကိုုပဲတိုုက္ရုုိက္ join လိုုက္မယ္။ အ့ဲဒါဆိုုရင္ parent node ရွာရေတာ့မယ့္အခ်ိန္မွာ တစ္ဆင့္ခ်င္းစီ လိုုက္ရွာေနစရာမလိုုေတာ့ ဘဲ parent node ကိုု အလြယ္တကူေတြ႔ျပီး Union လုုပ္ႏိုုင္မွာပါ။

### Union Find With Path Compression
![Images of unionfind](https://raw.githubusercontent.com/HlaingTinHtun/Data-Structure-Algorithm-In-Burmese-Explanations/master/medias/union%20find/union%20find%20with%20path%20compression.png)

ဘယ္ေနရာေတြမွာ apply လုုပ္လိုု႔ရလဲဆိုုရင္ connectivity ေတြကိုု unionized လုုပ္ထားတ့ဲ architecture ေတြ algorithm ေတြမွာ သံုုးလိုု႔ရပါတယ္။ ဥပမာ Kurskal algorithm ဆိုု node တစ္ခုုခ်င္းဆီကိုု ascending structure နဲ႔ union လိုုက္လုုပ္ျပီး minimum path ကိုုရွာတယ္။ တစ္ျခား Network connectivity infra ေတြမွာလည္း Union Find ကိုုသံုုးတာေတြရွိပါတယ္။

က်ေနာ္ pseudo code နဲ႔ algorithm sample ေလးပါထည့္ေပးလိုုက္ပါတယ္။

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
