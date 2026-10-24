# Canvas Beta

Canvas'ın Windows beta kurulumları ve sürüm notları. Bu depo kurulum dosyalarını dağıtır; kaynak kodu içermez. İndirmeler herkese açıktır.

**Gereksinim:** Windows 11 24H2 veya sonrası, x64.

## Güncelleme politikası

Paket sürümü `0.1.8.0`, uygulama sürümü `0.1.8-beta.1`'dir. Store'a geçene kadar beta güncellemeleri elle yapılır. `0.1.6.0` ve `0.1.7.0` içindeki eski uygulama içi açılış güncellemesi testinde, çalışan Canvas paketi nedeniyle `0x80073D02` hatası görüldü. Bu sürümlerden geçerken de aşağıdaki elle güncelleme yolunu kullanın.

Uygulama içi denetim, indirme/yükleme ve yeniden başlatma akışı kaldırıldı. Canvas güncelleme beklemeden normal açılır; ayarlarda yalnız yüklü sürüm ve sürüm geçmişi bulunur. Windows'un beta için açılış ve arka plan denetimleri aşağıdaki yardımcıyla kapalı tutulur. İlerideki Store paketi kendi Microsoft Store kanalından güncellenir.

Çalışmalarınızı kaydedip tüm Canvas Beta pencerelerini kapatın; aşağıdaki `.appinstaller` dosyasını yeniden indirip açın ve **Güncelle** seçin. Uygulamayı kaldırmayın veya sertifika güven ayarlarını değiştirmeyin. Ardından manuel güncelleme ayarını doğrulayın.

## 0.1.5.0'dan ilk geçiş

`0.1.5.0`, uygulama içi açılış güncelleyicisini içermez. Çalışmalarınızı kaydedip Canvas Beta'yı kapatın; aşağıdaki `.appinstaller` dosyasını indirip açın ve **Güncelle** seçin. Uygulamayı kaldırmayın. Sonrasında aşağıdaki manuel ayar doğrulamasını tamamlayın.

## Kurulum / 0.1.1.0'dan güncelleme

**[Canvas-Beta.appinstaller indir](https://github.com/kbingol/canvas-release/releases/download/beta-feed/Canvas-Beta.appinstaller)**

Dosyayı indirip açın; Windows'un kurulum penceresinde **Yükle** veya **Güncelle** seçin. Mevcut `0.1.1.0` kurulumunu kaldırmayın. Sertifikası zaten güvenilir olan kullanıcıların yeniden sertifika yüklemesi gerekmez. Kurulumdan sonra aşağıdaki manuel ayar doğrulamasını tamamlayın.

İlk kez kuruyorsanız önce [Canvas-Beta.cer](https://github.com/kbingol/canvas-release/releases/download/v0.1.8-beta.1/Canvas-Beta.cer) sertifikasını indirin. Parmak izi:

```text
5BE262C15AEEEF8771888BFEE1AF99CD35F3344F
```

Sertifikayı açıp **Sertifika Yükle → Yerel Makine → Tüm sertifikaları aşağıdaki depolama alanına yerleştir → Gözat → Güvenilen Kişiler → Tamam → İleri → Son** yolunu izleyin. Yönetici onayı gerekir. Bu test sertifikasına güvenme işlemi her bilgisayarda bir kez yapılır. Geçerli Kullanıcı veya Güvenilen Kök Sertifika Yetkilileri deposunu seçmeyin. Ardından yukarıdaki `.appinstaller` dosyasını açın.

## Sonraki güncellemeler

Yeni sürüm duyurulduğunda çalışmalarınızı kaydedip tüm Canvas Beta pencerelerini kapatın. Yukarıdaki aynı `.appinstaller` bağlantısını yeniden indirip açın ve **Güncelle** seçin. Güncellemeden sonra manuel ayar doğrulamasını tamamlayıp **Ayarlar → Update** içinde duyurulan sürümü kontrol edin. Uygulama güncelleme başlatmaz veya kendini güncelleme için yeniden açmaz; beta'da otomatik denetim beklenmez.

Her sürümde aynı sertifikayı yeniden yüklemeniz gerekmez. Yeni feed boş `<UpdateSettings />` içerir; `OnLaunch` ve `AutomaticBackgroundTask` eklenmez. Ancak eski Windows kayıtlarının otomatik tercihleri ayrıca kapatılmalıdır; yalnız feed'in değişmesi mevcut ayarın temizlendiğinin kanıtı değildir.

## Manuel ayarı doğrulama

[Set-CanvasBetaManualUpdates.ps1 dosyasını indirin](https://github.com/kbingol/canvas-release/releases/download/v0.1.8-beta.1/Set-CanvasBetaManualUpdates.ps1). Bu bir PowerShell betiğidir; dosya adının `.ps1` ile bittiğini kontrol edin ve içeriğini inceleyin. Windows dosyayı engellediyse **Özellikler → Engellemeyi kaldır** seçeneğini kullanın. Canvas'ın kurulu olduğu Windows hesabında, normal Windows PowerShell penceresini dosyanın klasöründe açıp çalıştırın:

```powershell
.\Set-CanvasBetaManualUpdates.ps1
```

Bu yardımcı yalnız geçerli kullanıcının `Canvas.Beta` / `CN=Canvas Beta` kaydında açılış ve arka plan denetimini kapatır; `CheckOnLaunch=false` ve `EnableAutomaticBackgroundTask=false` değerlerini geri okuyarak doğrular. `-WhatIf` ile ayar değiştirmeden önizleme yapılabilir. Mevcut beta kullanıcıları geçişte, `.appinstaller` kullananlar sonraki kurulum/güncellemelerden sonra da bu doğrulamayı yapar. Betiğin hata verdiği veya kayıt bulamadığı durumda bunu başarılı ayar değişikliği olarak kabul etmeyin. Kuruluşunuz betik çalıştırmayı engelliyorsa yöneticinize danışın; yürütme ilkesini değiştirmeyin. Bir bilgisayardaki değişiklik diğer test kullanıcılarına uygulanmaz; Store'un veya Windows'un genel güncelleme ayarlarına dokunulmaz.

Doğrudan imzalı `.msix` ile elle güncelleme de mümkündür. [Bu sürümün dosyalarındaki](https://github.com/kbingol/canvas-release/releases/tag/v0.1.8-beta.1) `Install-CanvasBeta.ps1`, aynı klasördeki MSIX ve sertifikayı doğrulayıp kurar, ardından yanındaki manuel politika yardımcısını çalıştırır. Doğrudan `.msix` kurulumu tek başına önceden kaydedilmiş otomatik tercihleri temizlediği anlamına gelmez. Dosyalar tek tek indirilebilir; ZIP indirmek gerekmez.

**[Tüm sürümler ve sürüm notları](https://github.com/kbingol/canvas-release/releases)** · **[Ayrıntılı kurulum kılavuzu](https://github.com/kbingol/canvas-release/releases/download/v0.1.8-beta.1/README.md)**

Eski `0.1.0.0` farklı paket kimliği kullanır ve yerinde güncellenmez. Projeleri `.flow` olarak dışa aktarıp yeni beta'da açın; kişisel asistanlarınızı yedekleyin. Kaldırma paket verilerini silebilir.

Microsoft belgeleri: [test sertifikasıyla dağıtım](https://learn.microsoft.com/en-us/windows/msix/package/sign-msix-package-guide#testing-distribute-to-testers-with-a-self-signed-certificate), [sertifika deposu](https://learn.microsoft.com/en-us/windows/msix/app-installer/troubleshoot-appinstaller-issues#trusted-certificates), [otomatik güncelleme davranışı](https://learn.microsoft.com/en-us/windows/msix/app-installer/auto-update-and-repair--overview), [güncelleme seçenekleri](https://learn.microsoft.com/en-us/windows/msix/app-installer/update-settings).
