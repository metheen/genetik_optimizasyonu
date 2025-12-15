# Proje Bilgileri
**Adınız:** Metin Can
**Soyadınız:** Nasıf
**Okul Numaranız:** 2212721017
**GitHub Repo Bağlantısı:** https://github.com/metheen/genetik_optimizasyonu

---

# Genetik Algoritma ile Test Çözeltisi Optimizasyonu (Senaryo 7)

Bu proje, Reaktif A ve Reaktif B karışım oranlarını optimize ederek en yüksek test hassasiyetini bulmayı amaçlar. Çözüm için **Genetik Algoritma** kullanılmış, kısıtlar **Ceza Yöntemi** ile yönetilmiştir.

## 1. Problem Özeti

Amaç, aşağıdaki fonksiyonu verilen kısıtlar dahilinde maksimize etmektir.

* **Amaç Fonksiyonu:**
    $$y = 3x_1 + 2x_2 + x_1x_2 - 0.5x_2^2$$

* **Değişken Sınırları:**
    * $x_1$ (Reaktif A) ve $x_2$ (Reaktif B) $\in [10, 80]$

* **Zorunlu Kısıtlar:**
    1.  $x_1 + x_2 \le 100$ (Toplam hacim sınırı)
    2.  $x_1 \ge 25$ (Minimum A oranı)

## 2. Algoritma Detayları

Projede kullanılan Genetik Algoritma parametreleri şunlardır:

* **Kodlama:** Reel Değer (Float) Kodlaması
* **Seçim Yöntemi:** Turnuva Seçimi (Tournament Selection)
* **Çaprazlama:** Aritmetik Çaprazlama (Arithmetic Crossover)
* **Mutasyon:** Gaussian (Normal Dağılım) Gürültü ekleme
* **Kısıt Yönetimi:** Kısıtları ihlal eden bireylere yüksek negatif ceza (-9999) uygulanarak elenmeleri sağlanır.

## 3. Kurulum ve Çalıştırma

Gerekli kütüphaneleri yükleyip projeyi çalıştırmak için terminalde aşağıdaki komutları kullanabilirsiniz:

```bash
# Kütüphanelerin yüklenmesi
pip install numpy matplotlib

# Projenin çalıştırılması
python main.py
