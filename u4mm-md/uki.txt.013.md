bqt4 - core libqt4 - gui

ၿပီးေနာက္ လက္ရွိ Skype version ၏ .deb package အား Skype website မွ download ျပဳလုပ္၍ 
	install ျပဳလုပ္ပါ။

    wget -O skype_ubuntu-current_amd64.deb http://www.skype.com/go/getskype-linux-beta-ubuntu-64
    sudo dpkg -i skype-ubuntu-current_amd64.deb
    sudo rm  skype-ubuntu-current_amd64.deb

အကယ္၍ 64-bit version သည္ သင့္အတြက္ အလုပ္မလုပ္ပါက 32-bit version အား အသံုးျပဳႏိုင္သည္။

    wget -O skype_ubuntu-current_i386.deb http://www.skype.com/go/getskype-linux-beta-ubuntu-32
    sudo dpkg -i --force -architecture  skype_ubuntu-current_i386.deb
    sudo rm  skype_ubuntu-current_i386.deb

###Installing Skype respository

Skype ၏ respository ထည့္သြင္းျခင္းအားျဖင့္လည္း Skype အား install လုပ္ႏုိင္ပါသည္။
ဤသို႔ျပဳလုပ္ျခင္းျဖင့္ auto update ျပဳလုပ္ေပးသည့္ အက်ဳိးေက်းဇူးရွိပါသည္။

-Resopsitory security key အား install လုပ္ရန္ (key server အတြက္ သင့္ firewall ၏ port 11371
	အား ဖြင့္ထားရန္လိုအပ္သည္။

    sudo apt - key adv -- keyserver pgp.mit.edu --recv -keys 0xd66b746e


###Skype repository,update ထည့္ျခင္းႏွင့္ Skype အား install ျပဳလုပ္ျခင္း။

    echo deb http://download.skype.com/linux/repos,debian/ stable non-free l   sudo tee - a
    sudo apt -get update
    sudo apt -get install skype

##Proprietary Extras

မူပိုင္ခြင့္အရ မွတ္ပံုတင္ထားေသာ ထပ္ေဆာင္း package မ်ား

ူမူပိုင္ခြင့္အရ မွတ္ပံုတင္ထားသည့္ software မ်ားသည္ အင္တာနက္ အသံုးျပဳရာတြင္ 
မ်ားစြာအေထာက္အကူျပဳပါလိမ့္မည္။ သို႔ေသာ္ လြတ္လပ္စြာ ရယူသံုးစြဲခြင့္မရွိပါ ။ Multimedia Codecs မ်ား၊
Java Runtime Environment ႏွင့္ Firefox အတြက္ plug-in မ်ားသည္ ထိုကဲ့သို႔ေသာ software မ်ားျဖစ္သည္။

#Restricted Extras

##ကန္႔သတ္ထားေသာ ထပ္ေဆာင္း package မ်ား

Ubuntu တြင္ ကန္႔သတ္ထားေသာ ထပ္ေဆာင္း package မ်ားကို ထည့္သြင္းလိုလွ်င္ command-line Terminal 
တြင္  command တစ္ခုတည္း ရိုက္ထည့္ရံုျဖင့္ လုပ္ေဆာင္ႏုိ္င္ပါသည္။ ထုိ package မ်ားတြင္ Adobe Flash 
Player, Jave Runtime Environment (JRE) (sun-java-jre) ႏွင့္ Firefox plug-in (icedtea) မ်ား ,
Microsoft မွ ထုတ္ေ၀ေသာ Font တခ်ဳိ႔ (msttcorefonts) ,multimedia codecs (w32codecs or
w64codecs), mp3 compatible encoding (lame), FFMpeg, extra Gstreamer codecs, DVD
decoding အတြက္ package မ်ား (libdvdread4,သို႔ေသာ္ အျခား decoder ျဖစ္သည့္ libdvdcss2 ကို
ရယူလိုပါက ဤေနရာတြင္ၾကည့္ပါ။) ,unrar archiver,odbc ႏွင့္ cabextract  မ်ားပါ၀င္သည္။ ထို႔အျပင္
အျခားေသာ အက်ဳိးအျမတ္ရယူသည့္ codecs မ်ားႏွင့္ avutils (libavcodec - unstripped - 52 ႏွင့္ libavutil-
unstripped - 49) မ်ားကိုလည္း ထည့္သြင္းေပးမည္ျဖစ္သည္။

    sudo apt-get install ubuntu-restricted-extras  

မွတ္ခ်က္ : ထည့္သြင္းျခင္း လုပ္ငန္းစဥ္အတြက္ command-line Terminal တြင္ လုပ္ေဆာင္ခ်က္မ်ား
ၿပီးဆံုးမွသာ ျပည့္စံု၍ အလုပ္လုပ္ေဆာင္ႏုိင္မည္ျဖစ္သည္။  ယခုေဖာ္ျပထားေသာ package အားလံုးကို Package
Manager အသံုးျပဳ၍ ထည့္သြင္းပါက ျပည့္စံုမည္မဟုတ္ပါ။

#Photos and Graphics

သင္၏ဓာတ္ပံုမ်ားကို ျပင္ဆင္ထိန္းသိမ္းျခင္း၊ ရင္သပ္ရႈေမာဖြယ္ 3D ပံုမ်ားႏွင့္ ဂရပ္ဖစ္မ်ားကို ဖန္တီးျခင္္း
သို႔မဟုတ္ Format ဖိုင္အမ်ဳိးအစား ေျပာင္းလဲျခင္းမ်ား ျပဳလုပ္ရန္။

##GIMP (Image Manipulator)

[Gimp](http://www.gimp.org/) သည္ အစြမ္းထက္ေသာ စြမ္းရည္ျပည့္၀သည့္ free open-source ျဖစ္ပါသည္။
ဂရစ္ဖစ္မ်ားႏွင့္ ဓာတ္ပံုမ်ားျပင္ဆင္သည့္ Adobe Photoshop ႏွင့္  ဆင္တူေသာ ေဆာ့ဖ္၀ဲျဖစ္ပါသည္။

    sudo apt - get install gimp

###GIMP အတြက္ သီးသန္႔ brushe မ်ား palette မ်ားႏွင့္ gradiend မ်ားရိွပါသည္။

    sudo apt-get install gimp-data-extras
 

##Dia (Diagram editor)
 
[Dia](http://live.gnome.org/Dia) သည္ Gnome အတြက္ ျပဳလုပ္ထားသည့္ GTK အေျခခံ diagram
ဖန္တီးသည့္ open source ပရိုဂရမ္ျဖစ္ပါသည္။ Visio ႏွင့္  ဆင္တူပါသည္။

sudo apt - get install dia


##Kivio (Diagram editor)

[Kivio](http://www.koffice.org/kivio/) သည္ flow-chat မ်ားႏွင့္ diagram မ်ားကို ဖန္တီးသည့္  open
source ပရိုဂရမ္ျဖစ္ၿပီး KDE အတြက္ ျပဳလုပ္ထားသည့္ KOffice Suite တြင္ ပါ၀င္ပါသည္။ Dia ဖေယာင္းမိတၱဴမ်ား ျပဳလုပ္၍ ရပါသည္။

    sudo apt - get install kivio


##Inkscape  Vector Illustrator

[Inkscape Vector Illustrator](http://www.inkscape.org/) သည္ Illustrator ၊CorelDraw စသည္တုိ႔ႏွင့္ 
တူညီသည့္ open source  ပံုဆြဲပရိုဂရမ္ျဖစ္ပါသည္။

    sudo apt-get install inkscape


##Digikam (Photo Organiser)

[Digikam](http://www.digikam.org) သည္ ဒစ္ဂ်စ္တယ္ ဓာတ္ပံုမ်ားကို ျပင္ဆင္ စုစည္းသိမ္းဆည္းဖို႔
အလြန္အဆင္ေျပေသာ open source ျဖစ္ပါသည္။ install လုပ္လိုလွ်င္

    sudo apt-get install digikam kipi-plugins digikam-doc


#F -spot (Photo Organiser)

[F -spot](http://htpp://f-spot.org/) သည္ ဒစ္ဂ်စ္တယ္ဓာတ္ပံုမ်ားကို ျပင္ဆင္စုစည္းသိမ္းဆည္းဖို႔
အလြန္အဆင္ေျပေသာ Gnome Desktop အတြက္ ျပဳလုပ္ထားသည့္ open source ျဖစ္သည္။ install
လုပ္လိုပါက:

    sudo apt-get install f-spot


##Google Picasa (Photo Organiser)


[Google Picasa](http://picasa.google.com.mm/linux/) သည္ Digikam ကဲ့သို႔ ပင္
ဓာတ္ပံုျပင္ဆင္သိမ္းဆည္းရန္ျဖစ္ပါသည္။ အြန္လိုင္းအသံုးျပဳထားပါက Google web server သုိ႔ 
တိုက္ရိုက္ပံုမ်ားကို upload လုပ္ႏုိင္ပါသည္။ အေသးစိ္တ္သိလိုပါက Picasa for Linux FAQ
(http://picasa.google.com/linux/faq.html) တြင္ ၾကည့္ပါ ။ Picasa 2.7 Download
(http://picasa.google.com/linux/download.html#picasa27) ေနရာတြင္ ကုိယ္တိုင္ install လုပ္ႏုိင္သည့္
.deb ဖိုင္ရရွိႏိုင္ပါသည္။

##Shotwell (Photo Organiser)

[Shotwell](http://www.yorba.org/shotwell/) အလြယ္တကူ ၾကည့္ရႈ ထိန္းခ်ဳပ္ႏိုင္မည့္
ေဆာ့၀ဲတစ္ခုျဖစ္ပါသည္။  ဤေနရာ (http://www.youba.org/shotwell/install/) တြင္ အေသးစိတ္
ၾကည\E1\80
