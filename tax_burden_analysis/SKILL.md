---
name: tax-burden-analysis
description: Dönem kârından kurumlar/geçici vergi yükünü tahmin eder, kanunen kabul edilmeyen giderlerin (KKEG) ve istisnaların etkisini gösterir, efektif vergi oranını ve vergi öncesi/sonrası kâr köprüsünü çıkarır, vergi için ayrılması gereken nakdi hesaplar. Beyanname hazırlamaz. "Vergi tahmini", "kurumlar vergisi ne kadar", "geçici vergi", "efektif vergi oranı", "KKEG etkisi", "vergi için ne kadar ayıralım" gibi ifadelerde tetiklenir.
---

# Vergi Yükü ve Dönem Vergisi Tahmini

Dönem kârının ne kadarının vergiye gideceğini tahmin eder ve nakit planı için "kenara ne ayıralım" sorusunu cevaplar. Ticari kârdan mali kâra köprü kurar. Resmi beyan değil, yönetim tahminidir.

## Ne zaman tetiklenir
- "Bu dönem yaklaşık ne kadar vergi öderiz?"
- "Geçici vergi için ne kadar ayırmalıyız?"
- "Efektif vergi oranımız ne?"
- "KKEG'ler vergiyi ne kadar artırıyor?"
- "Vergi öncesi ve sonrası kârı karşılaştır"

## Girdi
- Dönem ticari kârı (vergi öncesi)
- Kanunen kabul edilmeyen giderler (KKEG) ve varsa vergiden istisna kazançlar
- İndirim/teşvik kalemleri (varsa)
- Uygulanacak kurumlar/geçici vergi oranı (kullanıcıdan al — oran ve sektör istisnaları değişir)
- Para birimi ve dönem

## Çıktı yapısı
1. **Mali kâr köprüsü** — Ticari kâr (+) KKEG (−) İstisna/indirim = Vergi matrahı
2. **Tahmini vergi** — matrah × güncel oran
3. **Efektif vergi oranı** — tahmini vergi / ticari kâr
4. **Nakit karşılığı** — vergi için ayrılması önerilen tutar ve tahmini ödeme dönemi
5. **Doğrulama notu** — oran, istisna ve mahsupların mali müşavirle teyidi

## Kurallar
- Vergi oranını sabit yazma; güncel kurumlar/geçici vergi oranını kullanıcıdan iste. Finans/banka sektörü gibi farklı oranlar olabilir.
- Bu bir tahmindir; matrah, KKEG ve istisnaların kesin tutarı mali müşavir hesabına bağlıdır. "Resmi beyan değil" notunu koru.
- Geçici verginin yıl içinde mahsuplaşacağını hatırlat; aynı kârı iki kez vergi gibi gösterme.
- Ticari kâr ile mali kârı (matrah) net ayır; köprüyü adım adım göster.
- Geçmiş yıl zararı, yatırım indirimi gibi mahsupları kullanıcı belirtmeden varsayma.

## Örnek
**Girdi:** Ticari kâr 5.000.000 TL, KKEG 300.000 TL, istisna yok, oran kullanıcıdan: %25.
**Çıktı:** Matrah = 5.000.000 + 300.000 = 5.300.000 TL. Tahmini vergi = 1.325.000 TL. Efektif oran ≈ %26,5. Nakit önerisi: ilgili geçici/yıllık dönem için ~1,33 milyon TL ayrılmalı. Kesin tutar mali müşavirle teyit edilmeli.
