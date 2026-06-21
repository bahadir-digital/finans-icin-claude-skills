---
name: kdv-analysis
description: Hesaplanan, indirilecek ve devreden KDV'yi ayrıştırır, ödenecek KDV veya iade pozisyonunu çıkarır, tevkifatlı işlemleri ve KDV'nin nakit akışına etkisini gösterir. Yönetim seviyesinde analizdir, beyanname hazırlamaz. "KDV analizi", "ödenecek KDV ne kadar", "devreden KDV", "KDV iadesi", "KDV nakit etkisi", "tevkifat" gibi ifadelerde tetiklenir.
---

# KDV Yükü ve Nakit Etkisi

Türk KDV sisteminin finans yönetimi tarafına bakar: hangi dönemde ne kadar KDV ödeneceği, devreden/iade pozisyonu ve bunun nakit üzerindeki etkisi. Beyanname doldurmaz; karar ve nakit planlaması için analiz üretir.

## Ne zaman tetiklenir
- "Bu dönem ödenecek KDV ne kadar?"
- "Devreden KDV pozisyonumuz nasıl?"
- "KDV iadesi alabilir miyiz, ne kadar?"
- "KDV nakit akışımızı nasıl etkiliyor?"
- "Tevkifatlı satışların KDV etkisini göster"

## Girdi
- Hesaplanan KDV (satış KDV'si) ve indirilecek KDV (alış KDV'si), dönem bazında
- Önceki dönemden devreden KDV (varsa)
- İşlem KDV oranları ve tevkifat oranı (kullanıcıdan al — oranlar mevzuatla değişir)
- Varsa iade doğuran işlemler (ihracat, indirimli oran, kısmi tevkifat)
- Para birimi ve dönem

## Çıktı yapısı
1. **KDV özeti** — Dönem / Hesaplanan / İndirilecek / Devreden / Ödenecek KDV (veya devir)
2. **Pozisyon** — ödeme mi, iade/devir mi; tutar
3. **İade analizi** — iade doğuran işlem varsa yaklaşık iade tutarı ve türü (kısa not)
4. **Nakit etkisi** — KDV ödemesinin nakit akışındaki yeri ve tarihi
5. **Doğrulama notu** — oran/iade detaylarının mali müşavirle teyidi

## Kurallar
- KDV oranlarını sabit yazma; kullanıcıdan işleme uygun güncel oranı iste. Genel/indirimli oranlar dönemsel olarak değişebilir.
- Bu bir analiz aracıdır; KDV beyannamesi, e-defter, mizan kaydı üretmez. Resmi beyan için mali müşavire yönlendir.
- Ödenecek KDV = hesaplanan − (indirilecek + devreden). Negatifse sonraki döneme devreder.
- İade hesabını "yaklaşık" ver; iade süreci ve tutarı tebliğ şartlarına bağlıdır, kesinleştirme.
- Tevkifatta alıcının sorumlu sıfatıyla beyan ettiği kısmı satıcının tahsil ettiğiyle karıştırma.

## Örnek
**Girdi:** Hesaplanan KDV 180.000 TL, indirilecek 120.000 TL, devreden 30.000 TL.
**Çıktı:** Ödenecek KDV = 180.000 − 150.000 = 30.000 TL. Pozisyon: ödeme. Nakit etkisi: beyan dönemini takip eden ödeme tarihinde 30.000 TL çıkış; nakit planına eklenmeli. Oranlar ve iade durumu mali müşavirle teyit edilmeli.
