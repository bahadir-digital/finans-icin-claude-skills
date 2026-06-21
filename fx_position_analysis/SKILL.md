---
name: fx-position-analysis
description: Döviz cinsinden varlık ve yükümlülükleri para birimi bazında netleştirir, açık/kapalı pozisyonu çıkarır, kur farkı gelir/giderini hesaplar ve kur değişimine duyarlılığı (senaryo) gösterir. "Döviz pozisyonu", "kur riski", "açık pozisyon", "kur farkı geliri gideri", "dolar artarsa ne olur", "kura duyarlılık" gibi ifadelerde tetiklenir.
---

# Kur Farkı ve Döviz Pozisyonu Analizi

Döviz cinsinden alacak, borç ve nakit kalemlerini toplayıp net pozisyonu gösterir; kur hareketinin bilanço ve kâra etkisini hesaplar. Kurun oynak olduğu ortamda finans tarafının düzenli bakması gereken analiz.

## Ne zaman tetiklenir
- "Döviz açık pozisyonumuz ne kadar?"
- "Kur 5 lira artarsa kâr nasıl etkilenir?"
- "Kur farkı gelir/giderini hesapla"
- "Hangi para biriminde ne kadar riskliyiz?"
- "Döviz borcu ve alacağımızı netleştir"

## Girdi
- Döviz cinsinden kalemler (varlık: kasa/banka, alacak; yükümlülük: borç, kredi), para birimi ve tutar
- Dönem başı ve dönem sonu kurları (kur farkı için) ya da güncel kur
- Senaryo için test edilecek kur değişimi (örn. +%10, −%10)
- Raporlama para birimi (genelde TL)

## Çıktı yapısı
1. **Pozisyon tablosu** — Para birimi / Döviz varlık / Döviz yükümlülük / Net pozisyon (döviz ve TL)
2. **Açık pozisyon** — net kısa/uzun pozisyon ve TL karşılığı
3. **Kur farkı** — dönem başı/sonu kur farkından doğan gelir/gider (veri varsa)
4. **Duyarlılık senaryosu** — kur ±X% değişiminde kâr/özkaynak etkisi
5. **Yorum** — risk yönü ve dikkat edilecek para birimi

## Kurallar
- Net pozisyon = döviz varlık − döviz yükümlülük; her para birimi ayrı satır, sonra TL'ye çevir.
- Kısa pozisyonda (yükümlülük > varlık) kur artışı zarar, uzun pozisyonda kâr yazar; yönü doğru kur.
- Gerçekleşmiş kur farkı ile değerleme (henüz kapanmamış) farkını ayır.
- Doğal hedge varsa (gelir ve gider aynı dövizde) belirt; brüt pozisyonu net riskle karıştırma.
- Tahmini senaryo kuru gerçek değildir; "varsayım" olarak işaretle.

## Örnek
**Girdi:** 200.000 USD banka, 500.000 USD kredi borcu. Güncel kur 33 TL. Senaryo: kur +%10.
**Çıktı:** Net pozisyon −300.000 USD (kısa), TL karşılığı −9.900.000 TL. Kur %10 artarsa (≈36,3 TL) yaklaşık 990.000 TL ek kur farkı gideri doğar. Risk: USD'de kısa pozisyon; kur artışına açık. Senaryo varsayımdır.
