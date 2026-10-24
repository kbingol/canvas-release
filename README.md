# Canvas Beta

Canvas'ın Windows beta kurulumları ve sürüm notları. Bu depo kurulum dosyalarını dağıtır; kaynak kodu içermez. İndirmeler herkese açıktır.

**Gereksinim:** Windows 11 24H2 veya sonrası, x64.

## 0.1.2.0 kullanıcıları: otomatik güncelleme testi

Güncel paket `0.1.3.0`, uygulama sürümü `0.1.3-beta.1`'dir. `.appinstaller` üzerinden `0.1.2.0`'a geçtiyseniz **bu testte yeni kurulum dosyası indirmeyin veya açmayın; uygulamayı kaldırmayın.**

Çalışmalarınızı kaydedip Canvas Beta'yı kapatın ve Başlat menüsünden açın. Windows'un indirmeyi ve güncellemeyi uygun olduğunda tamamlamasına izin verin; ardından kaydedip kapatın ve Başlat menüsünden yeniden açın. **Ayarlar → Update** sayfasında `0.1.3-beta.1` göründüğünü ve mevcut projelerinizin korunduğunu kontrol edin. Güncelleme sessiz uygulanabilir; bildirim veya kesin bir tamamlanma süresi beklemeyin. Elle kurulum yapmadan sürümün değişmesi otomatik güncellemeyi doğrular.

## Kurulum / 0.1.1.0'dan güncelleme

**[Canvas-Beta.appinstaller indir](https://github.com/kbingol/canvas-release/releases/download/beta-feed/Canvas-Beta.appinstaller)**

Dosyayı indirip açın; Windows'un kurulum penceresinde **Yükle** veya **Güncelle** seçin. Mevcut `0.1.1.0` kurulumunu kaldırmayın. Sertifikası zaten güvenilir olan kullanıcıların yeniden sertifika yüklemesi gerekmez.

İlk kez kuruyorsanız önce [Canvas-Beta.cer](https://github.com/kbingol/canvas-release/releases/download/v0.1.3-beta.1/Canvas-Beta.cer) sertifikasını indirin. Parmak izi:

```text
5BE262C15AEEEF8771888BFEE1AF99CD35F3344F
```

Sertifikayı açıp **Sertifika Yükle → Yerel Makine → Tüm sertifikaları aşağıdaki depolama alanına yerleştir → Gözat → Güvenilen Kişiler → Tamam → İleri → Son** yolunu izleyin. Yönetici onayı gerekir. Bu test sertifikasına güvenme işlemi her bilgisayarda bir kez yapılır. Geçerli Kullanıcı veya Güvenilen Kök Sertifika Yetkilileri deposunu seçmeyin. Ardından yukarıdaki `.appinstaller` dosyasını açın.

## Sonraki güncellemeler

`.appinstaller` ile kurulduktan/güncellendikten sonra Windows, uygulama açılışında yeni sürümleri denetler ve paket güncellemesini yönetir. Canvas paketlenmiş bir masaüstü uygulamasıdır: Windows bu tür uygulamaları **güncelleme penceresi göstermeden** güncelleyebilir. `.appinstaller` tek başına Canvas içinden yeni sürüm bildirimi sağlamaz. Uygulama açıkken yeni sürüm yayımlanması anında bildirim oluşturmaz.

Doğrudan `.msix` ile kurulum güncelleme adresini kaydetmez. Windows'un sonraki sürümleri takip etmesi için yukarıdaki `.appinstaller` bağlantısını kullanın.

**[Tüm sürümler ve sürüm notları](https://github.com/kbingol/canvas-release/releases)** · **[Ayrıntılı kurulum kılavuzu](https://github.com/kbingol/canvas-release/releases/download/v0.1.3-beta.1/README.md)**

Eski `0.1.0.0` farklı paket kimliği kullanır ve yerinde güncellenmez. Projeleri `.flow` olarak dışa aktarıp yeni beta'da açın; kişisel asistanlarınızı yedekleyin. Kaldırma paket verilerini silebilir.

Microsoft belgeleri: [test sertifikasıyla dağıtım](https://learn.microsoft.com/en-us/windows/msix/package/sign-msix-package-guide#testing-distribute-to-testers-with-a-self-signed-certificate), [sertifika deposu](https://learn.microsoft.com/en-us/windows/msix/app-installer/troubleshoot-appinstaller-issues#trusted-certificates), [masaüstü uygulamalarında güncelleme davranışı](https://learn.microsoft.com/en-us/uwp/schemas/appinstallerschema/element-onlaunch#remarks).
