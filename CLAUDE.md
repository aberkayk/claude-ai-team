# AI Software Team

Bu proje, yazilim gelistirme sureclerini AI agentlar ile yoneten bir multi-agent sistemidir.

## Proje Yapisi

- `.claude/agents/` — Tum agent tanimlari
- `docs/` — Proje dokumantasyonu
  - `docs/architecture/` — Mimari kararlar (ADR formati)
  - `docs/requirements/` — Gereksinim dokumanlari
  - `docs/design/` — UI/UX tasarim dokumanlari
  - `docs/api/` — API dokumantasyonu
  - `docs/testing/` — Test planlari ve raporlari

## Calisma Kurallari

1. Her agent sadece kendi sorumluluk alaninda islem yapar
2. Agentlar arasi iletisim Project Manager uzerinden koordine edilir
3. Tum kararlar `docs/` altinda dokumante edilir
4. Kod degisiklikleri Code Reviewer onayindan gecer
5. Guvenlik kontrolleri her deploy oncesi yapilir

## Agent Kullanimi

Yeni bir ozellik gelistirmek icin:
```
"PM agent'i calistir: [ozellik aciklamasi]"
```

Belirli bir agent'i dogrudan calistirmak icin:
```
"Backend developer: [gorev aciklamasi]"
```

## Konvansiyonlar

- Dokumanlar Turkce yazilir
- Kod yorumlari Ingilizce yazilir
- Commit mesajlari Conventional Commits formatinda olur
- Branch isimleri: `feature/`, `bugfix/`, `hotfix/` prefix'leri kullanir
