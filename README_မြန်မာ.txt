YNS Kitchen Promotion Update (Worker v17)

ပါဝင်သောဖိုင်များ
1. worker.js — Promotion စည်းမျဉ်းများကို Server ဘက်တွင် စစ်ဆေးသည်။
2. index.html — Checkout တွင် နောက်ဆုံးအော်ဒါ Voucher Number ထည့်ရန် အကွက်ပါသည်။
3. admin/promos.html — Promotion စီမံခန့်ခွဲမှုစာမျက်နှာ။

တင်သွင်းမီ
- လက်ရှိ worker.js, index.html နှင့် admin/promos.html ကို Backup သိမ်းပါ။
- သင့် Worker တွင် အသုံးပြုနေသော DB binding နှင့် အခြား Environment Variables များကို မပြောင်းပါနှင့်။

တင်သွင်းနည်း
1. ZIP ထဲက worker.js ကို လက်ရှိ Cloudflare Worker code နဲ့ အစားထိုးပြီး Deploy လုပ်ပါ။
2. index.html ကို လက်ရှိ public index.html နေရာတွင် အစားထိုးပါ။
3. admin/promos.html ကို admin/promos.html နေရာတွင် တင်ပါ။
4. Admin > Promos ကိုဖွင့်ပြီး Promo Codes, Loyalty, VIP နှင့် Spend Threshold ဆက်တင်များကို စမ်းသပ်ပါ။
5. Settings/API တွင် Worker version 17 ပြကြောင်း စစ်ပါ။

ထည့်သွင်းထားသောအင်္ဂါရပ်များ
- Promo code စနစ်ကို အပြည့်ဖွင့်/ပိတ်နိုင်သည်။
- Loyalty အော်ဒါအကြိမ်ရေ လျှော့ဈေးကို သီးခြားဖွင့်/ပိတ်နိုင်သည်။
- VIP: ယခင်အော်ဒါစုစုပေါင်းသုံးစွဲငွေ သတ်မှတ်ချက်ပြည့်သူကို ရာခိုင်နှုန်းအလိုက် လျှော့နိုင်သည်။
- Spend threshold: စုစုပေါင်းသုံးစွဲငွေ သတ်မှတ်ချက်ပြည့်ပြီးနောက် အော်ဒါတစ်ခုချင်းစီတွင် သတ်မှတ်ငွေလျှော့နိုင်သည်။
- ဖုန်းနံပါတ်နဲ့ ချိတ်ထားသော voucher နှင့် auto reward များအတွက် နောက်ဆုံးအော်ဒါ Voucher Number ကိုလည်း စစ်ဆေးသည်။
- Birthday နှင့် referral အတွက် Admin က customer-specific voucher ကို ကိုယ်တိုင်ထုတ်ပေးသည့် campaign toggle များ ထည့်ထားသည်။

အရေးကြီးသော ကန့်သတ်ချက်များ
- Birthday အလိုအလျောက်ပေးရန် customer profile တွင် မွေးနေ့ကို စနစ်တကျသိမ်းဆည်းခြင်းနှင့် တစ်နှစ်တစ်ကြိမ်ပေးခြင်းကို ထပ်မံတည်ဆောက်ရန်လိုသည်။ ယခု version တွင် မွေးနေ့အလိုအလျောက်စစ်ဆေးခြင်း မပါသေးပါ။
- Referral အလိုအလျောက်စနစ်အတွက် referral code ဖန်တီးခြင်း၊ အခြား customer က အသုံးပြုခြင်းနှင့် နှစ်ဖက် reward ထုတ်ပေးခြင်း flow ကို ထပ်မံတည်ဆောက်ရန်လိုသည်။ ယခု version တွင် referral အလိုအလျောက်ရေတွက်ခြင်း မပါသေးပါ။ Campaign toggle များသည် manual voucher campaign အတွက်သာ ဖြစ်သည်။
- နောက်ဆုံး Voucher Number စစ်ဆေးမှုသည် ဖုန်းနံပါတ်တစ်ခုတည်းထက် ပိုကောင်းသော်လည်း Voucher Number ကို တခြားသူမြင်နိုင်/ရနိုင်ပါက အပြည့်အဝ identity verification မဟုတ်ပါ။ စစ်ဆေးမှုကြိုးစားမှုကို server မှ ကန့်သတ်ထားပြီး၊ အလွန်အရေးကြီးသော account အတွက် OTP သို့မဟုတ် login verification ပိုလုံခြုံသည်။
- VIP/Spend အတွက် အော်ဒါစုစုပေါင်းကို Cancelled မဟုတ်သော အော်ဒါများမှ တွက်သည်။
- Production တွင် တင်မီ test copy/staging site တွင် အရင်စမ်းသပ်ပါ။
