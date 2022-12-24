
# Myan San - Ecommerce

528’s, founded since 2018 and now 4 years ago, is a retail pharmacy company and we sold the products with reasonable price range. Now we planned to move forward as new step by the name MYANSAN for e-business in the future. We will sell our product with fair and reasonable price depends on market demand. We aim that people can easily buy medicine, pharmacy and consumer products from this web and app.

## Tech Enalysis 
```bash
ဒီ markdownလေးကတော့ ကျွန်တော် MyanSanဆိုတဲ့ 
E-commerce website မှာdeveloper အဖြစ်လုပ်နေစဉ်အတွင်း 
ကျွန်တော်လုပ်ခဲ့ရတဲ့ features တွေအကြောင်းပဲဖြစ်ပါတယ်။
ကျွန်တော်ရေးခဲ့တဲ့  အပိုင်းတွေမှာ Bugs တွေ Errors တွေ
တက်လာခဲ့ရင်  အလွယ်တစ်ကူပြင်ဆင်နိုင်ဖို့အတွက် 
Tech Documentation/Flow ရေးသားထားရခြင်းဖြစ်ပါတယ်။
```
## Code overview
- `Customer Order Detail`
ပထမ အပတ်မှာတော့ code flow ကိုနား‌လည်အောင်ကြည့်ခိုင်းပြီး 
customer panelဘက်က order details ကိုလုပ်ရပါတယ်။ 
Orders တွေကိုlistပြတဲ့ နေရာမှာတော့ database ရဲ့
order table ထဲကနေ current userရဲ့ idနဲ့ records တွေကို
လှမ်းဆွဲပြီး view fileမှာ foreachနဲ့ loopပတ်ပြီး
ပြလိုက်ပါတယ်။ Detail အတွက်ကတော့ page reload မဖြစ်စေချင်တဲ့ 
အတွက်ajaxကိုပဲသုံးလိုက်ပါတယ်။ အဲ့အတွက် <a>view</a>
Anchor တစ်ခုဖန်တီးလိုက်ပြီး viewဆိုပြီး သတ်မှတ်လိုက်ပါတယ်။ 
hrefမှာတော့ pageကို effect မဖြစ်စေချင်တဲ့အတွက် 
"javascript:void(0);" ဆိုပြီးထည့်လိုက်ပါတယ်။ ဒီနေရာမှာ 
ရှေ့က javascript ဆိုတာက ဒီanchorကို နှိပ်ရင် href ထဲက 
referenced pathကိုသွားမယ့်အစား javascript codeတွေကို 
run ပါဆိုပြီး ပြောတာဖြစ်ပါတယ်။ voidဆိုတာကတော့ undefinedကို 
return ပြန်ပေးတဲ့ operatorပဲဖြစ်ပါတယ်။ void(0)ကိုသုံးရခြင်းကတော့
လက်ရှိ‌pageကနေ ဘယ်ကိုမှ မသွားပါနဲ့ reload လည်း
မလုပ်ပါနဲ့ဆိုပြီး ပြောလိုက်တာဖြစ်ပါတယ်။ web.phpမှာ ‌defineလုပ်ထားတဲ့ 
urlကိုတော့ data attributeမှာ ထည့်ပေးလိုက်ပါတယ်။ 
ဒီနေရာမှာ hrefကနေမသွားပဲ dataကနေ ထည့်ပေးရတာက view fileကြီးကို 
responseအနေနဲ့ ထည့်ပေးချင်တာမလို့ပါ Detailအတွက်ကတော့ 
order tableရဲ့ unique identifier ဖြစ်တဲ့ order idနဲ့ Controller 
ကို ajaxနဲ့ ပို့လိုက်ပါတယ်။ Controller ကနေမှ detail view bladeကို 
order idကပါလာမယ့် record ပို့ပေးလိုက်ပြီး အဲ့view fileကို response 
အနေနဲ့ ပြန်ပို့ပေးလိုက်ပါတယ်။ ပြီးတော့ ကြိုထည့်ထားတဲ့ divထဲကို view fileကြီး 
ထည့်ပေးလိုက်ပြီးDetailကိုပြလိုက်ပါတယ်။Order list tableကြီးကို
show လုပ်တာ hideလုပ်တာတွေကိုတော့ assetsထဲက jsရဲ့ customထဲမှာ 
order_detail_view.js ဆိုတဲ့ fileမှာ ကြည့်နိုင်ပါတယ်။
- `Dynamic Breadcrumb-area`
After above feature ကျွန်တော် website ကိုလိုက်ကြည့်ရင်း
breadcrumbမှာ urlတွေက အလုပ်မဖြစ်နေပဲ မရှိတဲ့
page တွေကိုခေါ်သလို 404ပဲပြနေပါတယ်။ အဲ့တာကိုပြင်ဖို့codeကို ကြည့်လိုက်တော့
breadcrumbတွေကို view fileတစ်ခုစီမှာ ထပ်ခါထပ်ခါ
သုံးထားတဲ့အတွက် ဒီbreadcrumb areaကို fileတစ်ခုထဲမှာ
ထားလိုက်ပြီး PHP includeနဲ့ master bladeမှာ ခေါ်သုံးလိုက်ပါတယ်။
layouts ထဲက sharedထဲက breadcrumb-area.blade.php ထဲမှာကြည့်နိုင်ပါတယ်။
Requestထဲက segment တွေနဲ့စစ်ပြီး dynamic ဖြစ်အောင်လုပ်ထားလိုက်ပါတယ်။
နောက်ခါ pagesတွေ ထပ်တိုးဖြစ်ရင် အဲ့မှာdefineလုပ်လိုက်ရင်
တစ်ခါတည်းခေါ်သုံးပြီးသား ဖြစ်သွားမှာပါ။
- `Product Magnifying`
Product detailတွေမှာ magnify effect အတွက်ကိုတော့ jqueryscript.net ကနေ 
Product Carousel With magnifying Glass Effect - jQuery exzoom
ဆိုတဲ့ pluginကိုသုံးထားပါတယ်။ အသုံးပြုရတာနဲ့နားလည်ရလွယ်ကူတာမလို့
အရမ်းမရှင်းပြတော့ပါဘူး။ jqueryscript.netမှာ documentation ဖတ်လို့ရပါတယ်။
- `Checkout Page`




