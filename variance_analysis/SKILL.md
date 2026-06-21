---
name: variance-analysis
description: Bütçe ile gerçekleşen rakamları karşılaştırır, sapmaları tutar ve yüzde olarak hesaplar, lehte/aleyhte ayırır, olası kök nedenleri ve aksiyon önerilerini çıkarır. "Bütçe gerçekleşen karşılaştır", "sapma analizi yap", "plan fiili fark", "neden bütçeyi aştık", "variance" gibi ifadelerde tetiklenir.
---

# Bütçe–Gerçekleşen Sapma Analizi

Bütçe ve fiili rakamları yan yana koyup sapmayı hesaplar, sapmanın yönünü yorumlar ve nereye bakman gerektiğini söyler. Amaç ay sonu kapanışında "neden tuttu, neden tutmadı" sorusunu hızlı cevaplamak.

## Ne zaman tetiklenir
- "Bütçe ile gerçekleşeni karşılaştır"
- "Bu ayın sapma analizini çıkar"
- "Plan-fiili farkı tablo yap"
- "Hangi kalemlerde bütçeyi aştık?"
- "Gelir bütçenin altında kaldı, nedenini göster"

## Girdi
- Bütçe ve fiili rakamlar (kalem bazında: gelir, satışların maliyeti, faaliyet giderleri vb.)
- Dönem bilgisi (ay, çeyrek, kümülatif)
- Varsa önceki dönem rakamı (karşılaştırma için, opsiyonel)
- Para birimi ve binlik/milyon ölçeği

## Çıktı yapısı
1. **Sapma tablosu** — Kalem / Bütçe / Fiili / Sapma (tutar) / Sapma (%) / Yön (lehte/aleyhte)
2. **En büyük 3-5 sapma** — tutar olarak öne çıkanlar, kısa yorum
3. **Olası kök nedenler** — her büyük sapma için 1-2 hipotez (kesin değil, "kontrol edilecek" notu)
4. **Aksiyon önerileri** — kısa, uygulanabilir maddeler
5. **Özet cümle** — dönemin genel görünümü

## Kurallar
- Gelir sapmasında fiili > bütçe = lehte; gider sapmasında fiili < bütçe = lehte. Yönü karıştırma.
- Sapma yüzdesini bütçeye böl, fiiliye değil.
- Çok küçük sapmaları (örn. <%2 ve düşük tutar) öne çıkarma, dikkat dağıtır.
- Kök nedenleri kesinmiş gibi yazma; "muhtemel neden", "doğrulanmalı" dilini kullan.
- Sayıları kullanıcının verdiği ölçek ve para biriminde tut.

## Örnek
**Girdi:** Reklam gideri bütçe 200.000 TL, fiili 260.000 TL.
**Çıktı:** Aleyhte 60.000 TL sapma (+%30). Olası neden: dönem içi ek kampanya veya birim maliyet artışı. Aksiyon: kampanya getirisini (dönüşüm/ciro) gider artışıyla karşılaştır, bütçe dışı harcamayı onay sürecine bağla.
