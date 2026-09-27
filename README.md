# module-obs

LibreUniversity **Öğrenci Bilgi Sistemi (OBS/SIS)** modülü. Öğrencinin kayıttan mezuniyete kadar resmi akademik süreçlerini yönetir ([MODULES.md §2](https://github.com/Libre-University/docs/blob/main/MODULES.md), [FR-02](https://github.com/Libre-University/docs/blob/main/FUNCTIONAL_REQUIREMENTS.md)).

Bu repo, `platform-api` uygulamasına kurulan bağımsız bir Django uygulama paketidir (`libre-university-obs`). Çekirdeğe yalnızca `libre-university-core` arayüzü üzerinden erişir ([ADR-0010](https://github.com/Libre-University/docs/blob/main/docs/adr/0010-develop-modules-as-separate-packages.md)).

## Ne İş Yapar?

- Öğrenci akademik kaydı ve program ilişkisi
- Müfredat ve müfredat dersleri
- Ders açma (şube, kapasite, dönem)
- Ders kayıt, kontenjan ve çakışma kontrolü
- Danışman onayı
- Değerlendirme kalemleri ve not girişi
- Transkript ve öğrenci belgesi

## Sahip Olduğu Veriler

`Student`, `Curriculum`, `CurriculumCourse`, `CourseSection`, `Enrollment`, `GradeItem`, `Grade` ([DATA_MODEL.md](https://github.com/Libre-University/docs/blob/main/DATA_MODEL.md)).

## Fazlara Göre İşler

| Faz | Bu repoda yapılacaklar |
| --- | --- |
| Faz 0 | Modül şablonundan iskelet, CI, OBS iş kurallarının kabul kriterleri olarak yazılması, alan sözlüğü |
| Faz 1 | `Student`, `Curriculum`, `CurriculumCourse` modelleri ve yönetim API'leri |
| Faz 2 | Ders açma, ders kayıt ve kuyruk, danışman onayı, not girişi, yük testi (MVP'nin ana akışları) |
| Faz 3 | Transkript ve öğrenci belgesi, bildirim entegrasyonu, mobil için okuma API'leri |
| Faz 4+ | Yoklama, staj ve intibak, mezuniyet, aday/kabul, not itiraz iş akışları |

Ayrıntılı ve işaretlenebilir liste: [ROADMAP.md](ROADMAP.md). Fazlar [ana yol haritası](https://github.com/Libre-University/docs/blob/main/ROADMAP.md) ile hizalıdır. Açık işler için `phase:*` etiketlerine bakın.

## Katkı

Katkı rehberi, davranış kuralları ve güvenlik politikası organizasyon genelinde [`.github`](https://github.com/Libre-University/.github) reposundadır. Mimari kararlar [`docs`](https://github.com/Libre-University/docs) reposundaki ADR'lerle alınır.

## Lisans

Bu proje [GNU Affero Genel Kamu Lisansı v3.0 veya sonrası](LICENSE) (AGPL-3.0-or-later) ile lisanslanmıştır. Ağ üzerinden hizmet olarak sunulan değiştirilmiş sürümlerin kaynak kodu da kullanıcılarla paylaşılmalıdır ([ADR-0002](https://github.com/Libre-University/docs/blob/main/docs/adr/0002-prefer-agpl-3-or-later-license.md)).
