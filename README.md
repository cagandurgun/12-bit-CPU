# 12-bit CPU
Bu README dosyası, basit ve sınırlı yeteneklere sahip 12-bit Harvard mimarisi kullanan deneysel bir işlemcinin özelliklerini ve temel buyruk kümesini açıklamaktadır. 

## Genel Özellikler 

- 12-bit veri yolu
- Harvard mimarisi (ayrı veri ve buyruk bellekleri)
- Tek vuruşlu çalışma
- 49 KB veri belleği
- 25 MB buyruk belleği

## Buyruk Kümesi İşlemci, 6 temel buyruğa sahiptir: 

1. TOPLAMA (TOP) - opcode: 000
2. ÇIKARMA (CIK) - opcode: 001
3. NOT AND (NND) - opcode: 010
4. YÜKLEME (YUK) - opcode: 011
5. SAKLAMA (SAK) - opcode: 100
6. EŞİTSE DALLAN (ESD) - opcode: 101

## Buyruk Formatı 

Her buyruk 12 bit uzunluğundadır ve şu formatta düzenlenmiştir: 

``` [opcode (3 bit)] [KY1 (3 bit)] [KY2/ANL (3 bit)] [HY/ANL (3 bit)] ``` 

- KY1, KY2: Kaynak yazmaçları - HY: Hedef yazmacı
- ANL: Adres veya dallanma için kullanılan alan

## Özel Notlar 

- ESD (EŞİTSE DALLAN) buyruğu, mevcut konumdan -24 ile +24 arasında buyruk atlayabilme yeteneğine sahiptir.
- YÜKLEME ve SAKLAMA buyrukları, veri belleğine erişim için özel adres hesaplama yöntemleri kullanır.

## Test Senaryoları README dosyasında, işlemcinin temel buyruklarını test etmek için örnek test senaryoları bulunmaktadır: 

1. Toplama Testi
2. Çıkarma Testi
3. Not And Testi
4. Eşitse Dallan Testi

Bu testler, işlemcinin temel işlevselliğini doğrulamak için kullanılabilir.
