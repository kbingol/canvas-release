# Canvas Beta

Canvas'ın Windows beta kurulumları ve sürüm notları. Bu depo kurulum dosyalarını dağıtır; kaynak kodu içermez. İndirmeler herkese açıktır.

**Gereksinim:** Windows 11 24H2 veya sonrası, x64.

## 0.1.4.0 kullanıcıları: arka plan güncellemesi testi

Güncel paket `0.1.5.0`, uygulama sürümü `0.1.5-beta.1`'dir. `.appinstaller` üzerinden kurduğunuz `0.1.4.0` sürümünden geçerken **bu testte yeni kurulum dosyası indirmeyin veya açmayın; uygulamayı kaldırmayın.**

Çalışmalarınızı kaydedip Canvas Beta'yı kapatın; bilgisayarı internet bağlantısıyla açık bırakın. Windows'un yaklaşık sekiz saatte bir çalışan arka plan görevinin indirmeyi ve güncellemeyi uygun olduğunda tamamlamasına izin verin. Daha sonra Başlat menüsünden açıp **Ayarlar → Update** sayfasında `0.1.5-beta.1` göründüğünü ve mevcut projelerinizin korunduğunu kontrol edin. Elle kurulum yapmadan sürümün değişmesi otomatik geçişi doğrular; kesin bir tamamlanma süresi beklemeyin.

Eski açılış denetimi ayarları Windows yeni yapılandırmayı kaydedene kadar geçerli kalabilir; ilk açılışın hiç beklemeden gerçekleşeceği garanti edilmez. Bu sürüm için yerel kurulum ve uygulamayı çalıştırarak uçtan uca güncelleme testi yapılmamıştır.

## Kurulum / 0.1.1.0'dan güncelleme

**[Canvas-Beta.appinstaller indir](https://github.com/kbingol/canvas-release/releases/download/beta-feed/Canvas-Beta.appinstaller)**

Dosyayı indirip açın; Windows'un kurulum penceresinde **Yükle** veya **Güncelle** seçin. Mevcut `0.1.1.0` kurulumunu kaldırmayın. Sertifikası zaten güvenilir olan kullanıcıların yeniden sertifika yüklemesi gerekmez.

İlk kez kuruyorsanız önce [Canvas-Beta.cer](https://github.com/kbingol/canvas-release/releases/download/v0.1.5-beta.1/Canvas-Beta.cer) sertifikasını indirin. Parmak izi:

```text
5BE262C15AEEEF8771888BFEE1AF99CD35F3344F
```

Sertifikayı açıp **Sertifika Yükle → Yerel Makine → Tüm sertifikaları aşağıdaki depolama alanına yerleştir → Gözat → Güvenilen Kişiler → Tamam → İleri → Son** yolunu izleyin. Yönetici onayı gerekir. Bu test sertifikasına güvenme işlemi her bilgisayarda bir kez yapılır. Geçerli Kullanıcı veya Güvenilen Kök Sertifika Yetkilileri deposunu seçmeyin. Ardından yukarıdaki `.appinstaller` dosyasını açın.

## Sonraki güncellemeler

`.appinstaller` ile ilk kurulum veya bir defalık geçiş, Windows'a sabit güncelleme adresini kaydeder. Bu sürüm yalnız `AutomaticBackgroundTask` kullanır: Windows, uygulama açılmasa da yaklaşık sekiz saatte bir penceresiz arka plan denetimi yapar. `OnLaunch` kaldırılmıştır; yeni yapılandırma kaydedildikten sonra denetim uygulama açılışına bağlı değildir.

Windows paketi indirip uygun zamanda uygular; belirli bir sürede veya açılışta yeni sürüme geçiş garanti değildir. Her sürümde kurulum dosyası indirmeniz veya aynı sertifikayı yeniden yüklemeniz gerekmez. Canvas'a özel açılış güncelleme ekranı veya uygulama içi güncelleyici eklenmemiştir.

Doğrudan `.msix` ile kurulum güncelleme adresini kaydetmez. Windows'un sonraki sürümleri takip etmesi için yukarıdaki `.appinstaller` bağlantısını kullanın.

**[Tüm sürümler ve sürüm notları](https://github.com/kbingol/canvas-release/releases)** · **[Ayrıntılı kurulum kılavuzu](https://github.com/kbingol/canvas-release/releases/download/v0.1.5-beta.1/README.md)**

Eski `0.1.0.0` farklı paket kimliği kullanır ve yerinde güncellenmez. Projeleri `.flow` olarak dışa aktarıp yeni beta'da açın; kişisel asistanlarınızı yedekleyin. Kaldırma paket verilerini silebilir.

Microsoft belgeleri: [test sertifikasıyla dağıtım](https://learn.microsoft.com/en-us/windows/msix/package/sign-msix-package-guide#testing-distribute-to-testers-with-a-self-signed-certificate), [sertifika deposu](https://learn.microsoft.com/en-us/windows/msix/app-installer/troubleshoot-appinstaller-issues#trusted-certificates), [otomatik güncelleme davranışı](https://learn.microsoft.com/en-us/windows/msix/app-installer/auto-update-and-repair--overview), [güncelleme seçenekleri](https://learn.microsoft.com/en-us/windows/msix/app-installer/update-settings).
