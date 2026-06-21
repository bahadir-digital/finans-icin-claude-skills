---
name: aging-analysis
description: Alacakları ve borçları vade yaşına göre gruplar (0-30, 31-60, 61-90, 90+ gün), geciken kalemleri öne çıkarır, tahsilat riskini ve ortalama tahsilat/ödeme süresini gösterir. "Alacak yaşlandırma", "borç yaşlandırma", "kim ne kadar geciktirdi", "vadesi geçen faturalar", "tahsilat riski", "aging" gibi ifadelerde tetiklenir.
---

# Alacak/Borç Yaşlandırma Analizi

Açık alacak ve borçları vade yaşına göre kovalara böler, hangi tutarın ne kadar süredir beklediğini gösterir. Tahsilat takibi ve tedarikçi ödeme planı için temel araç.

## Ne zaman tetiklenir
- "Alacak yaşlandırma tablosu çıkar"
- "Vadesi 90 günü geçen alacaklar kim?"
- "Müşteri bazında geciken bakiyeleri göster"
- "Borçlarımızın yaşlandırmasını yap"
- "Ortalama tahsilat süremiz ne?"

## Girdi
- Açık kalemler listesi (müşteri/tedarikçi, fatura tutarı, fatura veya vade tarihi)
- Referans tarih (bugün veya rapor tarihi)
- Varsa toplam satış/alış (DSO/DPO hesabı için, opsiyonel)
- Para birimi

## Çıktı yapısı
1. **Yaşlandırma tablosu** — Cari / 0-30 / 31-60 / 61-90 / 90+ gün / Toplam
2. **Vadesi geçenler** — gün cinsinden gecikmeye göre sıralı, en riskliler üstte
3. **Yoğunlaşma** — toplam alacağın ne kadarı tek müşteride/tedarikçide
4. **DSO / DPO** — ortalama tahsilat / ödeme süresi (veri varsa)
5. **Aksiyon notu** — öncelikli takip edilecek bakiyeler

## Kurallar
- Yaş = referans tarih − vade tarihi (vade yoksa fatura tarihi + bilinen vade gününü kullan).
- 90+ kovasını her zaman ayrı ve görünür tut; şüpheli alacak adayı budur.
- Tek müşteride toplanan yüksek bakiyeyi (yoğunlaşma riski) belirt.
- Tahsil edilemez demek için yeterli bilgi yoksa "şüpheli/takip" de, karşılık ayır deme.
- Alacak ve borç yaşlandırmasını ayrı tablo olarak ver, karıştırma.

## Örnek
**Girdi:** X müşterisi 120.000 TL, fatura 100 gün önce, vade 30 gün.
**Çıktı:** 90+ gün kovasında, 70 gün gecikmiş. Toplam alacağın %35'i bu müşteride. Aksiyon: önce bu bakiye için yazılı tahsilat hatırlatması ve ödeme planı görüşmesi; tahsilat olmadan yeni vade açma.
