---
name: expense-analysis
description: Giderleri kategoriye göre gruplar, dönemler arası karşılaştırır, beklenmedik artış ve sapmaları (anomali) yakalar, giderin ciroya oranını ve en çok büyüyen kalemleri gösterir. "Gider analizi", "giderler neden arttı", "anormal harcama", "kategori bazında gider", "gider/ciro oranı", "en çok büyüyen giderler" gibi ifadelerde tetiklenir.
---

# Gider Analizi ve Anomali Tespiti

Gider kalemlerini düzenler, dönem dönem karşılaştırır ve "burada bir şey değişmiş" dedirten satırları öne çıkarır. Maliyet kontrolünün ilk adımı.

## Ne zaman tetiklenir
- "Giderleri kategori bazında analiz et"
- "Bu ay giderler neden arttı?"
- "Beklenmedik harcama var mı?"
- "Giderlerin ciroya oranı nasıl değişti?"
- "Geçen yıla göre en çok büyüyen gider kalemleri"

## Girdi
- Gider verisi (kalem/kategori, tutar, dönem)
- Karşılaştırma dönemi (önceki ay/çeyrek/yıl veya bütçe)
- Varsa ciro (gider/ciro oranı için)
- Para birimi

## Çıktı yapısı
1. **Kategori tablosu** — Kategori / Cari dönem / Karşılaştırma / Değişim (tutar, %)
2. **Anomaliler** — beklenenin belirgin üstünde/altında kalan kalemler, kısa not
3. **En çok büyüyen ilk 5** — tutar ve yüzde olarak
4. **Gider/ciro oranı** — toplam ve ana kategorilerde (veri varsa)
5. **Yorum + kontrol listesi** — incelenecek kalemler

## Kurallar
- Anomali eşiğini belirt (örn. ±%20 veya tutar eşiği); keyfi "yüksek" deme.
- Tek seferlik harcamayı (örn. yıllık lisans, ceza) tekrar eden giderden ayır; trendi bozar.
- Mevsimsellik varsa aynı dönemle (YoY) karşılaştır, bir önceki ayla değil.
- Artışı kötü, azalışı iyi diye otomatik yorumlama; bağlam sorulmalı.

## Örnek
**Girdi:** Yazılım/abonelik gideri geçen ay 40.000 TL, bu ay 95.000 TL.
**Çıktı:** +%138 artış, anomali olarak işaretlendi. Olası neden: yeni yıllık abonelik veya kullanıcı sayısı artışı. Kontrol: tek seferlik mi tekrarlı mı, kullanılmayan lisans var mı.
