# Graduation-Project
Mobile Driving Assistant Application

Bu proje, iPhone'da çalışan bir mobil sürüş asistanı uygulaması geliştirmeyi amaçlamaktadır. Uygulama, YOLO tabanlı trafik işaretleri, trafik ışıkları ve şerit takip sistemi kullanarak, sürücülere gerçek zamanlı yol uyarıları sağlamaktadır. Ayrıca, kamera görüntüsü üzerinden trafik levhaları ve ışıkları algılar, şerit takip yapar ve sesli uyarılar ile kullanıcıyı bilgilendirir.

 # Özellikler
Gerçek Zamanlı Trafik Levhası Tespiti
Trafik işaretleri (örneğin, hız sınırı, dur işareti) algılanır ve kullanıcıya sesli veya görsel uyarı verilir.

Trafik Işığı Tespiti
Kırmızı, yeşil, sarı ışıklar tespit edilir ve kullanıcıya trafik ışığının durumu bildirilir.

Şerit Takip Sistemi
Araç şeritlerini takip eder. Şeritten sapma durumunda sesli uyarı verilir.

Sesli ve Görsel Uyarılar
Trafik işareti ve ışığı algılandığında sesli uyarı (düt sesi) verilir. Şeritten sapma durumunda kırmızı ekran gösterilir.

Hız Göstergesi
GPS verisiyle hız takibi yapılır. Hız göstergesi ekranda görüntülenir.

Gece/Gündüz Modu
Zaman dilimine göre gece veya gündüz moduna geçiş yapılır. Gece modunda ekran daha az ışık yayar.

# Teknolojiler ve Araçlar
Flutter: Uygulama geliştirme için kullanıldı.

YOLOv8: Trafik levhaları ve ışıkları tespit etmek için kullanıldı.

TFLite: Modeli mobil uyumlu hale getirmek için kullanıldı.

Camera Plugin: Canlı kamera görüntüsü almak için kullanıldı.

Dart: Flutter ile birlikte kullanılan programlama dili.

TensorFlow Lite: Modelin mobil uyumlu hale getirilmesi için kullanıldı.

# Proje Yapısı
bash
Kopyala
Düzenle
/mobil_surusu_asistani
│
├── /assets                  # Görsel ve model dosyaları
│   └── /models              # YOLO model dosyaları
│   └── /images              # Uygulama içindeki resimler (ikonlar vs.)
│
├── /lib
│   ├── /components          # Yeniden kullanılabilir widget'lar
│   ├── /screens             # Ekranlar (Ana ekran, ayarlar ekranı, vb.)
│   ├── /services            # Kamera, model yükleme ve nesne tespiti
│   └── /utils               # Yardımcı fonksiyonlar (gece/gündüz modu, hız hesaplama)
│
├── /test                    # Birim testleri ve widget testleri
│
├── pubspec.yaml             # Flutter bağımlılıkları
└── README.md                # Proje açıklaması


# Geliştirici Notları
Model Yükleme: Uygulama, YOLO modelini TensorFlow Lite formatında çalıştırır. Modeli Flutter içinde yüklemek ve çalıştırmak için tflite_flutter paketini kullandık.

Kamera Entegrasyonu: camera Flutter plugin'i kullanılarak canlı kamera görüntüsü alınır ve bu görüntü üzerine nesne tespiti yapılır.

Hız Takibi: Gerçek zamanlı hız verisi almak için geolocator veya location gibi paketler kullanılabilir.

Uyarılar: Sesli uyarılar için Flutter'ın audioplayers paketinden yararlanılabilir.

# Bu proje, yalnızca eğitim ve kişisel kullanım amaçlıdır. Ticari veya ticari olmayan başka bir şekilde yeniden dağıtılamaz, değiştirilip satılamaz.
