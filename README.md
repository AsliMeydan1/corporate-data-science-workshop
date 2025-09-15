# corporate-data-science-workshop

# Corporate Data Science Workshop Datasets

Bu repo, kurumsal data science atölyesi için hazırlanmış örnek veri setlerini içerir.  
Katılımcılar bu veriler üzerinde basit keşifsel analiz, veri temizleme ve görselleştirme uygulamaları yapabilir.

---

## Dosyalar

### 1️- `OnlineRetail_Sample.csv`
- **Satır Sayısı:** 1000  
- **Sütunlar:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country  
- **İçerik:** Gerçek bir online perakende veri setinden türetilmiş örnek
- **Amaç:** 
  - Toplam satış analizi
  - En çok satılan ürünler
  - Ülke bazlı satış dağılımı
  - Basit veri temizliği (eksik müşteri ID’leri, iade satırları)

---

### 2️- `OnlineRetail_KirliVeri_Ornek.csv`
- **Satır Sayısı:** 5  
- **Amaç:** Katılımcılarla veri temizleme çalışması yapmak  
- **İçerdiği Hatalar:**
  - Büyük/küçük harf farkı (`Chair` vs `chair`)
  - Negatif Quantity (iade satırı)
  - Eksik CustomerID (boş satır)
  - Standart olmayan ülke ismi (`turkey`)

---

## Kullanım
### Google Colab Üzerinden Çalıştırma

```python
import pandas as pd

# Ana veri seti
url = "https://raw.githubusercontent.com/AsliMeydan1/corporate-data-science-workshop/refs/heads/main/OnlineRetail_Sample.csv"
df = pd.read_csv(url)
df.head()

# Kirli veri örneği
url_dirty = "https://raw.githubusercontent.com/AsliMeydan1/corporate-data-science-workshop/refs/heads/main/OnlineRetail_KirliVeri_Ornek.csv"
df_dirty = pd.read_csv(url_dirty)
df_dirty
