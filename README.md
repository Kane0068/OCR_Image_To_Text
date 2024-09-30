Öncelikle, internet bağlantısı olan bir bilgisayarda şu adımları izleyin: 

* a) Tesseract OCR'ı indirin:

Windows için: https://github.com/UB-Mannheim/tesseract/wiki Linux için: Kaynak kodunu indirip derleyebilirsiniz veya dağıtımınıza özel paket yöneticisini kullanabilirsiniz.

* b) Python paketlerini indirin: Copypip download paddleocr paddlepaddle easyocr opencv-python-headless pandas pytesseract Bu komut, tüm bağımlılıklarıyla birlikte paketleri indirecektir. İndirilen tüm dosyaları (Tesseract kurulum dosyası ve .whl uzantılı Python paketleri) kapalı devre ortamınıza aktarın.

Kapalı devre ortamında: 
* a) Tesseract OCR'ı kurun. 
* b) Python paketlerini şu şekilde yükleyin: Copypip install --no-index --find-links /path/to/downloaded/packages paddleocr paddlepaddle easyocr opencv-python-headless pandas pytesseract

Şimdi, güncellenmiş kodu görelim: OCR Script for Closed Network EnvironmentClick to open code Bu güncellenmiş kod, kapalı devre bir ortamda çalışmak üzere tasarlanmıştır. Önemli noktalar:

Kodun başında, manuel olarak yüklenmesi gereken kütüphanelerin bir listesi bulunmaktadır. Otomatik yükleme komutları kaldırılmıştır, çünkü bunlar kapalı bir ağda çalışmayacaktır. Kodun geri kalanı aynı şekilde çalışmaya devam edecektir.

Bu kodu kapalı devre ortamınızda kullanmak için:

Yukarıda belirtilen adımları izleyerek gerekli tüm paketleri ve Tesseract OCR'ı önceden indirin ve yükleyin. Bu Python scriptini kapalı devre ortamınıza aktarın. 
Scripti çalıştırın: Copypython script_name.py

İstendiğinde, işlemek istediğiniz görüntü dosyalarının yollarını girin ve OCR yöntemini seçin.

Bu yaklaşım, kapalı devre bir ortamda çalışmanıza olanak tanır. Ancak, bazı paketlerin (özellikle easyocr ve paddleocr) ek model dosyaları indirebileceğini unutmayın. Bu dosyaları da önceden indirip uygun konumlara yerleştirmeniz gerekebilir.

Reference : [HuggingFace OCR](https://huggingface.co/spaces/pragnakalp/OCR-image-to-text)
