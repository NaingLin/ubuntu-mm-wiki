#Password chceker and enforcement#

###[John the Ripper](http://www.openwall.com/john/) Password စစ္ေဆးမႈႏွင့္ အတည္ျပဳမႈ###

John the Ripper သည္ Dictionary ၏ password မ်ားအား ဖ်က္ရန္အတြက္ အခမဲ့အသံုးျပဳႏိုင္ေသာ open source ျဖစ္ၿပီး ေယဘုယ်အားျဖင့္ ၄သန္းခန္႔ ဘာသာေပါင္းစံုျဖင့္ အသံုးျပဳေနၾကသည္။ အဘယ္ေၾကာင့္ဆိုေသာ္
ဤ program သည္ က်ယ္က်ယ္ျပန္႔ျပန္႔ႏွင့္ လြယ္လင့္တကူ ရႏိုင္ေသာေၾကာင့္ ျဖစ္ၿပီး  မိမိ၏ ကြန္ျပဴတာ ႏွင့္ LAN ၏  password မ်ားအား  စစ္ေဆးျခင္း၊ လံုျခံဳေအာင္ ျပဳလုပ္ျခင္းမ်ားအတြက္လည္း ၏
အသံုး၀င္ေသာေၾကာင့္ျဖစ္သည္။ Install ျပဳလုပ္ရန္

	sudo apt - get install john

[Passwdqc](http://www.openwall.com/passwdqc/) သည္ password မ်ား၏ ၾကံ့ခိုင္မႈအားအတည္ျပဳေပးရန္အတြက္ သံုးေသာ module တစ္ခုျဖစ္သည္။ Install ျပဳလုပ္ရန္

	sudo apt - get install passwdqc


#MD5Sum#

File တစ္ခု၏ MD5 sum မ်ားအား စစ္ေဆးရန္အတြက္ သံုးေသာ command line တစ္ခုျဖစ္သည္။

	md5sum filename

မွတ္ခ်က္။  ။ Filenames with spaces

###Spaces ခံ၍ အမည္ေပးထားေသာ File မ်ား###

-`Spaces` ခံ၍ ရိုက္ႏွိပ္ထားေသာ File ႏွင့္ Folder အမည္မ်ားအား မ်က္ေတာင္ အဖြင့္ အပိတ္မ်ား `( )` မ်ား ထည့္အသံုးျပဳသင့္သည္။ ဥပမာအားျဖင့္ This Dir အမည္ေပးထားေသာ directory တစ္ခု သို႔မဟုတ္
	`/home/This Dir` အမည္ရွိ directory တစ္ခုအား ေျပာင္းလဲခ်င္ပါက ေအာက္ပါ command 
	အား အသံုးျပဳရမည္။

	cd This Dir

သုိ႔မဟုတ္

	cd/home/This Dir

-တစ္နည္းအားျဖင့္ `backslash (/)` ကို space ေနရာမွာ အစားထုိးျခင္းျဖင့္လည္း အသံုးျပဳႏုိင္ပါသည္။

This Dir အမည္ေပးထားေသာ directory တစ္ခု သို႔မဟုတ္ `/home/This Dir` အမည္ရွိ directory တစ္ခုအား ေျပာင္းလဲခ်င္ပါက 

	cd This /Dir 

သို႔မဟုတ္

	cd/home/This /Dir


#Alien#

[Alien](http://kitenet.net/~joey/code/alien/) သည္ (Red Hat) .rpm packages မ်ားကို  (Debian).deb packages မ်ားအျဖစ္သို႔ ေျပာင္းလဲေပးေသာ ဖိုင္ေျပာင္းနည္းတစ္ခုျဖစ္သည္။ ဒီနည္းဟာ စိတ္ခ်ရတဲ့နည္းမဟုတ္သလို ေျပာင္းလိုက္တဲ့ package ေတြရဲ႕ function ေတြကို ေသခ်ာျပန္စစ္ေဆးေပးဖို႔လိုအပ္ပါတယ္။ မ်ားေသာအားျဖင့္ စာေၾကာင္းေတြ ျပန္ေျပာင္းေပးဖို႔ လိုအပ္ပါတယ္။ Source ကေန `(Debian).deb package` ကို ေျပာင္းေပးျခင္းက ပိုၿပီးစိတ္ခ်ရပါတယ္။ Alien software ရဲ႕ maintainer ေတြ ကို္ယ္တိုင္ကိုက important package ေတြကို ဖိုင္ေျပာင္းတဲ့အခါ Alien ကို အသံုးမျပဳေစခ်င္ၾကပါဘူး။ Alien ကို version နံပါတ္ေတြ ေျပာင္းတာကေန ထိန္းထားခ်င္တယ္ဆိုရင္ေတာ့ ေဖာ္ျပပါ command ကို ရိုက္ထည့္ေပးပါ။

	alien - k rpm _file _name.rpm

.rpm ကို .deb အျဖစ္ေျပာင္းနည္း

	alien - d package - name .rpm

.rpm ကို .deb အျဖစ္ေျပာင္းၿပီး ရလာတဲ့ file ကို တစ္ခါတည္း install လုပ္ရန္

	alien - i package - name .rpm

.rpm ကို Debian အျဖစ္ေျပာင္းရန္

	sudo alien - k  .rpm
	

#Software Troubleshooting#

####Program အစတြင္ လုပ္ပိုင္ခြင့္ Error တက္ျခင္း##

အကယ္၍  သင့္တြင္ လုပ္ပိုင္ခြင့္ Error တစ္ခုတက္လာပါက ေဖာ္ျပပါအတိုင္း လုပ္ေဆာင္ပါ။

	sudo chown - R user /home/user

မွတ္ခ်က္ ။    user ဆိုေသာ ေနရာတြင္ သင့္ username အမွန္အား ထည့္ေပးပါ။ ဤ command သည္ folder ၏ ပိုင္ရွင္အား ေျပာင္းလဲေပးမည္ျဖစ္သည္။ `-R` အပါအ၀င္  (recursively ) ကိုဆိုလိုၿပီး folder အခြဲမ်ားပါ ပါ၀င္ပါသည္။


##CD - ROM Troubleshooting##

###CD - ROM Error အားေျဖရွင္းျခင္း###

အကယ္၍ သင္ CD burner အသံုးျပဳၿပီး  burn ေန႔စဥ္အတြင္းမွာ `cdrecord has no permission to open the device` ဆိုတဲ႔ Error တက္လာပါက terminal ကို ဖြင့္ၿပီး

	sudo chmod 777 /dev /scd0

လို႔ ရိုက္လိုက္ပါ။

မွတ္ခ်က္။ `/dev/scd0` ေနရာတြင္ သင့္ device အားထည့္ေပးပါ။
မွတ္ခ်က္။ `chmod 777` သည္ folder အား လုပ္ပိုင္ခြင့္အျပည့္အစံုေပးလိုက္သည့္ universal option ျဖစ္သည္။ `777` ဆုိေသာ ဂဏန္းသည္ ေရးျခင္း၊ ဖတ္ျခင္း ၊လုပ္ေဆာင္ျခင္း စသည့္ လုပ္ပိုင္ခြင့္ တု႔ိကို အသံုးျပဳသူအား အျပည့္အ၀ ေပးလိုက္သည္ဟု အဓိပၸါယ္ ရသည္။

