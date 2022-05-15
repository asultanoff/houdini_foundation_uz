# 1. Solar System (Part 0)

# Theory: solar system

## UI

Birinchi marta ochganda Houdini interfeysi qo'rqichli ko'rinishi mumkin. Lekin Houdini judayam oddiy va intuitiv UI ga ega. Programma o'rganishda odatda birinchi UI ni o'rgatishdan boshlanadi. Lekin Houdini programmasining mahsus ish jarayoni tabiyati va bizning o'qitish usuldan kelib chiqib, biz UI elementlari va ularni vazifalari haqida iloji boricha qisqacha to'xtalib o'tamiz. 

Houdinida eng asosiy oynalar quyidagilar:

![](D:\dev\Houdini\Houdini Foundation\Images\1_0.gif)

Houdinida birnichi 100-200 soat o'tqazadigan vaqtinigizning 95% da manashu 3 ta oynadan foydalanasiz. Bugungi dars va kurs davomida bu oynalardan tashqari yana bir qancha yangi oynalardan foydalanamiz va UI xaqida bosqichma bosqich ko'proq tushunchaga ega bo'lasiz.

Shu 3 ta oyna aslida bir-biriga judayam bo'gliq. Houdini 3d obyektlar bilan ishlaydi. Ushbu 3 ta oyna 3d obyektlar va ularga bog'liq bo'lgan ma'lumotlarni nafaqat ko'rsatib beradi, balki ularni o'zgartirishga xam imkon beradi. 

**Viewport** houdinidagi 3d obyektlarni 3 o'lchamda ko'ratib (render qilib) beradi. **Viewport**da nodalar **parameter**lariga o'zgartirish kiritsa ham bo'ladi

![](D:\dev\Houdini\Houdini Foundation\Images\1_1.gif)

Ikkinchi oyna, **Parameters** oynasi houdini obyektlari parameterlarni ushlab turadigan oyna xisoblanadi. Boya aytib o'tganimizdek, **Viewport** oynasida **parameter**larni o'zgartirish imkoniyati bor. Lekin ba'zi bir **parameter**lar viewportda ko'rinmaydi.

![](D:\dev\Houdini\Houdini Foundation\Images\1_3.gif)

Houdini obyektlari asosan nodalarda saqlanadi. **Network** usha nodalarni ushlab turadigan tarmoq xisoblanadi. Demak, **Network** 3d obyektlarni **noda** sifatida saqlasa, **Viewport** usha nodalarni 3 o'lchamli shaklini ko'rsatib beradi. 

![](D:\dev\Houdini\Houdini Foundation\Images\1_2.gif)



Ko'rib turganingizdek, ushbu 3 ta oyna Houdinidagi ma'lumotlarni turli qismlarini va xar xil formada sizga, ya'ni Houdini foydalanuvchilariga ko'rsatib beradi.

## Houdini obyektlari

Houdini yangi sessiyasini ochib, tepadagi shelf oynasidan **boxni** bosamiz. Kursorni viewportga qaytarib olib kelganda, kursorga qizil kub bog'langanini ko'ramiz. Viewportni pasida "Select position for Box. Hold shift to move off the construction plane". Bu podskaza, yoki **hint**. Houdini shelfdagi instrumentlariga shunaqa hint qoldirish imkoniyatini xam beradi. Kursorni viewportga qaytarib **Enter** knopkasini bosamiz. Ushanda Box 3d obyekt fazoni markazida xosil bo'ladi. 

![](D:\dev\Houdini\Houdini Foundation\Images\1_4.gif)

**Viewport** houdinidagi ma'lumotni 3 o'lchamda ko'rsatib beradi. Viewportda 3d space (3 o'lchamli fazo) da xarakatlanish uchun biz kamera manipulyatsiyalarini o'rganishimiz kerak. 

Kamerani o'zgartirish uchun, kamera rejimiga o'tishimiz kerak. Kamera rejimi knopkasi viewportni chap tomonidagi panelda, magnit knopkasi pasida turadi. Kamera rejimiga kirganimizda, kursor belgisi qo'l belgisiga aylanadi. Qarab turgan kameramizni quyidagicha o'zgartiramiz.

- Kamera rejimida "mishka"ni chap knopkasini bosib, kursorni qimirlatsak, qarab turgan kameramiz aylanadi. Buni houdini terminida **"Tumble"** deyiladi.
- "mishka"ni o'rta knopkasini bosib, kursorni qimirlatsak, qarab turgan kameramizni tepa/pas yoki chap/o'ngga yuradi. Buni houdini terminida **"Track"** deyiladi.
- "mishka"ni o'ng knopkasini bosib, kursorni qimirlatsak, qarab turgan kameramizni to'g'riga/orqaga yuradi. Buni houdini terminida **"Dolly"** deyiladi.

***

`Kamerani o'zgartirishni aytilmagan yana 2 yo'lini toping`

***

Xozircha kamera rejimga siz viewportni chap panelidagi kamera knopkasini bosib o'tishni bilasiz. Kamera rejimiga yana <ESC> knopkasi orqali o'tsa xam bo'ladi.

Kamera rejimiga o'tishning yana bir qisqa yo'li, <SPACE> yoki <ALT> knopkasini bosgan xolda, "mishka" orqali odatdagidek kamera **transform** ni o'zgartirsak bo'ladi. 

![](D:\dev\Houdini\Houdini Foundation\Images\1_5.gif)

Manashu yasab olgan kubimiz houdini obyekti xisoblanadi. Houdini obyektlari xar xil bo'lishi mumkin. Houdinida yasalgan effektlar, materiallar, modellar houdini nodalari orqali yasaladi. 

Nodalar network view oynasida ko'rinadi. Hozir network viewda box_object1 nodasini ko'rib turibmiz. Nodaning chap tomonida yashil, o'ng tomonida ko'k belgilari bor. Bu belgilar aslida knopka bo'lib, ularni bossa bo'ladi. 

***

* viewportdagi chap paneldan strelka belgisini yoqing
* viewportdagi kubni ustiga bosing. Kub chegaralari sariq rang bo'ldi. Networkdayam box_object1 nodasi chegaralari sariq rangga aylandi. Siz kub obyektini tanladingiz.
* box_object1 nodasini yashil knopkasini bosing. U knopka o'chib, yashil rang nodaning rangiga aylanishi kerak.
* agar kub tanlangan xolda bo'lsa viewportni bo'sh joyiga bosing
* viewportda kubni tanlab ko'ring
* nodaning o'ng tomonidagi ko'k knopka ni bosing. Viewportda noda yo'qoladi.

![](D:\dev\Houdini\Houdini Foundation\Images\1_6.gif)

***

Bu knopkalar kursorni nodaing ustiga olib kelganda radial menu shaklida xam paydo bo'ladi. Demak, nodalarni ustida ularni xususiyatini o'zgartiradigan knopkalar bor. 

Network view tepasida parameter oynasi bor. Parameter oynasi tanlangan nodaning parameterlarini ko'rsatadi. 

box_object1 nodasida 3ta gruppa parameterlar bor.

* Transform
* Render
* Misc

Transform guruhida Translate, Rotate, Scale va boshqa shunga o'xshagan paramterlarni ko'rib turibmiz. Bu paramterlarni turli xil yo'llar bilan o'zgartirishimiz mumkin. Quyidagi slaydda shu usullarni ko'ramiz. 

![](D:\dev\Houdini\Houdini Foundation\Images\1_7.gif)

Houdini obyektlarni biz xozirgacha faqat shelfdan yasashni bilamiz. Quyidagi slaydda Houdini obyektlarni yasashni yana 2 yo'lini ko'ramiz.

![](D:\dev\Houdini\Houdini Foundation\Images\1_8.gif)

## Transform va handle lar

Houdini obyektlarini fazodagi positsiyasi, o'qi atrofidagi aylangan burchagi, 3 ta o'q boyicha kattalik koefetsenti, uning o'qining pozitsiyasi xaqidagi ma'lumotlar 3 ta sonlar bilan belgilanadi. Misol uchun kubning pozitsiyasi {0, 0, 0} bo'lsa, u fazoning o'rtasida turgan bo'ladi. Agar uning pozitsiyasi {1, 0, 0} bo'lsa, u fazo markazidan **X** o'qi bo'yicha 1 metr uzoqlikda joylashgan bo'ladi. 

Obyektlarni fazodagi aytib o'tilgan parameterlari **Transform** deb ataladi. Obyektlarning transformi aslida matritsa bilan belgilanadi. Matritsalar bilan kurs davomida xali tanishib chiqamiz. Xozircha Transform deganda ushbu n ta narsani eslab qoling

* Houdini obyektlarini fazodagi positsiyasi ***(Position)***
* o'qi atrofidagi aylangan burchagi ***(Rotation)***
* 3 ta o'q boyicha kattalik koefetsenti ***(Scale)***
* uning o'qining pozitsiyasi xaqidagi ma'lumotlar ***(Pivot)***

Parameterda ko'rgan Transform parameterlari Houdini obyektlarini transformini o'zgartirish parameterlari xisoblanadi. 

* Translate obyektni fazodagi pozitsiyasini o'zgartiradi
* Rotate uni o'qlari bo'yicha aylantradi
* Scale uni o'qlari bo'yicha kattaligini o'zgartiradi
* Pivot Translate uni o'q pozitsiyasini o'zgartiradi
* Uniform Scale uni kattaligini xamma o'qlari bo'yicha proportsional o'zgartiradi

Obyekt transformini parameterlar yoki viewportdagi **handle** lar bilan o'zgartirsa bo'ladi. Parameter orqali transformlarni o'zgartirishni biz ko'rib chiqdik. 

Viewportni chap panelida strelka knopkasini 2 ta pasida Move, Rotate, Scale knopkalari joylashgan. Ular obyektlarni Translate, Rotate, Scale parameterlarini handle lari hisoblanadi. Ular quyidagicha ishlaydi.

 ![](D:\dev\Houdini\Houdini Foundation\Images\1_9.gif)

E'tibor bergan bo'lsangiz, Handle larni o'zgartirganizda, obyekt parameterlarida o'zgarish kiritiladi.

Har bitta handle ni o'zini sozlash menyusi bor. Agar handle aktivlashgan holda, handle o'rtasiga kursorni olib borib o'ng knopkani bosilsa, handle lar uchun bir qancha menyu elementlarini ko'rasiz. Ularni xammasi bizga kerak emas. Quyidagi slaydda ulardan asosiylari ko'rsatilgan. 

![](D:\dev\Houdini\Houdini Foundation\Images\1_10.gif)







