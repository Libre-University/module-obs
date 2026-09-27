# module-obs Yol Haritası

İş kuralları: [DATA_MODEL.md › Temel İş Kuralları](https://github.com/Libre-University/docs/blob/main/DATA_MODEL.md#temel-i̇ş-kuralları). Akışlar: [UML.md](https://github.com/Libre-University/docs/blob/main/UML.md).

## Faz 0: Hazırlık (davet öncesi)

- [ ] `platform-api` modül şablonundan paket iskeleti (`libre-university-obs`)
- [ ] CI: ruff, mypy, pytest (modül test düzeneğiyle), migration kontrolü
- [ ] Ders açma, ders kayıt ve not girişi iş kurallarının Given/When/Then kabul kriterleri olarak yazılması
- [ ] OBS alan sözlüğü (şube, kontenjan, AKTS, danışman onayı, harf notu…)
- [ ] Modül README'sinde kurulum ve geliştirme adımları

## Faz 1: Temel Modeller

- [ ] `Student` modeli ve program ilişkisi
- [ ] `Curriculum`, `CurriculumCourse`
- [ ] Yönetim API'leri ve yetki kuralları (birim kapsamlı)
- [ ] Yapay örnek veri üreticileri

## Faz 2: MVP Akademik Akışları

- [ ] `CourseSection`: kapasite, şube kodu tekilliği, arşivli ders kontrolü
- [ ] `Enrollment`: kayıt dönemi, aynı derse tek şube, kontenjan, `pending_advisor_approval`
- [ ] Ders kayıt anları için kuyruk tasarımı ve yük testi (50.000 öğrenci senaryosu)
- [ ] Danışman onayı akışı
- [ ] `GradeItem`, `Grade`, dönem sonrası gerekçeli not değişikliği, audit ve bildirim

## Faz 3

- [ ] Transkript ve öğrenci belgesi taslağı (PDF)
- [ ] Mobil uygulama için okuma API'leri

## Faz 4+

- [ ] Yoklama ve devamsızlık
- [ ] Staj, intibak, muafiyet
- [ ] Mezuniyet ve diploma eki
- [ ] Aday ve kabul süreçleri
