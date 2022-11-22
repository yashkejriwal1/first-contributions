کمانڈر ترمیم #

اگر آپ اپنے دور دراز ذخیرہ میں تبدیلی کرتے ہیں تو صرف اس کے بعد احساس کرنے کے لۓ آپ کے پاس وعدہ کردہ پیغام میں ٹائپو ہے یا آپ کو اپنے حالیہ حاکموں میں ایک لائن شامل کرنا بھول گیا ہے.
تم اس میں کیسے ترمیم کرتے ہو؟ یہ وہی ہے جو سبق کا احاطہ کرتا ہے.

## آپ Github کے لئے دھکیل دیا ہے کے بعد ایک حالیہ پیغام کا ارتکاب تبدیل کرنا.

کسی فائل کو کھولنے کے بغیر ایسا کرنے کے لئے:
* میں ٹائپ کریں `` `git commit --amend -m "اپنا نیا ارتکاب کے بعد پیغام "` `` ارتکاب
* ذخیرہ کرنے کے لئے تبدیل کرنے کے لئے چلائیں `` `git push origin <branch-name>` ``.

نوٹ: اگر آپ صرف ``` git commit --amend ``` میں ٹائپ کریں تو، آپ کے ٹیکسٹ ایڈیٹر آپ کو وعدہ پیغام میں ترمیم کرنے کے لئے فوری طور پر کھولیں گے.
`` -m`` جھگڑے کو شامل کرنے سے روکتا ہے.

## ایک واحد پر ترمیم کا ارتکاب

لہذا، اگر ہم ایک ہی لفظ کو تبدیل کرنے کی طرح ایک فائل میں ایک معمولی تبدیلی کرنے کے لئے بھول گئے ہیں اور ہم نے پہلے سے ہی ہمارے دور دراز ذخیرہ کرنے کے لئے وعدے کو دھکا دیا ہے؟

یہاں وضاحت کرنے کے لئے میری اقلیت کی لاگت ہے:

`` `
g56123f create file bot file
a2235d updated contributor.md
a5da0d modified bot file
`` `
آتے ہیں کہ میں بوٹ فائل میں ایک ہی لفظ شامل کرنے کے لئے بھول گیا

اس کے بارے میں جانے کے لۓ 2 طریقے ہیں. سب سے پہلے ایک مکمل طور پر نیا وعدہ ہے جو اس طرح کی تبدیلی پر مشتمل ہے:

`` `
g56123f create file botfile
a2235d updated contributor.md
a5da0d modified botfile
b0ca8f added single word to botfile
`` `
دوسرا طریقہ 5da0d وعدہ میں ترمیم کرنا ہے، اس نئے لفظ کو شامل کریں اور یہ ایک عہد کے طور پر جتھوٹ کو دھکا دیں.
دوسری آواز بہتر ہے کیونکہ یہ صرف ایک معمولی تبدیلی ہے.

اس کو حاصل کرنے کے لئے، ہم مندرجہ ذیل کریں گے:
* فائل میں ترمیم کریں. اس صورت میں، میں نے پہلے ہی اتار دیا گیا لفظ شامل کرنے کے لئے میں botfile میں ترمیم کریں گے.
* اگلا، فیلڈ اسٹینج علاقے میں `` `git add <filename>` ``

عام طور پر اسٹینجنگ علاقے میں فائلوں کو شامل کرنے کے بعد، ہمارا اگلا کام ہمارا وعدہ ہے - ہمارا وعدہ پیغام "صحیح ہے؟
لیکن چونکہ ہم یہاں حاصل کرنا چاہتے ہیں اس سے پچھلے وعدوں میں ترمیم کرنا ہے، ہم اس کے بجائے چلائیں گے:

* `` `git commit --amend ` ``
 اس کے بعد ٹیکسٹ ایڈیٹر کو لانے اور پیغام کو ترمیم کرنے کے لئے آپ کو فوری طور پر کریں گے. آپ پیغام کو چھوڑنے کا فیصلہ کر سکتے ہیں کیونکہ اس سے پہلے تھا یا اسے تبدیل کر دیا گیا تھا.
* ایڈیٹر سے باہر نکلیں
* اپنی تبدیلیوں کو دھکا دیں `` `git push origin <branch-name>` ``

اس طرح، دونوں تبدیلیاں ایک ہی انجام میں ہو گی.