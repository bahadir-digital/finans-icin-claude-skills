# Finans için Claude Skills

> Finans profesyonelleri ve dijital CFO'lar için 10 hazır Claude Skill'i. Bütçe, nakit, yaşlandırma, kârlılık, KDV, vergi, kur ve enflasyon analizlerini ham veriden çıkarır.

![lisans](https://img.shields.io/badge/lisans-MIT-green)
![skill](https://img.shields.io/badge/skill-10-orange)
![claude](https://img.shields.io/badge/Claude-Project%20%2B%20Skills-6c5ce7)
![dil](https://img.shields.io/badge/dil-T%C3%BCrk%C3%A7e-blue)

"Türkçe Profesyoneller İçin Claude Skills" serisinin finans paketidir. Skiller günlük tekrar eden finansal analiz işlerine odaklanır ve ham veriyi karar alınabilir çıktıya çevirir. Genel analiz araçlarının yanında Türk finans sistemine özgü KDV, vergi, kur farkı ve enflasyon muhasebesi analizlerini de içerir.

Bu skiller **yönetim seviyesinde analiz** üretir. Resmi beyan, e-defter veya yasal mali tablo yerine geçmez; bu işler mali müşavire aittir.

## İçindekiler

- [Repo yapısı](#repo-yapısı)
- [Kurulum](#kurulum)
- [Paketteki skiller](#paketteki-skiller)
- [Örnek kullanım](#örnek-kullanım)
- [Sınırlar](#sınırlar)
- [Seri](#seri)
- [Katkı](#katkı)
- [Lisans](#lisans)
- [Bağlantılar](#bağlantılar)

## Repo yapısı

```text
finans-icin-claude-skills/
├── README.md
├── PROJECT_INSTRUCTIONS.md
├── variance_analysis/
│   └── SKILL.md
├── cash_flow_tracker/
│   └── SKILL.md
├── aging_analysis/
│   └── SKILL.md
├── profitability_analysis/
│   └── SKILL.md
├── expense_analysis/
│   └── SKILL.md
├── financial_summary/
│   └── SKILL.md
├── kdv_analysis/
│   └── SKILL.md
├── tax_burden_analysis/
│   └── SKILL.md
├── fx_position_analysis/
│   └── SKILL.md
└── inflation_accounting/
    └── SKILL.md
```

Her klasör, tek bir analiz işini tanımlayan bir `SKILL.md` dosyası içerir.

## Kurulum

1. Claude.ai'da yeni bir **Project** oluştur.
2. `PROJECT_INSTRUCTIONS.md` içeriğini Project talimatları alanına yapıştır; köşeli parantezli alanları kendine göre doldur.
3. 10 skill klasörünü `SKILL.md` dosyalarıyla birlikte Project'e yükle.
4. Sohbete başla. Veriyi yapıştır ya da soruyu sor; ilgili skill otomatik devreye girer.

> Skills özelliği için Claude.ai'da uygun bir plan gerekir. Güncel plan ve özellik bilgisi için Claude dokümantasyonuna bakabilirsin.

## Paketteki skiller

| # | Skill | Klasör | Ne işe yarar |
| :-: | --- | --- | --- |
| 1 | Bütçe–Gerçekleşen Sapma Analizi | `variance_analysis` | Plan-fiili fark, kök neden, aksiyon |
| 2 | Nakit Akışı ve Pozisyon Takibi | `cash_flow_tracker` | Nakit pozisyonu, tahsilat-ödeme, runway |
| 3 | Alacak/Borç Yaşlandırma | `aging_analysis` | Yaşlandırma kovaları, gecikme, tahsilat riski |
| 4 | Kârlılık Analizi | `profitability_analysis` | Ürün/müşteri/segment marjı ve kâr kırılımı |
| 5 | Gider Analizi ve Anomali Tespiti | `expense_analysis` | Kategori kırılımı, anomali, gider/ciro oranı |
| 6 | Ham Veriden Hızlı Finansal Özet | `financial_summary` | Tabloyu yapıştır, özet ve uyarıları al |
| 7 | KDV Yükü ve Nakit Etkisi | `kdv_analysis` | Ödenecek/devreden KDV, iade, nakde etki |
| 8 | Vergi Yükü ve Dönem Vergisi Tahmini | `tax_burden_analysis` | Kurumlar/geçici vergi tahmini, efektif oran |
| 9 | Kur Farkı ve Döviz Pozisyonu | `fx_position_analysis` | Açık pozisyon, kur farkı, duyarlılık senaryosu |
| 10 | Enflasyon Muhasebesi Etki Analizi | `inflation_accounting` | Düzeltmenin tablo ve kâra etkisi, parasal kazanç/kayıp |

## Örnek kullanım

```text
Bütçe ile gerçekleşeni karşılaştır, en büyük sapmaları göster.
Önümüzdeki 13 haftanın nakit akışını çıkar, hangi hafta açığa düşeriz?
Alacak yaşlandırma tablosu yap, 90 günü geçenleri işaretle.
Bu mizanı yapıştırıyorum, bana yönetici özeti çıkar.
Ticari kâr şu, KKEG bu; geçici vergi için ne kadar ayıralım?
Döviz pozisyonumuzu netleştir, kur %10 artarsa kâr nasıl etkilenir?
```

## Sınırlar

Yapay zekâ sihir değildir. Bu skiller analizi hızlandırır ama son kontrol sende kalır. Üretilen her rakamı ve yorumu kendi verinle doğrula. Vergi, KDV ve enflasyon düzeltmesi gibi konularda oranlar ve mevzuat değişir; skill'e güncel değeri sen ver ve resmi işlemler için mali müşavirine danış.

## Seri

"Türkçe Profesyoneller İçin Claude Skills" serisinin paketleri:

| # | Meslek | Durum |
| :-: | --- | --- |
| 1 | Öğretmenler | ✅ Yayında |
| 2 | Müşteri Hizmetleri | ✅ Yayında |
| 3 | Finans / Dijital CFO | ✅ Bu paket |
| 4 | İnsan Kaynakları | ⏳ Planlanıyor |
| 5 | Yöneticiler | ✅ Yayında |
| 6 | Satış | ⏳ Planlanıyor |
| 7 | Proje Yöneticileri | ✅ Yayında |
| 8 | Operasyon | ⏳ Planlanıyor |
| 9 | Mali Müşavirler | ⏳ Planlanıyor |

## Katkı

Geri bildirim ve öneriler memnuniyetle karşılanır. Bir hata bulursan ya da eklenmesini istediğin bir analiz varsa Issues üzerinden veya WhatsApp topluluğundan ulaşabilirsin. Skilleri kendi ihtiyacına göre uyarlamak serbesttir.

## Lisans

[MIT](LICENSE) — dilediğin gibi kullan, uyarla, dağıt.

## Bağlantılar

| Kanal | Adres |
| --- | --- |
| Blog | https://bahadir.digital |
| LinkedIn | https://linkedin.com/in/bahadireren |
| Instagram (kişisel) | https://instagram.com/bahadir.digital |
| Instagram (iş/AI) | https://instagram.com/ofiste.ai |
| X | https://x.com/bahadir_digital |
| WhatsApp topluluğu | https://chat.whatsapp.com/I2763pKIpmS9xADAHLaGPE |
| E-posta | bahadireren@gmail.com |
