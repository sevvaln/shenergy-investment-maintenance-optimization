<img width="1170" height="400" alt="image" src="https://github.com/user-attachments/assets/f81c2a63-4347-41c1-98c5-400aa878e54d" />

# SHE-NERGY MAKİNE ÖĞRENMESİ İLE YATIRIM BAKIM OPTİMİZASYONU  
# GRUP 13 (WALTER WATT EKİBİ)

Bu depo, Enerjisa She-nergy programı kapsamında bir öğrenci ekibi tarafından geliştirilen kural tabanlı bir karar destek prototipini içermektedir.

Sistem, verilen Excel veri seti üzerinden CBS / Asset kodu bazında kesinti kayıtlarını analiz eder ve her bir şebeke unsuru için:    YATIRIM – BAKIM – OPERASYON kararını üretir.
Üretilen bu kararlar, geliştirilen interaktif Gradio arayüzü üzerinden görselleştirilerek kullanıcıya sunulmaktadır.

# Projenin Temel Yaklaşımı

Bu çalışmanın amacı, elektrik dağıtım şebekelerinde yatırım ve bakım kararlarını verinin izin verdiği çerçevede, şeffaf ve izlenebilir bir karar mantığıyla desteklemektir.

Proje süresince sağlanan veri setleri:

- yatırım ve bakım ayrımını büyük ölçüde belirli eşikler ve açık kurallar üzerinden tanımlamakta,

- akış diyagramı mantığında ilerleyen, deterministik bir yapı sunmaktadır.

Bu nedenle geliştirilen sistem, kural tabanlı bir karar ağacı yaklaşımı ile tasarlanmıştır.

# Karar Mekanizması

Karar mekanizması, aşağıdaki temel değişkenleri kullanır:

- Ortalama yük seviyesi (%80 eşik)

- Şebeke unsuru tipi (TRAFO / FİDER)

- Tarih bilgisi (28.01.2009 öncesi / sonrası)

- Özelleştirme tarihi bulunamadığında imal yılı kullanılır

- Yatırım planı / görüşü (VAR – YOK)

Bu değişkenler üzerinden sistem, her CBS kodu için 7 net karar yolu tanımlar ve tek bir karar üretir:

# YATIRIM – BAKIM – OPERASYON



# Arayüz (Gradio)

Geliştirilen Gradio tabanlı arayüz, karar mekanizmasından bağımsız yeni bir karar üretmez.
Arayüzde gösterilen YATIRIM / BAKIM / OPERASYON sonucu, arka planda çalışan kural tabanlı karar ağacının çıktısıdır.
Arayüzün amacı, bu kararın dayandığı verileri ve özet metrikleri
kullanıcıya şeffaf ve görsel bir şekilde sunmaktır.

Arayüz ile kullanıcı:

- Excel dosyasını yükleyebilir

- CBS kodu girerek analiz çalıştırabilir

- Kararı renkli karar kartı olarak görebilir

- Kesinti kayıtlarını tablo halinde inceleyebilir

- Kesinti nedenlerinin frekans dağılımını görüntüleyebilir

- Yıllara göre kesinti sayılarını inceleyebilir

- İl / ilçe bazlı yaklaşık lokasyonu harita üzerinde görebilir

- Daha önce sorgulanan CBS kodlarını geçmişten tekrar seçebilir

  

# Kullanım

- Excel dosyasını yükleyin (.xlsx)

- CBS kodunu girin

- Analiz Et butonuna basın

- Sistem otomatik olarak karar, özet metrikler ve görselleri üretir

  

# Notlar

- Gerçek veri setleri bu depoda paylaşılmamıştır.

- Kod yapısı, farklı kolon isimleri ve tarih/yük formatlarına uyum sağlayacak şekilde esnek tasarlanmıştır.

- Bu çalışma, teknik bir öğrenci projesi olarak karar destek yaklaşımının uygulanabilir bir prototipini sunmaktadır.

  

# Geliştirme Alanları

- SAIDI / SAIFI metriklerinin doğrudan karar mekanizmasına entegrasyonu

- Yatırım–bakım gri alanlarının modellenebilmesi için ek veri alanlarının tanımlanması

- Kural tabanlı yapı üzerine makine öğrenmesi destekli hibrit karar mekanizmalarının eklenmesi

Projenin karar destek çıktıları, aşağıdaki arayüz bağlantısı üzerinden
interaktif olarak incelenebilir: https://020658f3a6610f4b53.gradio.live/
Not: Arayüz, karar mekanizmasını içeren kodlar çalıştırıldıktan sonra aktif hale gelmekte ve karar ağacının ürettiği çıktıları görselleştirmektedir.

