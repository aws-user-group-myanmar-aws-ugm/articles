# Elastic Compute Cloud (or) EC2 - Episode (1)

![](https://i.imgur.com/dRgLosS.jpg "Elastic Compute Cloud")

ဒီေန့မွာေတာ့ AWS မွာရွိတဲ့ Service ေတြထဲကမွ တစ္ခုအပါအဝင္ျဖစ္ျပီး လူသံုးအမ်ားဆံုး Core Service တစ္ခုလည္းျဖစ္တဲ့ EC2 (Elastic Compute Cloud) Instance အေျကာင္းကိုေျပာျပေပးသြားမွာျဖစ္ပါတယ္။ ဆိုေတာ့ကာ ကြ်န္ေတာ္တို့ျကားဖူးေနတဲ့ AWS က EC2 Instance ဆိုတာဘယ္လို Service လဲဆိုရင္ေတာ့ျဖင့္ အနီးစပ္ဆံုးေျပာရင္ Virtual Private Server ( VPS ) ေတြလိုပါပဲ။ EC2 ကအဓိကအားျဖင့္ Cloud Compute ပိုင္းကိုလုပ္ေဆာင္ပါတယ္။ Compute ဆိုတဲ့ထဲမွာအမ်ားျကီးပါဝင္ပါတယ္။ လြယ္လြယ္ေျပာရရင္ ကြ်န္ေတာ္တို့သံုးခ်င္တဲ့ Web Server, Application Server, Database Server စတာေတြအတြက္ Cloud ေပါ္မွာတင္ျပီးအသံုးျပုလို့ရနိုင္ေအာင္လုပ္ေပးတယ္ေပါ့ဗ်ာ။ EC2 Instance ေတြဟာ ေသခ်ာမြန္းမံထားတဲ့ Xen Virtualization ေပါ္မွာအေျခခံထားတာျဖစ္ျပီး 2017 ေနာက္ပိုင္း Instance Class တစ္ခ်ို့ကိုေတာ့ KVM Based Virtualization ( [Nitro](http://www.brendangregg.com/blog/2017-11-29/aws-ec2-virtualization-2017.html) ) ေပါ္မွာအေျခခံထားတာျဖစ္ပါတယ္။ EC2 ( Elastic Compute Cloud ) ေပါ္မွာ Linux Distro ေတာ္ေတာ္မ်ားမ်ား၊ BSD ၊ Windows Operaing System စတာေတြ Run လို့ရပါတယ္။On-Premise မွာ ကိုယ္တိုင္ OS Install/Setup လုပ္ရမဲ့ အခ်ိန္ေတြကို Cloud ေပါ္မွာဆိုရင္ေတာ့ မိနစ္ပိုင္းအတြင္းျပီးမွာျဖစ္တဲ့ အတြက္အခ်ိန္ကုန္သက္သာေစျပီး Future Plan အတြက္ Scaling ( Horizontal/Vertical ) ျပုလုပ္ရာမွာလည္းအလြယ္တကူျပုလုပ္နိုင္မွာျဖစ္ပါတယ္။ 

**Amazon EC2 ( Elastic Compute Cloud )** တြင္ Virtual Server အျပင္ ၎မွ Supporting ေပးထားေသာ Features မ်ားကိုမိတ္ဆက္ေပးပါရေစ။

#### Basics

 - Instances and AMIs

 - Regions and Availability Zones

 - Instance Types

 - Tags


#### Networking and Security

 - Amazon EC2 Key Pairs

 - Security Groups

 - Elastic IP Addresses

 - Amazon EC2 and Amazon VPC

#### Storage

 - Amazon EBS

 - Instance Store


# Guide


* အရင္ဆံုး Naming အေနနဲ့ AWS မွာ EC2 ကို ***Instance*** လို့လည္းေခါ္ျကပါတယ္။
* Resources မ်ားအတြက္ Multiple Physical Locations ေခါ္  ***Regions, Availability Zones ( AZs )***
* CPU, Memory, Storage, Networking Capacity ဘယ္ေလာက္သံုးမယ္ကိုေရြးခ်ယ္နိုင္မယ့္ ***Instance Types***
* Instance အတြင္း Additional Software မ်ားကိုအခ်ိန္တိုအတြင္းေရြးခ်ယ္ျပီး Install/Setup လုပ္နိုင္ေသာ Preconfigure Template ေခါ္ ***AMIs ( Amazon Machine Images )*** 
* Instance မ်ားကို လံုျခုစြာ Remote Login ျပုလုပ္နိုင္ရန္အတြက္  ***Key Pair ( Public/Private Key )***
* Instance ကို Stop or Terminate လုပ္ရင္ပ်က္သြားမဲ့ Temporary Storage Volume အတြက္ ***Instance Store Volumes*** 
* Persistent/Permanent Storage Data Volume အတြက္ ***Amazon Elastic Block Storages ( Amazon EBS Volumes )***
* Instances မ်ားအတြက္  ***Security Groups***   ေခါ္ Firewall ( Specify the protocols, ports, and source IP range ) 
* ***Elastic IP*** Addresses ေခါ္ Instance မ်ားအတြက္ Static Public IPv4 Addresses
* EC2 Instances မ်ားအတြက္လိုအပ္ေသာ Virtual Network မ်ားကို AWS Cloud အတြင္း Logically Isolated ျဖစ္ရန္အတြက္သတ္မွတ္နိုင္ေသာ ***Amazon Virtual Private Clouds ( Amazon VPCs)***
* AWS အတြင္းရွိ Instances, Amazon Machine Images ( AMI ) နွင့္ အျခားေသာ Resources မ်ားကို Manage လုပ္ရလြယ္ကူေစရန္အတြက္ ***Tags***


   သည္ေလာက္ဆိုရင္ေတာ့ **Amazon EC2** ရဲ့ အေျခခံ Concepts နဲ့ သူရဲ့နာမည္အေခါ္အေဝါ္ေလးေတြကို အျကမ္းဖ်င္းသေဘာေပါက္လိမ့္မယ္ထင္ပါတယ္။ Episode (1) ပဲရွိေသးတဲ့အတြက္ေနာက္ထပ္ Episodes ေတြမွာ Feature တစ္ခုခ်င္းစီရဲ့ Use Case နဲ့ Details ေလးေတြေရးသားသြားဦးမွာမို့ ဆက္လက္အားေပးျကပါဦး ခင္ဗ်ာ။
   
   [Wai Yan Min](https://www.facebook.com/waiyanminthesuperman "Profile")
   [AWS User Group Myanmar](https://www.facebook.com/awsugm/ "Facebook Group") 
