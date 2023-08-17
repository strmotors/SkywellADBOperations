# Skywell ADB İşlemleri Kılavuzu

```
███████╗████████╗   ██████╗ 
██╔════╝╚══██╔══╝   ██╔══██╗
███████╗   ██║█████╗██████╔╝
╚════██║   ██║╚════╝██╔══██╗
███████║   ██║      ██║  ██║
╚══════╝   ╚═╝      ╚═╝  ╚═╝
```
Skywell ADB İşlemleri Kılavuzuna hoş geldiniz! Bu kılavuz, Skywell ET5 aracınızdaki ADB (Android Hata Ayıklama Köprüsü) işlemlerini adım adım yönetme talimatları sunar.

## Giriş

ADB kullanarak Skywell ET5 aracınızdaki uygulama yüklemelerini ve kaldırmalarını verimli bir şekilde yönetebilirsiniz. Aracınızdaki multimedya sistemi Android işletim sistemine dayanmaktadır ve her Android cihaz hata ayıklama amacıyla bir ADB arabirimi içerir. Bu teknolojiyi kullanarak aracınızın sistemine bağlanabilir, yeni uygulamaları yükleyebilir ve mevcut olanları kaldırabilirsiniz.

### Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Kişisel bir hotspot oluşturabilen bir cihaz (örneğin, cep telefonunuz).
- Windows işletim sistemli bir bilgisayar.

### İndirmeler

Gerekli dosyaları indirin:

- [Skywell Klasörü](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing)

**Önemli Not:** Bu adımları izlemek cihazınıza zarar vermez veya garantisini geçersiz kılmaz. Tüm işlemler geri alınabilir. Garanti sorunlarından kaçınmak için aracınızı yetkili servise götürmeden önce eklediğiniz uygulamaları kaldırmanız önerilir. Yardım için bize **strmotorstr@gmail.com** adresinden ulaşabilirsiniz.

## Yükleme Adımları

### Adım 1: Gerekli Dosyaları Hazırlama

1. [Buradan](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing) gerekli dosyaları indirin ve indirilen arşivden "Skywell" klasörünü çıkarın.
2. Çıkarılan "Skywell" klasörünü masaüstünüze taşıyın.
3. Yüklemek istediğiniz .apk dosyalarını "Skywell" klasörüne yerleştirin.

### Adım 2: Araç Wi-Fi Ağına Bağlanma

1. Cep telefonunuzda kişisel bir hotspot oluşturun ve aracınızı ve bilgisayarınızı bu ağa bağlayın.
2. Aracın ayarlarında, "Bluetooth Calling" bölümüne gidin ve "wifi adb opened" mesajı görünene kadar "Bluetooth Calling" yazan yere tekrar tekrar dokunun.
3. Aracın IP adresini araç ayarları menüsündeki Wi-Fi ayarlarına erişerek bulun. Bağlı olduğunuz Wi-Fi ağına tıkladığınız zaman, arabanın IP adresini görebilirsiniz.

### Adım 3: ADB Bağlantısı Kurma

1. "Windows Tuşu + R" tuşlarına basarak "Çalıştır" penceresini açın, ardından `cmd` yazın ve "Tamam" tuşuna basın.
2. Komut İstemi'nde aşağıdaki komutları girin:
```
cd Desktop\Skywell
adb connect <Araç IP Adresi>
adb install ./<APK Dosya İsmi>.apk
```
`<Araç IP Adresi>`'ni, aracın ayarlarından elde ettiğiniz gerçek IP adresiyle değiştirin.

### Adım 4: Yükleme Doğrulama

1. Yükleme işleminden sonra aracınızdaki uygulama merkezini açın.
2. Yeni yüklenen uygulamayı göremiyorsanız, uygulama merkezini, sol üstteki çarpı ikonuna basarak kapatın ve tekrar açın.

## Kaldırma Adımları

### Adım 1: Kaldırma İçin Hazırlık Yapma

1. "Skywell" klasörünün hâlâ masaüstünüzde olduğundan emin olun.
2. Hem aracın hem de bilgisayarın aynı Wi-Fi ağına bağlı olduğundan emin olun.

### Adım 2: ADB Bağlantısı Kurma ve Erişim Sağlama

1. Tekrar `Windows Tuşu + R` tuşlarına basarak "Çalıştır" penceresini açın ve `cmd` yazarak "Tamam" tuşuna basın.
2. Komut İstemi'nde aşağıdaki komutları girin:
```
cd Desktop\Skywell
adb disconnect
adb connect <Araç IP Adresi>
adb shell am start -a android.settings.SETTINGS
```
`<Araç IP Adresi>`'ni, aracın IP adresiyle değiştirin.

3. Bu, tabletteki gizli "Ayarlar" menüsünü açacaktır. Bu menüden, herhangi bir Android cihazdaki gibi, istediğiniz uygulamayı kaldırabilirsiniz.

## Yazar Hakkında

Bu kılavuz, *ST-R Motors* tarafından hazırlanmıştır. Umarız bu kılavuz Skywell ET5 aracınızdaki ADB işlemlerini basitleştirir. Yardım için her zaman **strmotorstr@gmail.com** adresinden bize ulaşabilirsiniz.

Skywell ET5 aracınızla keyifli sürüşler!
