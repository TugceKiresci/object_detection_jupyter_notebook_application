API İLE İLGİLİ BİLGİLER

Klasör Yapısı:<br>
api/<br>
└── api_project/<br>
└── camera/ # API kodlarının bulunduğu klasör<br>

Kurulum Adımları:
1) Klasöre Gir
	<br>cd Desktop/yeni_api
2) Sanal Ortamı Oluştur (ilk kez kurulum yapılıyorsa)
	<br>python -m venv myenv (Sİstemine bağlı olarak python yerine python3 de kullanılabilir.)
	<br>//Bu işlem sonun yeni_api klasöründe myenv adında bir klasör oluşur.
3) Sanal Ortamı Aktifleştir
	<br>myenv\Scripts\activate

4) API'yi Çalıştırmak
	<br>cd api_project (projenin çalıştırılacağı klasöre gidilir.)
	<br>python manage.py runserver (API' yi çalıştıran komut. Bu komut sonucunda API linki gelmeli.)


KAMERA İLE İLE İLGİLİ UYGULAMALAR 

1) Robot Tespiti Uygulaması
2) Hareketli Nesne Yön Tahmini Uygulaması

Kurulum

Aşağıdaki Python paketlerinin yüklü olması gerekir:
<br>pip install opencv-python ipywidgets matplotlib Pillow requests numpy ipympl

Jupyter Notebook’ta widget desteği için şu komut çalıştırılmalıdır:
<br>jupyter nbextension enable --py widgetsnbextension --sys-prefix


Klasör Yapısı
<br>.
<br>├── Kamera_Uygulamaları.ipynb
<br>├── dataset/                  # Görüntü dosyaları
<br>├── dataset_videos/          # Video dosyaları (hareket analizi için)


1)Robot Tespiti Uygulaması

Özellikler<br>
-Görüntü kaynağı olarak dataset, webcam, veya API seçilebilir.<br>
-Üç farklı tespit algoritması sekmeler (tabs) halinde sunulmaktadır:<br>
	<br>Algoritma 1: Belirli filtreleme ve eşikleme
	<br>Algoritma 2: Renk tabanlı maskeleme
	<br>Algoritma 3: Gelişmiş eşikleme veya morfolojik işlemler
	<br>(algoritmalar değiştirilebilir ve genişletilebilir yapıdadır)<br>
<br>-Her algoritma sekmesinde yalnızca o algoritmaya ait parametreler görünür.
<br>-Dataset seçildiğinde tam orijinal görüntü, renk bozulmadan gösterilir.
<br>-Webcam veya API kaynağı seçildiğinde sabit pencere içinde gerçek zamanlı video önizleme yapılır.
<br>-“Görüntü İşle” butonuna basıldığında o anki görüntü yakalanır, işlenir ve gösterilir.

Kullanım Akışı

Dataset seçilirse:
<br>-Dropdown menüden görüntü seçilir.
<br>-Görüntü doğrudan gösterilir.

Webcam veya API seçilirse:
<br>-Video önizleme canlı olarak gösterilir.
<br>-“Görüntü İşle” butonuna tıklanınca önizleme durur, kare alınır ve işlenmiş hali gösterilir.

<br>NOT:Dataset seçilince diğer kaynaklara ait bileşenler inaktif hale gelir (tersi de geçerlidir).

2)Hareketli Nesne Yön Tahmini Uygulaması

Özellikler<br>

Görüntü kaynağı: dataset_videos, webcam, veya API
<br>-Hareketli pikseller belirlenerek yön tespiti yapılır.
<br>-Hareketli alanlar dikdörtgen içinde gösterilir.
<br>-Görüntü sabit boyutlu pencere (640x480) içinde oynatılır.
<br>-Webcam/API kaynaklarında canlı video önizleme yapılır.
<br>-“Görüntü İşle” butonuna basıldığında video durur.
<br>-O anki görüntü işlenerek yön bilgisi elde edilir ve işaretlenmiş olarak gösterilir.


