---
name: profitability-analysis
description: Ürün, müşteri, segment veya proje bazında kârlılığı çıkarır; brüt/katkı/net marjı hesaplar, en kârlı ve zarar ettiren kalemleri sıralar. "Kârlılık analizi", "hangi ürün kâr getiriyor", "müşteri bazında marj", "zarar ettiren ürünler", "segment kârlılığı", "marj kırılımı" gibi ifadelerde tetiklenir.
---

# Kârlılık Analizi

Cironun nereden geldiğini değil, kârın nereden geldiğini gösterir. Ürün/müşteri/segment kırılımında marjı hesaplar ve en çok ile en az kazandıranı ortaya koyar.

## Ne zaman tetiklenir
- "Ürün bazında kârlılığı çıkar"
- "Hangi müşteriler zarar ettiriyor?"
- "Segmentlerin marjını karşılaştır"
- "En kârlı 10 ürün hangisi?"
- "Ciro yüksek ama kâr neden düşük?"

## Girdi
- Kırılım birimi (ürün / müşteri / segment / proje)
- Her birim için gelir ve ilgili maliyetler (doğrudan maliyet; varsa dağıtılmış genel gider)
- Marj tanımı tercihi (brüt / katkı payı / net)
- Para birimi

## Çıktı yapısı
1. **Kârlılık tablosu** — Birim / Gelir / Maliyet / Kâr / Marj % / Toplam kârdaki pay
2. **Sıralama** — en kârlıdan en az kârlıya; zarar edenler ayrı işaretli
3. **Ciro vs kâr karşılaştırması** — yüksek ciro/düşük marj ve tersi durumlar
4. **Yoğunlaşma** — kârın büyük kısmını taşıyan az sayıda birim (Pareto)
5. **Kısa yorum + aksiyon** — fiyatlama, maliyet veya portföy önerisi

## Kurallar
- Marj türünü baştan netleştir; brüt ile katkı payını karıştırma.
- Genel gider dağıtımı yapıldıysa dağıtım anahtarını belirt; keyfi dağıtım yorumu çarpıtır.
- Zarar eden birimi hemen "kapat" deme; stratejik/çapraz satış nedeni olabilir, soru sorarak ayır.
- Yüzde marjı yüksek ama tutarı küçük kalemleri tutar bazında da göster.

## Örnek
**Girdi:** A ürünü ciro 1.000.000 TL / maliyet 920.000 TL; B ürünü ciro 300.000 TL / maliyet 180.000 TL.
**Çıktı:** A marj %8 (80.000 TL), B marj %40 (120.000 TL). Ciro lideri A ama kârı B taşıyor. Aksiyon: A'da fiyat/maliyet gözden geçirilmeli; B'nin hacmini büyütme fırsatı değerlendirilmeli.
