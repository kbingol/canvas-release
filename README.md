# Canvas Beta

Canvas'ın Windows beta kurulumları ve sürüm notları. Bu depo kurulum dosyalarını dağıtır; kaynak kodu içermez. İndirmeler herkese açıktır.

**Gereksinim:** Windows 11 24H2 veya sonrası, x64.

## 0.1.6.0 → 0.1.7.0 güncelleme testi

Güncel paket `0.1.7.0`, uygulama sürümü `0.1.7-beta.1`'dir. Bu yayın, mevcut açılış güncelleyicisini gerçek paketler arasında sınamak için yalnız sürüm numaralarını yükseltir.

Testin başlangıcında `0.1.6.0` (`0.1.6-beta.1`) kurulu olmalıdır. **Bu test için yeni kurulum dosyası indirmeyin veya açmayın; uygulamayı kaldırmayın.**

1. Canvas Beta'yı açmadan, Windows Ayarları'ndaki kurulu uygulama bilgilerinden başlangıç sürümünün `0.1.6.0` olduğunu doğrulayın.
2. Çalışmalarınızı kaydedip tüm Canvas Beta pencerelerini normal şekilde kapatın.
3. İnternet bağlantısı açıkken Canvas Beta'yı **Başlat menüsünden** açın. Beklenen akış: açılışta denetim, indirme, yükleme ve yeni sürümle yeniden açılış.
4. **Ayarlar → Update** sayfasında `0.1.7-beta.1` göründüğünü ve projelerinizin korunduğunu kontrol edin.

Windows'un arka plan görevi önceden güncellemişse uygulama zaten `0.1.7-beta.1` olarak açılabilir; bu durumda açılışta indirme ve yeniden başlatma akışı sınanmış olmaz. Gerçek kurulumdan yeni sürüme yeniden açılışa kadar uçtan uca test henüz tamamlanmamıştır.

Hata çıkarsa açılış ekranındaki tam hata metnini kaydedin. Uygulamayı kaldırmayın, diğer Canvas işlemlerini zorla sonlandırmayın veya sertifika güven ayarlarını değiştirmeyin.

## 0.1.5.0'dan ilk geçiş

`0.1.5.0` henüz açılış güncelleyicisine sahip değildir. Çalışmalarınızı kaydedip Canvas Beta'yı kapatın; Windows'un mevcut arka plan güncellemesini bekleyin veya aşağıdaki `.appinstaller` dosyasını açıp **Güncelle** seçin. Uygulamayı kaldırmayın. Bu geçiş, yukarıdaki açılış güncellemesi testi sayılmaz.

## Kurulum / 0.1.1.0'dan güncelleme

**[Canvas-Beta.appinstaller indir](https://github.com/kbingol/canvas-release/releases/download/beta-feed/Canvas-Beta.appinstaller)**

Dosyayı indirip açın; Windows'un kurulum penceresinde **Yükle** veya **Güncelle** seçin. Mevcut `0.1.1.0` kurulumunu kaldırmayın. Sertifikası zaten güvenilir olan kullanıcıların yeniden sertifika yüklemesi gerekmez.

İlk kez kuruyorsanız önce [Canvas-Beta.cer](https://github.com/kbingol/canvas-release/releases/download/v0.1.7-beta.1/Canvas-Beta.cer) sertifikasını indirin. Parmak izi:

```text
5BE262C15AEEEF8771888BFEE1AF99CD35F3344F
```

Sertifikayı açıp **Sertifika Yükle → Yerel Makine → Tüm sertifikaları aşağıdaki depolama alanına yerleştir → Gözat → Güvenilen Kişiler → Tamam → İleri → Son** yolunu izleyin. Yönetici onayı gerekir. Bu test sertifikasına güvenme işlemi her bilgisayarda bir kez yapılır. Geçerli Kullanıcı veya Güvenilen Kök Sertifika Yetkilileri deposunu seçmeyin. Ardından yukarıdaki `.appinstaller` dosyasını açın.

## Sonraki güncellemeler

`0.1.6.0` ve sonrasında Canvas Beta, çalışma alanı açılmadan önce güncellemeyi denetler. Güncelleme yoksa normal açılır. Yeni beta sürümü varsa indirme ve yükleme ilerlemesini gösterir, ardından yeni sürümü açmak için yeniden başlatma işlemini başlatır. Bulunan beta güncellemesi tamamlanmadan eski sürümün çalışma alanı açılmaz.

İnternet bağlantısı yoksa veya denetim/yükleme başarısızsa **Yeniden dene** seçeneği gösterilir; sorun çözülmeden çalışma alanına geçilmez. Pencereyi kapatabilirsiniz. Başka Canvas pencereleri yeni sürümün açılmasını engelliyorsa çalışmalarınızı kaydedip o pencereleri kapatın ve yeniden deneyin; diğer pencereler zorla kapatılmaz.

Windows'un sessiz arka plan güncellemesi de korunur. Güncellemenin belirli bir sürede tamamlanacağı garanti edilmez. Her sürümde kurulum dosyası indirmeniz veya aynı sertifikayı yeniden yüklemeniz gerekmez. Güncelleme adresini kaydetmek için ilk kurulumda veya bir defalık geçişte yukarıdaki `.appinstaller` bağlantısını kullanın; doğrudan `.msix` ile kurulum bu adresi kaydetmez.

**[Tüm sürümler ve sürüm notları](https://github.com/kbingol/canvas-release/releases)** · **[Ayrıntılı kurulum kılavuzu](https://github.com/kbingol/canvas-release/releases/download/v0.1.7-beta.1/README.md)**

Eski `0.1.0.0` farklı paket kimliği kullanır ve yerinde güncellenmez. Projeleri `.flow` olarak dışa aktarıp yeni beta'da açın; kişisel asistanlarınızı yedekleyin. Kaldırma paket verilerini silebilir.

Microsoft belgeleri: [test sertifikasıyla dağıtım](https://learn.microsoft.com/en-us/windows/msix/package/sign-msix-package-guide#testing-distribute-to-testers-with-a-self-signed-certificate), [sertifika deposu](https://learn.microsoft.com/en-us/windows/msix/app-installer/troubleshoot-appinstaller-issues#trusted-certificates), [otomatik güncelleme davranışı](https://learn.microsoft.com/en-us/windows/msix/app-installer/auto-update-and-repair--overview), [güncelleme seçenekleri](https://learn.microsoft.com/en-us/windows/msix/app-installer/update-settings).
