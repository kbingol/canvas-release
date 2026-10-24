# Canvas Beta

Canvas'ın Windows beta kurulumları ve sürüm notları. Bu depo kurulum dosyalarını dağıtır; kaynak kodu içermez. İndirmeler herkese açıktır.

**Gereksinim:** Windows 11 24H2 veya sonrası, x64.

## 0.1.6.0 sürümüne geçiş

Güncel paket `0.1.6.0`, uygulama sürümü `0.1.6-beta.1`'dir. Bu sürüm, çalışma alanı açılmadan önce güncellemeyi denetleyen ve bulunan beta güncellemesini yükleyen açılış ekranını içerir.

`0.1.5.0` henüz bu açılış davranışına sahip değildir. İlk geçiş için çalışmalarınızı kaydedip Canvas Beta'yı kapatın; Windows'un mevcut arka plan güncellemesini bekleyin veya aşağıdaki `.appinstaller` dosyasını açıp **Güncelle** seçin. Uygulamayı kaldırmayın. Başlat menüsünden açtıktan sonra **Ayarlar → Update** sayfasında `0.1.6-beta.1` göründüğünü ve projelerinizin korunduğunu kontrol edin.

Yeni açılış akışının güncelleme testi, `0.1.6.0` kurulduktan sonra `0.1.7.0` gibi daha yüksek bir sürüm yayımlandığında yapılabilir: yeni kurulum dosyası indirmeden Canvas Beta'yı Başlat menüsünden açın ve güncellemeyi açılış ekranından takip edin. Gerçek kurulumdan yeni sürüme yeniden açılışa kadar uçtan uca test henüz tamamlanmamıştır.

## Kurulum / 0.1.1.0'dan güncelleme

**[Canvas-Beta.appinstaller indir](https://github.com/kbingol/canvas-release/releases/download/beta-feed/Canvas-Beta.appinstaller)**

Dosyayı indirip açın; Windows'un kurulum penceresinde **Yükle** veya **Güncelle** seçin. Mevcut `0.1.1.0` kurulumunu kaldırmayın. Sertifikası zaten güvenilir olan kullanıcıların yeniden sertifika yüklemesi gerekmez.

İlk kez kuruyorsanız önce [Canvas-Beta.cer](https://github.com/kbingol/canvas-release/releases/download/v0.1.6-beta.1/Canvas-Beta.cer) sertifikasını indirin. Parmak izi:

```text
5BE262C15AEEEF8771888BFEE1AF99CD35F3344F
```

Sertifikayı açıp **Sertifika Yükle → Yerel Makine → Tüm sertifikaları aşağıdaki depolama alanına yerleştir → Gözat → Güvenilen Kişiler → Tamam → İleri → Son** yolunu izleyin. Yönetici onayı gerekir. Bu test sertifikasına güvenme işlemi her bilgisayarda bir kez yapılır. Geçerli Kullanıcı veya Güvenilen Kök Sertifika Yetkilileri deposunu seçmeyin. Ardından yukarıdaki `.appinstaller` dosyasını açın.

## Sonraki güncellemeler

`0.1.6.0` ve sonrasında Canvas Beta, çalışma alanı açılmadan önce güncellemeyi denetler. Güncelleme yoksa normal açılır. Yeni beta sürümü varsa indirme ve yükleme ilerlemesini gösterir, ardından yeni sürümü açmak için yeniden başlatma işlemini başlatır. Bulunan beta güncellemesi tamamlanmadan eski sürümün çalışma alanı açılmaz.

İnternet bağlantısı yoksa veya denetim/yükleme başarısızsa **Yeniden dene** seçeneği gösterilir; sorun çözülmeden çalışma alanına geçilmez. Pencereyi kapatabilirsiniz. Başka Canvas pencereleri yeni sürümün açılmasını engelliyorsa çalışmalarınızı kaydedip o pencereleri kapatın ve yeniden deneyin; diğer pencereler zorla kapatılmaz.

Windows'un sessiz arka plan güncellemesi de korunur. Güncellemenin belirli bir sürede tamamlanacağı garanti edilmez. Her sürümde kurulum dosyası indirmeniz veya aynı sertifikayı yeniden yüklemeniz gerekmez. Güncelleme adresini kaydetmek için ilk kurulumda veya bir defalık geçişte yukarıdaki `.appinstaller` bağlantısını kullanın; doğrudan `.msix` ile kurulum bu adresi kaydetmez.

**[Tüm sürümler ve sürüm notları](https://github.com/kbingol/canvas-release/releases)** · **[Ayrıntılı kurulum kılavuzu](https://github.com/kbingol/canvas-release/releases/download/v0.1.6-beta.1/README.md)**

Eski `0.1.0.0` farklı paket kimliği kullanır ve yerinde güncellenmez. Projeleri `.flow` olarak dışa aktarıp yeni beta'da açın; kişisel asistanlarınızı yedekleyin. Kaldırma paket verilerini silebilir.

Microsoft belgeleri: [test sertifikasıyla dağıtım](https://learn.microsoft.com/en-us/windows/msix/package/sign-msix-package-guide#testing-distribute-to-testers-with-a-self-signed-certificate), [sertifika deposu](https://learn.microsoft.com/en-us/windows/msix/app-installer/troubleshoot-appinstaller-issues#trusted-certificates), [otomatik güncelleme davranışı](https://learn.microsoft.com/en-us/windows/msix/app-installer/auto-update-and-repair--overview), [güncelleme seçenekleri](https://learn.microsoft.com/en-us/windows/msix/app-installer/update-settings).
